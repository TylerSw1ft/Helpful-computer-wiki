# Android

## Developer Options

### Minimum Width

#### [Convert dp units to pixel units](https://developer.android.com/training/multiscreen/screendensities.html#dips-pels)

`px = dp * (dpi / 160)`

`dp = px/dpi/160`

* Use [DisplayInfo](https://play.google.com/store/apps/details?id=it.gerdavax.displayinfo) to find `dpi`
* `px` is display horizontal resolution

## Kernel

### Updates

[Android devices do NOT receive kernel version updates (see Paragraph 3)](https://arstechnica.com/gadgets/2019/11/google-outlines-plans-for-mainline-linux-kernel-support-in-android/)

### Why ARM requires per-device kernel builds (and x86 doesn't)

* [Kernel driver loading](https://www.reddit.com/r/linux/comments/dyv2qi/google_outlines_plans_for_mainline_linux_kernel/f840zb5/)
* [Lack of DeviceTree support](https://www.reddit.com/r/linux/comments/dyv2qi/google_outlines_plans_for_mainline_linux_kernel/f84kokk/)
* [Combination of the above](https://www.reddit.com/r/Android/comments/e5qqn6/engineer_from_samsung_says_chipset_vendors_are_to/f9rq3dm/)

# ANSYS

## Benchmarks

### CFD

* [ANSYS FLUENT Performance Comparison: AMD Opteron vs. Intel XEON](http://www.padtinc.com/blog/ansys-fluent-performance-comparison-amd-opteron-vs-intel-xeon/)
* [Part 2: ANSYS FLUENT Performance Comparison: AMD Opteron vs. Intel XEON](http://www.padtinc.com/blog/part2-ansys-fluent-performance-comparison-amd-opteron-vs-intel-xeon/)
* [Xeon Gold Cascade Lake vs Epyc Rome - CFX & Fluent - Benchmarks (Windows Server 2019)](https://www.cfd-online.com/Forums/hardware/223929-xeon-gold-cascade-lake-vs-epyc-rome-cfx-fluent-benchmarks-windows-server-2019-a.html)

# Backup

## Strategy

### How many copies of data are needed

[3-2-1](https://www.reddit.com/r/DataHoarder/wiki/backups#wiki_the_3-2-1_strategy)

### How to select HDD capacity

Buy the largest capacity HDDs per bay or slot you can afford. Unit storage cost isn't a bad metric, but as fleet size grows, footprint costs begin to dominate. For example, it's less expensive in the long run to have 1 machine with 4x16 TB HDDs than 4 machines with 4x4 TB HDDs each. See the *Retiring Pods* section [here](https://www.soothsawyer.com/ryan-smith-uses-backblazes-smart-data-to-illustrate-the-power-of-data/) for a case study.

# Bash

* [How to check version](https://www.cyberciti.biz/faq/how-do-i-check-my-bash-version/)
* [Writing Scripts on Linux using Bash](https://devconnected.com/writing-scripts-on-linux-using-bash/)
* [Zsh/Bash startup files loading order (.bashrc, .zshrc etc.)](https://shreevatsa.wordpress.com/2008/03/30/zshbash-startup-files-loading-order-bashrc-zshrc-etc/)
* [Advanced Bash Scripting Guide](https://devconnected.com/advanced-bash-scripting-guide/)
* [In commands, `#` means `root`, `$` means any other user](https://unix.stackexchange.com/a/291733)

# `bash-it`

* [How To Customize Bash on Linux with Bash-it](https://computingforgeeks.com/easily-customize-linux-bash-with-bash-it/)
  * After installation, run the following:
    * `bash-it enable completion all`
    * Add `bash-it update` `cron` job to root crontab
    * Enable plugins (`bash-it enable plugin PluginName`) individually and only if necessary. `bash-it enable plugin all` tends to throw errors on login
    * **DO NOT** install `ng-common` as it will break `bash-it`

# BSD

[Manpower issues](https://www.csoonline.com/article/3250653/is-the-bsd-os-dying-some-security-researchers-think-so.html)

## FreeBSD

* [FreeBSD Find Out All Installed Hard Disk Size Information](https://www.cyberciti.biz/faq/freebsd-hard-disk-information/)
* [Shells](https://www.freebsd.org/doc/handbook/shells.html)

## FuryBSD

* [Installation](https://github.com/furybsd/furybsd-handbook/wiki/Installing-FuryBSD)
* [Live USB creation](https://github.com/furybsd/furybsd-livecd/wiki)

## GhostBSD

### Enable `sshd` at startup

In terminal, run `# rc-update add sshd default`

### Mount (Debian 10.2+) NFSv4 share

In terminal, run `# mount -t nfs -o nfsv4 ServerIPAddress:/PathToServerShare LocalMountPath`

### Setup SSH server

Run `# service sshd start` at the terminal.

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

# Computer Science

[Ultimate physical limits to computation](https://arxiv.org/abs/quant-ph/9908043)

# `cp` command

* [Syntax](https://www.computerhope.com/unix/ucp.htm)
* How to copy new scripts to Termux script folder on Android:

`cp /sdcard/SourceFolder/Script.sh ~/.termux/tasker/Script.sh`

e.g. `cp /sdcard/Sync/Scripts/Bash/MoveFilesToSync.sh ~/.termux/tasker/MoveFilesToSync.sh`

# cron

[How to Schedule and Automate tasks in Linux using Cron Jobs](https://www.linuxtechi.com/schedule-automate-tasks-linux-cron-jobs/)

# crontab

## How to edit the root crontab in Debian

Pretty much anything that requires `sudo` needs to be put here:

`# crontab -u root -e`

# Debian

* [Don't Break Debian](https://wiki.debian.org/DontBreakDebian)
* [systemd documentation index](https://wiki.debian.org/systemd/documentation)

# Dell

## BIOS updates using a USB stick

1. Follow Steps 2.1 to 2.6 [here](https://www.dell.com/support/article/us/en/19/sln143196/how-to-create-a-bootable-usb-flash-drive-using-dell-diagnostic-deployment-package-dddp?lang=en)
2. Follow these [instructions](https://www.dell.com/support/article/us/en/19/sln129956/dell-bios-updates?lang=en#Five)

# Disk Erasure

## Windows

[Eraser](http://eraser.heidi.ie/)

# Disqus

[What HTML tags are allowed within comments](https://help.disqus.com/en/articles/1717235-what-html-tags-are-allowed-within-comments)

# Fans

[Effects of Grill Patterns on Fan Performance/Noise](https://www.pugetsystems.com/labs/articles/Effects-of-Grill-Patterns-on-Fan-Performance-Noise-107/)

# Firefox

[ How To Install The Latest Firefox (Non-ESR) On Debian 10 Buster (Stable) Or Bullseye (Testing)](https://www.linuxuprising.com/2019/12/how-to-install-latest-firefox-non-esr.html?m=1)

# Github

[Creating releases](https://help.github.com/en/articles/creating-releases)

# GParted

[Manual](https://gparted.org/display-doc.php?name=help-manual)

# HDDs

* [4k vs. 512](https://community.spiceworks.com/topic/post/6093125) 
  * ([Further discussion](https://www.techpowerup.com/forums/threads/hdd-bytes-per-sector-types-512e-vs-512n-vs-4kn.254422/))
* [Advanced format (4K) disk compatibility update](https://docs.microsoft.com/en-us/windows/win32/w8cookbook/advanced-format--4k--disk-compatibility-update)
* [Don't Know What 4K Hard Drive Is? Look Here!](https://www.partitionwizard.com/partitionmagic/what-is-4k-hard-drive.html)

> 4K native HDD is also called 4Kn hard drive. Both 512 emulated hard drive and 4Kn hard drive are 4K drives as their physical sector size are 4096 (4K) bytes. However, for hard disk drives working in the 4K native mode, there is no emulation layer in place, and the disk media directly exposes its 4096, 4112, 4160, or 4224-byte physical sector size to the system firmware and operating system.

# Illumos

## OpenIndiana

### General documentation

* [Oracle Solaris Information Library](https://docs.oracle.com/cd/E37838_01/)
* [OpenIndiana Docs](http://docs.openindiana.org/)
* [OpenIndiana Wiki](https://wiki.openindiana.org/)

### Packages and publishers (repositories)

* [How to update all packages & system](https://wiki.openindiana.org/oi/3.+Installing+software+and+package+management)
  * Run the following:
    * `# pkgin -y full-upgrade`
    * `# pkgin -y autoremove`
    * `# pkg update -v -r`
    * Check the output of the last command to see if there's a new boot environment to boot into. If there is, reboot the machine
* [Publishers (repos) and how to set them](https://www.openindiana.org/packages/)
* [How to set up, update, and manage packages from pkgsrc repository](https://pkgsrc.joyent.com/install-on-illumos/) 
  * Replace all instances of `gpg` on above page with `gpg2`
  * Edit `PATH` & `MANPATH` variables in `/export/home/YourUsername/.profile` using `pluma`. New lines should look like the code block below
  * `bootstrap-trunk-x86_64-YYYYMMDD.tar.gz` & `bootstrap-trunk-x86_64-YYYYMMDD.tar.gz.asc` can be safely deleted once setup is complete

```
PATH="$HOME/bin:$HOME/.local/bin:/opt/local/sbin:/opt/local/bin:$PATH"
MANPATH=/opt/local/man:$MANPATH
```
* [List of all available pkgsrc packages](https://pkgsrc.joyent.com/packages/SmartOS/trunk/x86_64/All/)
* [How to set up SFE repository](http://sfe.opencsw.org/quickrepolinks)
  * Run `# pfexec pkg set-publisher -G '*' -g http://sfe.opencsw.org/localhostoih localhostoih`

### crontab

* [Creating and Editing crontab Files](https://docs.oracle.com/cd/E37838_01/html/E60997/sysrescron-24589.html#scrolltoc)
* [Syntax of crontab File Entries](https://docs.oracle.com/cd/E37838_01/html/E60997/sysrescron-62861.html#scrolltoc)

### ZFS

#### How to determine which drives a zpool is on

`$ zpool status -v ZPoolName`

# ISA

[The final ISA showdown: Is ARM, x86, or MIPS intrinsically more power efficient?](https://www.extremetech.com/extreme/188396-the-final-isa-showdown-is-arm-x86-or-mips-intrinsically-more-power-efficient/3) Answer: power efficiency is largely independent of ISA

# Latency

[Latency Numbers Every Programmer Should Know](https://colin-scott.github.io/personal_website/research/interactive_latency.html)

# Linux

* [Basic Linux Commands](https://linuxize.com/post/basic-linux-commands/)
* Documentation parody: [You Figure It Out](https://www.youtube.com/watch?v=ZZtu6c_c3W8)
* [Linux Boot Process: What You Should Know](https://www.maketecheasier.com/linux-boot-process/)

# Logical Volume Management

[Logical Volume Management Explained on Linux](https://devconnected.com/logical-volume-management-explained-on-linux/)

# LTO-8 

* [Backwards compatibility](https://www.lto.org/solutions/benefits/compatibility/)
* [Recommended models](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#internal)

# Microsoft Windows 

* [How to perform a clean boot in Windows](https://support.microsoft.com/en-us/help/929135/how-to-perform-a-clean-bot-in-windows)
* [Release channels](https://www.reddit.com/r/sysadmin/comments/e8k8jt/the_release_ring_sku_combo_completely_specify_an/fadyfq3/)
* [Deploy Storage Spaces on a stand-alone server](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces)

# `nano`

[Getting started](https://www.redhat.com/sysadmin/getting-started-nano)

# Napp-it

* [Official Napp-it forum](https://forums.servethehome.com/index.php?forums/solaris-nexenta-openindiana-and-napp-it.26/)
* [HardForum thread](https://hardforum.com/threads/opensolaris-derived-zfs-nas-san-omnios-openindiana-solaris-and-napp-it.1573272/)
* [Setup manual](http://www.napp-it.org/doc/downloads/setup_napp-it_os.pdf)
* [User manual](http://openzfs.hfg-gmuend.de/napp-it_manuals/napp-it.pdf)
* [Tuning](https://napp-it.org/manuals/tuning_en.html)
* [Installation instructions](https://napp-it.org/manuals/nas_en.html) (see **Install napp-it/ setup your NAS ready to use**)
* `napp-it-18.12.zip`, `nappit2.sh`, & `setup-napp-it.log` can all be safely deleted after successful installation

# `nnn`

[Keyboard and mouse](https://github.com/jarun/nnn#keyboard-and-mouse)

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

# Oracle

## Solaris

[The sudden death and eternal life of Solaris](http://dtrace.org/blogs/bmc/2017/09/04/the-sudden-death-and-eternal-life-of-solaris/)

# `pip` for Python 3

## Installation

* [Debian 10](https://linux4one.com/how-to-install-pip-on-debian-10/)
* [Ubuntu 19.04](https://www.serverlab.ca/scripting-programming/install-python-pip-on-ubuntu-19-04/)

## Updating

Run:

`pip3 install -U pip`

# PSUs

## ATX12VO Standard

[Single Rail Power Supply Desktop Platform Form Factors ATX12VO (12 V Only)](https://www.intel.com/content/dam/www/public/us/en/documents/guides/single-rail-power-supply-platform-atx12vo-design-guide.pdf)

## Modular

* [Cables cannot be reliably mixed](https://www.gamersnexus.net/guides/2702-psa-on-mixing-modular-psu-cables-dont-do-it)
* [Why cables cannot be reliably mixed](https://forums.evga.com/FindPost/2646323)

# Pushover

* [Push Notifications from the Command Line Using Pushover](https://mikebuss.com/2014/01/03/push-notifications-cli/)
* [API](https://pushover.net/api)
* [Example code and Pushover libraries](https://support.pushover.app/i44-example-code-and-pushover-libraries)

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

# ReFS

[ReFS integrity streams](https://docs.microsoft.com/en-us/windows-server/storage/refs/integrity-streams)

# Resilio Sync

## Android

[Sync interface on Android](https://help.resilio.com/hc/en-us/articles/213500383-Sync-interface-on-Android-)

# `restic`

* [Including and excluding files](https://restic.readthedocs.io/en/latest/040_backup.html#including-and-excluding-files)
* [Scripting](https://restic.readthedocs.io/en/latest/075_scripting.html)

# S.M.A.R.T.

[ATA S.M.A.R.T. attributes](https://en.wikipedia.org/wiki/S.M.A.R.T.#ATA_S.M.A.R.T._attributes)

# Scripting (Linux)

[How to make a script executable](https://stackoverflow.com/a/43530252/3754100): at script location, run `chmod +x <script-file-name-including-extension>`

# smartmontools

https://www.smartmontools.org/wiki/TocDoc

# SSDs

[The SSD Endurance Experiment: They’re all dead](https://techreport.com/review/27909/the-ssd-endurance-experiment-theyre-all-dead/)

# Structured Cabling

[When you need plenum cable](https://www.reddit.com/r/homelab/comments/ejkrrq/using_solid_core_cat6_cable_with_ip_security/fczrxbs/)

# Synology

[RAID Calculator](https://www.synology.com/en-us/support/RAID_calculator)

# systemd

[How to create a new systemd service](https://www.redhat.com/sysadmin/replacing-rclocal-systemd)

# tsch

[Add a splash of color to your command line environment](https://blogs.aalto.fi/marijn/2016/07/05/add-a-splash-of-color-to-your-command-line-environment/)

# Ubuntu

[How to Easily Add Users to Groups in Ubuntu](https://www.maketecheasier.com/add-remove-user-to-groups-in-ubuntu/) (See Section 2)

# UniFi Controller

* [Transition from MongoDB](https://community.ui.com/user/di3/f30234be-4be5-45e5-abf9-a4c2320f7080) in version 5.13.x
* [EOL Definitions](https://community.ui.com/questions/Announcement-EOL-for-some-UniFi-AP-models/65487283-ce9d-49f4-85b9-b6aa54659ef7)

# UNIX

[What UNIX Cost Us](https://www.youtube.com/watch?v=9-IWMbJXoLM) - A talk about how "the UNIX way" makes a lot of stuff much more difficult than it needs to be

# unRAID

[Calculator](http://unraid.category5.tv/)

# Veeam

## Agent for

### Linux FREE

* [System Requirements](https://helpcenter.veeam.com/docs/agentforlinux/userguide/system_requirements.html?ver=30)
* [User Guide](https://helpcenter.veeam.com/docs/agentforlinux/userguide/overview.html?ver=30)

### Windows FREE

[User Guide](https://helpcenter.veeam.com/docs/agentforwindows/userguide/overview.html?ver=30)

# `vi`

[vi Editor in UNIX](https://www.geeksforgeeks.org/vi-editor-unix/)

# `vifm`

[Cheatsheet](https://vifm.info/cheatsheets.shtml)

# Volume Shadow Copy

* [How to set it up](http://itsimple.info/?p=258)
* [Shadow Explorer (shadow copies browsing tool)](https://www.shadowexplorer.com/downloads.html)

# ZFS 

* [Feature Matrix](https://zgrep.org/zfs.html)
* [Performance, Part 1](https://www.ixsystems.com/blog/zfs-pool-performance-1/)
* [Performance, Part 2](https://www.ixsystems.com/blog/zfs-pool-performance-2/)
* [Quickstart (See Steps 3 to 6)](https://github.com/jdrch/Hardware/wiki/How-to-Set-Up-Regular,-Recurring,-Incremental,-Online-Filesystem-Backups-using-Restic)
* [RAIDZ*x* vs. mirroring resilience to *F* drive destruction](https://github.com/jdrch/Hardware/wiki/How-to-Calculate-the-Odds-of-Physical-Attack-Data-Loss-for-a-ZFS-Array)
* [Latest OpenZFS development status and relationship among projects](https://drive.google.com/file/d/197jS8_MWtfdW2LyvIFnH58uUasHuNszz/view)
* [When To (and Not To) Use RAID-Z](https://blogs.oracle.com/roch/when-to-and-not-to-use-raid-z)
* [Linus Torvalds recommends against ZFS (on Linux)](https://www.realworldtech.com/forum/?threadid=189711&curpostid=189841)

# `zfsnap`

* [Homepage](https://www.zfsnap.org/)
* [Github](https://github.com/zfsnap/zfsnap.org)

# zrep

* [Homepage](http://www.bolthole.com/solaris/zrep/)
* [Github](https://github.com/bolthole/zrep)