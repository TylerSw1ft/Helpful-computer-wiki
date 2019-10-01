# Preamble

Yes, you can use `zfs send` and `zfs receive` for this. However, that requires having another, separate ZFS machine, which is expensive. OTOH, this method allows you to backup to any repository you have access to, regardless of filesystems.

# Why not use disk imaging?

1. [`dump`](https://www.freebsd.org/cgi/man.cgi?dump(8)) doesn't support infinite incremental backups, leading to excessive disk wear on the repository
2. [Bareos supports disaster recovery for Linux only](https://docs.bareos.org/Appendix/DisasterRecoveryUsingBareos.html). Or, at least, it relies on Relax and Recover, [which supports Linux only](http://relax-and-recover.org/download/) 
3. AMANDA backups apparently [do not retain permissions](https://wiki.zmanda.com/index.php/How_To:Do_a_Bare_Metal_Restore) (see 6) there)

# Caveats and constraints

Project Trident, which I use, uses OpenRC as its init system. Unfortunately, the vast majority of OpenRC documentation is written for Gentoo Linux, while FreeBSD documentation and guides are written for rc.d. This leaves Trident in a bit of a support no man's land when it comes to services, and so many 3rd party packages available in AppCafe that rely on services don't work reliably. This apparently includes the samba client. **Ergo, the aim here is avoid solutions that rely on services running on Trident, unless I can somehow get them running**.

As such, backup to the respository will have to occur using the backup app itself, NFS, or SSH. 

# Method Source Links

* https://forums.freebsd.org/threads/copying-freebsd-to-a-different-disk.55606/post-315655
* https://www.reddit.com/r/freebsd/comments/d712mz/generally_speaking_how_do_i_restore_an_entire_os/f17t0fi/
* http://www.wonkity.com/~wblock/docs/html/backup.html#_em_dump_8_em_em_restore_8_em

# Disqualified Applications

## Borg

FreeBSD package [apparently needs to be built locally](https://www.freshports.org/archivers/py-borgbackup), which is problematic.

## BackupPC 

Crappy documention.

## UrBackup

* Can't get Server and Client to see each other on the same subnet
* Matching UrBackup forum [thread](https://forums.urbackup.org/t/need-help-getting-freebsd-urbackup-client-v2-3-4-1-to-see-debian-10-urbackup-server-on-the-same-subnet/7725)
* Installed server on [Debian 10 machine](https://github.com/jdrch/Hardware/blob/master/Dell%20OptiPlex%20390-1%20SFF.md)
* Got client backend running on [Trident machine](https://github.com/jdrch/Hardware/blob/master/Dell%20OptiPlex%20390%20SFF.md)

Wrote OpenRC script:

    #!/sbin/openrc-run
    name="urbackup_client"
    description="UrBackup Client"
    command=/usr/local/sbin/urbackupclientbackend
    pidfile="/var/run/urbackupclientbackend.pid"
    command_args="-w $pidfile -c /usr/local/etc/urbackup/urbackupclient.conf"
    supervisor=supervise-daemon
    output_log="/var/log/urbackupclient.log"
    error_log=${output_log}

    depend(){
	    provide urbackup_client
	    need localmount
	    use net
    }

Ken Moore [says](https://t.me/ProjectTrident/39203) I should create a pull request for this [in the TrueOS ports repo](https://github.com/trueos/trueos-ports/tree/trueos-master/archivers/urbackup-client).

I can start urbackupclientbackend in the background using `sudo /usr/local/sbin/urbackupclientbackend -d`, but so far `sudo urbackupclientctl set-settings` returns me to the command prompt.

Client log files indicate it's not seeing the server:

    2019-09-26 09:49:06: urbackupserver: Server started up successfully!
    2019-09-26 09:49:06: FileSrv: Servername: -DellOptiplex390-
    2019-09-26 09:49:06: Started UrBackupClient Backend...
    2019-09-26 09:49:07: Looking for old Sessions... 0 sessions
    2019-09-26 10:19:08: Looking for old Sessions... 0 sessions
    2019-09-26 10:49:09: Looking for old Sessions... 0 sessions
    [...]
    2019-09-27 07:49:51: Looking for old Sessions... 0 sessions
    2019-09-27 08:19:52: Looking for old Sessions... 0 sessions
    2019-09-27 08:49:53: Looking for old Sessions... 0 sessions
    2019-09-27 09:18:30: WARNING: Shutting down (Signal 2)
    2019-09-27 09:18:30: Deleting lbs...
    2019-09-27 09:18:30: Shutting down plugins...
    2019-09-27 09:18:30: Deleting server...

Per [Debian's documentation](https://wiki.debian.org/DebianFirewall#Basic_software_for_network_traffic_manipulation), it's configured to allow all traffic by default, which means the lack of connectivity probably isn't due to the server. At this point, I'm giving up on getting UrBackup to work on Trident, aside from committing code corresponding to what I've learned from the attempt so far. 

# Candidate Applications

## Restic

* Got it working, but having problems with [poor transfer speeds](https://www.reddit.com/r/DataHoarder/comments/dbikbg/how_do_i_speed_up_my_restic_on_freebsd_12_to_nfs/). Suggested remedies:
  * Do a [network speed test](https://www.reddit.com/r/homelab/comments/dbin7u/how_do_i_speed_up_my_restic_on_freebsd_12_to_nfs/f2217bh/). Did it on Debian 10 server via my ISP's tool 1st since I have a 200 Mb·s^-1 connection, got this passing result:

![](https://raw.githubusercontent.com/jdrch/Hardware/master/Mediacom%20Cable%20%20%20Speed%20Test%202019-09-30.png)

  * Check NIC link rate/connection speed
    * https://www.cyberciti.biz/faq/howto-determine-ethernet-connection-speed/

Using `ethtool` (which has to be installed 1st) on Debian 10 server:

    sudo ethtool enp4s0
    Settings for enp4s0:
        Supported ports: [ TP MII ]
        Supported link modes:   10baseT/Half 10baseT/Full 
                                100baseT/Half 100baseT/Full 
                                1000baseT/Half 1000baseT/Full 
        Supported pause frame use: Symmetric Receive-only
        Supports auto-negotiation: Yes
        Supported FEC modes: Not reported
        Advertised link modes:  10baseT/Half 10baseT/Full 
                                100baseT/Half 100baseT/Full 
                                1000baseT/Half 1000baseT/Full 
        Advertised pause frame use: Symmetric Receive-only
        Advertised auto-negotiation: Yes
        Advertised FEC modes: Not reported
        Link partner advertised link modes:  10baseT/Half 10baseT/Full 
                                             100baseT/Half 100baseT/Full 
                                             1000baseT/Full 
        Link partner advertised pause frame use: Symmetric Receive-only
        Link partner advertised auto-negotiation: Yes
        Link partner advertised FEC modes: Not reported
        Speed: 1000Mb/s
        Duplex: Full
        Port: MII
        PHYAD: 0
        Transceiver: internal
        Auto-negotiation: on
        Supports Wake-on: pumbg
        Wake-on: g
        Current message level: 0x00000033 (51)
                               drv probe ifdown ifup
        Link detected: yes

That looks like a pass to me.

On the Trident machine:

    ifconfig
    re0: flags=8843<UP,BROADCAST,RUNNING,SIMPLEX,MULTICAST> metric 0 mtu 1500
        options=8209b<RXCSUM,TXCSUM,VLAN_MTU,VLAN_HWTAGGING,VLAN_HWCSUM,WOL_MAGIC,LINKSTATE>
        [redacted lines]
        media: Ethernet autoselect (1000baseT <full-duplex>)
        status: active
        nd6 options=23<PERFORMNUD,ACCEPT_RTADV,AUTO_LINKLOCAL>

That looks like a pass also.

### NFS Resources

* [FreeBSD NFSv4 man page](https://www.freebsd.org/cgi/man.cgi?query=nfsv4)
* https://linuxconfig.org/how-to-set-up-a-nfs-server-on-debian-10-buster
* [Linux exports man page](https://linux.die.net/man/5/exports)
* [FreeBSD fstab man page](https://www.freebsd.org/cgi/man.cgi?query=fstab&apropos=0&sektion=0&manpath=FreeBSD+12.0-RELEASE+and+Ports&arch=default&format=html)