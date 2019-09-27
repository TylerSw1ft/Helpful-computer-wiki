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

# Disqualified Applications

## Borg

FreeBSD package [apparently needs to be built locally](https://www.freshports.org/archivers/py-borgbackup), which is problematic.

## BackupPC 

Crappy documention.

# Candidate Applications

## UrBackup

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

## Restic

* Already works for folder backup on Trident machine. Might have to use it to backup entire filesystem also
* Needs NFS to work

### NFS Resources

* [FreeBSD man page](https://www.freebsd.org/cgi/man.cgi?query=nfsv4)
* https://linuxconfig.org/how-to-set-up-a-nfs-server-on-debian-10-buster
* https://www.server-world.info/en/note?os=Debian_10&p=nfs&f=1