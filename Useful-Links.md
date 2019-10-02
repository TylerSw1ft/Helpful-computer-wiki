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

# crontab

## How to edit the root crontab in Debian

Pretty much anything that requires `sudo` needs to be put here:

`sudo crontab -u root -e`

# LTO-8 

[Backwards compatibility](https://www.lto.org/solutions/benefits/compatibility/)

# `nano`

[Getting started](https://www.redhat.com/sysadmin/getting-started-nano)

# OpenRC

My advice with OpenRC is to interact with it only:

1. For apps included in your distribution base
2. For apps that explicitly support it
3. Never otherwise

## Converting between OpenRC and rc.d

* [OpenRC vs rc.dCompare and contrast (PDF warning)](http://www.wonkity.com/~wblock/openrc/OpenRC_rc.d.pdf)
* [Gentoo OpenRC to systemd Cheatsheet](https://wiki.gentoo.org/wiki/OpenRC_to_systemd_Cheatsheet)
* [Gentoo Comparison of init systems](https://wiki.gentoo.org/wiki/Comparison_of_init_systems)

## General documentation (written for Gentoo Linux)

* [Gentoo OpenRC Wiki](https://wiki.gentoo.org/wiki/OpenRC)
* [Gentoo supervise-daemon Tips 'n Tricks](https://wiki.gentoo.org/wiki/OpenRC/supervise-daemon#Tips_.27n_tricks)

# RAID

* [Explanation of parity and redundancy levels](http://www.raid-calculator.com/raid-types-reference.aspx)
* [Drive count vs. drive capacity vs. redundancy level vs. time reliability chart](https://www.reddit.com/r/synology/comments/6fld1a/comparison_of_reliability_among_different_raid/)
* [Reliability calculator](https://wintelguy.com/raidmttdl.pl)

# `restic`

* [How to set it up (written for Project Trident, but generally applicable)](https://github.com/project-trident/trident-docs/blob/master/restic.md)
* [Including and excluding files](https://restic.readthedocs.io/en/latest/040_backup.html#including-and-excluding-files)
* [Scripting](https://restic.readthedocs.io/en/latest/075_scripting.html)

# smartmontools

https://www.smartmontools.org/wiki/TocDoc

# systemd

[How to create a new systemd service](https://www.redhat.com/sysadmin/replacing-rclocal-systemd)

# Volume Shadow Copy

* [How to set it up](http://itsimple.info/?p=258)
* [Shadow Explorer (shadow copies browsing tool](https://www.shadowexplorer.com/downloads.html)

# ZFS 

* [Quickstart (See Steps 3 to 6)](https://github.com/project-trident/trident-docs/blob/master/restic.md)

# `zfsnap`

* [How to set it up](https://github.com/project-trident/trident-docs/blob/master/zfssnap.md)