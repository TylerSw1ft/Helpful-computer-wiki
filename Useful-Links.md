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

### How many copies of data are needed

[3-2-1](https://www.reddit.com/r/DataHoarder/wiki/backups#wiki_the_3-2-1_strategy)

### How to select HDD capacity

Buy the largest capacity HDDs per bay or slot you can afford. Unit storage cost isn't a bad metric, but as fleet size grows, footprint costs begin to dominate. For example, it's less expensive in the long run to have 1 machine with 4x16 TB HDDs than 4 machines with 4x4 TB HDDs each. See the *Retiring Pods* section [here](https://www.soothsawyer.com/ryan-smith-uses-backblazes-smart-data-to-illustrate-the-power-of-data/) for a case study.

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

# CLIs vs. GUIs

[Most system administrators prefer firewall GUIs over CLIs](https://www.zdnet.com/article/most-system-administrators-prefer-firewall-guis-over-clis/)

# Cockpit

* [Installation on Debian and Ubuntu](https://computingforgeeks.com/how-to-install-cockpit-on-ubuntu-18-04-debian-9/)
* [Setting it up to start on boot](https://cockpit-project.org/guide/latest/startup.html#startup-boot)
* [Cockpit and the evolution of the Web User Interface](https://fedoramagazine.org/cockpit-and-the-evolution-of-the-web-user-interface/)
* [Performing storage management tasks in Cockpit](https://fedoramagazine.org/performing-storage-management-tasks-in-cockpit/)
* [Managing software and services with Cockpit](https://fedoramagazine.org/managing-software-and-services-with-cockpit/)

# cron

[How to Schedule and Automate tasks in Linux using Cron Jobs](https://www.linuxtechi.com/schedule-automate-tasks-linux-cron-jobs/)

# crontab

## How to edit the root crontab in Debian

Pretty much anything that requires `sudo` needs to be put here:

`sudo crontab -u root -e`

# Disk Erasure

## Windows

[Eraser](http://eraser.heidi.ie/)

# Disqus

[What HTML tags are allowed within comments](https://help.disqus.com/en/articles/1717235-what-html-tags-are-allowed-within-comments)

# Github

[Creating releases](https://help.github.com/en/articles/creating-releases)

# ISA

[The final ISA showdown: Is ARM, x86, or MIPS intrinsically more power efficient?](https://www.extremetech.com/extreme/188396-the-final-isa-showdown-is-arm-x86-or-mips-intrinsically-more-power-efficient/3) Answer: power efficiency is largely independent of ISA

# LTO-8 

* [Backwards compatibility](https://www.lto.org/solutions/benefits/compatibility/)
* [Recommended models](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#internal)

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

# PSUs

## Modular

* [Cables cannot be reliably mixed](https://www.gamersnexus.net/guides/2702-psa-on-mixing-modular-psu-cables-dont-do-it)
* [Why cables cannot be reliably mixed](https://forums.evga.com/FindPost/2646323)

# [r/DataHoarder](https://www.reddit.com/r/DataHoarder/)

[Wiki](https://old.reddit.com/r/DataHoarder/wiki/index)

# RAID

* [Explanation of parity and redundancy levels](http://www.raid-calculator.com/raid-types-reference.aspx)
* [Drive count vs. drive capacity vs. redundancy level vs. time reliability chart](https://www.reddit.com/r/synology/comments/6fld1a/comparison_of_reliability_among_different_raid/)
* [Reliability calculator](https://wintelguy.com/raidmttdl.pl)
* [Performance calculator](https://blog.storagecraft.com/raid-performance/)

## DRAID (Distributed RAID)

* [Some details about how DRAID works](https://www.ibm.com/developerworks/community/blogs/svcstorwize/entry/Some_details_about_how_DRAID_works?lang=en)

> Distributed RAID was launched in 7.6.0 and allows a RAID5 or RAID6 array to be distributed over a larger set of drives. Previously if you created a RADI5 array over 8 drives, the data was striped across them with each stripe having a data strip on 7 of the drives and a parity strip on the 8th. In distributed RAID5 you specify the stripe width and the number of drives separately so you can still have 7 data strips protected by a parity strip but those 8 drives are selected from 64. On top of that we added distributed sparing, this is the idea that instead of having a spare sat on the side that isn't being used, each drive in the array gives up some of its capacity to make a spare.

# `restic`

* [Including and excluding files](https://restic.readthedocs.io/en/latest/040_backup.html#including-and-excluding-files)
* [Scripting](https://restic.readthedocs.io/en/latest/075_scripting.html)

# S.M.A.R.T.

[ATA S.M.A.R.T. attributes](https://en.wikipedia.org/wiki/S.M.A.R.T.#ATA_S.M.A.R.T._attributes)

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
* [Quickstart (See Steps 3 to 6)](https://github.com/jdrch/Hardware/wiki/How-to-Set-Up-Regular,-Recurring,-Incremental,-Online-Filesystem-Backups-using-Restic)
* [RAIDZ*x* vs. mirroring resilience to *F* drive destruction](https://github.com/jdrch/Hardware/wiki/How-to-Calculate-the-Odds-of-Physical-Attack-Data-Loss-for-a-ZFS-Array)