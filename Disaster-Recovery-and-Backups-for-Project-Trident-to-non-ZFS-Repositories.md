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

* Installed server on Debian 10 machine
* Currently trying to get client running on Trident machine. Mike Remski of the Project Trident Telegram [has an idea](https://t.me/ProjectTrident/38834) about this, and the FreeBSD port's maintainer has replied to my email asking for help. He said:

> Have you tried the RC script?
> `/usr/local/etc/rc.d/urbackup_client`

> You normally start the client service with the RC script, and then configure it with the server’s web interface, or with > urbackupclientctl.

> There’s also information in the port’s pkg-message.

## Restic

* Already works for folder backup on Trident machine. Might have to use it to backup entire filesystem also
* Needs NFS to work

### NFS Resources

* [FreeBSD man page](https://www.freebsd.org/cgi/man.cgi?query=nfsv4)
* https://linuxconfig.org/how-to-set-up-a-nfs-server-on-debian-10-buster
* https://www.server-world.info/en/note?os=Debian_10&p=nfs&f=1