# Android

## Developer Options

### Minimum Width

#### [Convert dp units to pixel units](https://developer.android.com/training/multiscreen/screendensities.html#dips-pels)

`px = dp * (dpi / 160)`

`dp = px/dpi/160`

* Use [DisplayInfo](https://play.google.com/store/apps/details?id=it.gerdavax.displayinfo) to find `dpi`
* `px` is display horizontal resolution

# Backup

## Strategy

[3-2-1](https://www.reddit.com/r/DataHoarder/wiki/backups#wiki_the_3-2-1_strategy)

# Btrfs

[Cheatsheet](https://blog.programster.org/btrfs-cheatsheet)

## Creation

Use default values

## fstab

Tab separated:

`UUID=Insert_UUID_Here   /path/to/Btrfs/filessystem  btrfs   defaults,autodefrag 0   0`

## Scheduled scrubs

Should be performed monthly. Put the following in the [root crontab](https://github.com/jdrch/Hardware/wiki/Useful-Links#how-to-edit-the-root-crontab-in-debian):

`@monthly btrfs scrub start /path/to/Btrfs/filessystem`

# Cockpit

* [Installation on Debian and Ubuntu](https://computingforgeeks.com/how-to-install-cockpit-on-ubuntu-18-04-debian-9/)
* [Setting it up to start on boot](https://cockpit-project.org/guide/latest/startup.html#startup-boot)

# crontab

## How to edit the root crontab in Debian

Pretty much anything that requires `sudo` needs to be put here:

`sudo crontab -u root -e`

# Disqus

[What HTML tags are allowed within comments](https://help.disqus.com/en/articles/1717235-what-html-tags-are-allowed-within-comments)

# Github

[Creating releases](https://help.github.com/en/articles/creating-releases)

# LTO-8 

* [Backwards compatibility](https://www.lto.org/solutions/benefits/compatibility/)
* [Internal drives](https://iq.quantum.com/exLink.asp?10444458OP44N16I37407297&view=1)
  * Recommended models:
    * TC-L82AN-EY
    * TC-L82AN-BR

# `nano`

[Getting started](https://www.redhat.com/sysadmin/getting-started-nano)

# OpenRC

My OpenRC advice is to interact with it only:

1. For apps included in your distribution base
2. For apps that explicitly support it
3. Never otherwise

## Converting between OpenRC and rc.d

* [OpenRC vs rc.d Compare and contrast (PDF warning)](http://www.wonkity.com/~wblock/openrc/OpenRC_rc.d.pdf)
* [Gentoo OpenRC to systemd Cheatsheet](https://wiki.gentoo.org/wiki/OpenRC_to_systemd_Cheatsheet)
* [Gentoo Comparison of init systems](https://wiki.gentoo.org/wiki/Comparison_of_init_systems)

## General documentation (written for Gentoo Linux)

* [Gentoo OpenRC Wiki](https://wiki.gentoo.org/wiki/OpenRC)
* [Gentoo supervise-daemon Tips 'n Tricks](https://wiki.gentoo.org/wiki/OpenRC/supervise-daemon#Tips_.27n_tricks)

# `pip` for Python 3

# Installation

* [Debian 10](https://linux4one.com/how-to-install-pip-on-debian-10/)
* [Ubuntu 19.04](https://www.serverlab.ca/scripting-programming/install-python-pip-on-ubuntu-19-04/)

# Updating

Run:

`pip3 install -U pip`

# RAID

* [Explanation of parity and redundancy levels](http://www.raid-calculator.com/raid-types-reference.aspx)
* [Drive count vs. drive capacity vs. redundancy level vs. time reliability chart](https://www.reddit.com/r/synology/comments/6fld1a/comparison_of_reliability_among_different_raid/)
* [Reliability calculator](https://wintelguy.com/raidmttdl.pl)
* [Performance calculator](https://blog.storagecraft.com/raid-performance/)

# `restic`

* [Including and excluding files](https://restic.readthedocs.io/en/latest/040_backup.html#including-and-excluding-files)
* [Scripting](https://restic.readthedocs.io/en/latest/075_scripting.html)

# smartmontools

https://www.smartmontools.org/wiki/TocDoc

# systemd

[How to create a new systemd service](https://www.redhat.com/sysadmin/replacing-rclocal-systemd)

# Veeam

## Agent

### for Linux FREE

[System Requirements](https://helpcenter.veeam.com/docs/agentforlinux/userguide/system_requirements.html?ver=30)

# Volume Shadow Copy

* [How to set it up](http://itsimple.info/?p=258)
* [Shadow Explorer (shadow copies browsing tool](https://www.shadowexplorer.com/downloads.html)

# ZFS 

* [Performance, Part 1](https://www.ixsystems.com/blog/zfs-pool-performance-1/)
* [Performance, Part 2](https://www.ixsystems.com/blog/zfs-pool-performance-2/)
* [Quickstart (See Steps 3 to 6)](https://github.com/jdrch/Hardware/wiki/How-to-Set-Up-Regular,-Recurring,-Recursive,-Incremental,-Online,-In-Place-Filesystem-Backups-Using-zfsnap)
* [RAIDZ*x* vs. mirroring resilience to *F* drive destruction](https://github.com/jdrch/Hardware/wiki/How-to-Calculate-the-Odds-of-Physical-Attack-Data-Loss-for-a-ZFS-Array)