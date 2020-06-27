# WARNING: The links on this page are not necessarily exhaustive with respect to each heading/topic

# Android

[OEM support windows](https://www.reddit.com/r/Android/comments/gd35u6/are_we_and_all_the_tech_reviewers_counting/fpg32oe/)

## Developer Options

### Minimum Width

#### [Convert dp units to pixel units](https://developer.android.com/training/multiscreen/screendensities.html#dips-pels)

`px = dp(dpi/160)`

`dp = 160px/dpi`

* Use [DisplayInfo](https://play.google.com/store/apps/details?id=it.gerdavax.displayinfo) to find `dpi`
* `px` is display horizontal resolution

## Kernel

### Updates

[Android devices do NOT receive kernel version updates (see Paragraph 3)](https://arstechnica.com/gadgets/2019/11/google-outlines-plans-for-mainline-linux-kernel-support-in-android/)

### Why ARM requires per-device kernel builds (and x86 doesn't)

* [Kernel driver loading](https://www.reddit.com/r/linux/comments/dyv2qi/google_outlines_plans_for_mainline_linux_kernel/f840zb5/)
* [Lack of DeviceTree support](https://www.reddit.com/r/linux/comments/dyv2qi/google_outlines_plans_for_mainline_linux_kernel/f84kokk/)
* [Combination of the above](https://www.reddit.com/r/Android/comments/e5qqn6/engineer_from_samsung_says_chipset_vendors_are_to/f9rq3dm/)

## LineageOS

### How to determine upstream AOSP security patch status

Search the page at the following URL for “security string” :

`https://github.com/LineageOS/android_build/blob/lineage-X.Y/core/version_defaults.mk`

Where `X.Y` is the LineageOS version you’re using, e.g. 16.0. You should see a date which corresponds to an upstream Android patch date.

# ANSYS

## Benchmarks

### CFD

* ANSYS FLUENT Performance Comparison: AMD Opteron vs. Intel XEON, Part
  * [1](http://www.padtinc.com/blog/ansys-fluent-performance-comparison-amd-opteron-vs-intel-xeon/)
  * [2](http://www.padtinc.com/blog/part2-ansys-fluent-performance-comparison-amd-opteron-vs-intel-xeon/)
* [Xeon Gold Cascade Lake vs Epyc Rome - CFX & Fluent - Benchmarks (Windows Server 2019)](https://www.cfd-online.com/Forums/hardware/223929-xeon-gold-cascade-lake-vs-epyc-rome-cfx-fluent-benchmarks-windows-server-2019-a.html)

## Mechanical 2020 R1

* How to resolve the "The shared license is current not available for this application" error
  * Click `Start`
  * Search for `Server (or Client) ANSLIC_ADMIN Utility 2020 R1`
  * Click `Run as Administrator`
  * In the window that pops up, click `Set License Preferences for User YourUsername`
  * Click the `2020 R1` radio button and click `OK`
  * Ensure all the tabs in the window that pops up have the `Use a separate license for each application`
  * Click `Apply`
  * Click `OK`

* How to resolve Model cells opening as Read-Only
  * On the License Server:
    * Click `Start`
    * Click `Ansys Inc License Manager`
    * Right-click on `SERVER ANSLIC_ADMIN`
    * Click `Run as Administrator`
    * Go to `Set Site Preferences` -> `Specify Product Order` -> `v12 and higher`
    * Click `Reset to Default`
  * On the workstation, *after the above has been completed*:
    * Open Workbench
    * Go to `Tools` -> `License Preferences`
    * Click `Reset to Default`
    * Quit and reopen Workbench

# `apt`

* [Fixing “The following packages have been kept back” Error While Updating Ubuntu and Debian-based Linux Distributions](https://itsfoss.com/following-packages-have-been-kept-back/)
* [How to clean up sources](https://askubuntu.com/a/762815/932418)
* How to find a package's installed dependencies: `# apt-cache rdepends --installed PackageName`. For soft dependencies (which may or may not be already installed) use `# apt show PackageName`

# Backup

## Strategy

### How many copies of data are needed

[3-2-1](https://www.reddit.com/r/DataHoarder/wiki/backups#wiki_the_3-2-1_strategy)

### How to select HDD capacity

Buy the largest capacity HDDs per bay or slot you can afford. Unit storage cost isn't a bad metric, but as fleet size grows, footprint costs begin to dominate. For example, it's less expensive in the long run to have 1 machine with 4x16 TB HDDs than 4 machines with 4x4 TB HDDs each. See the *Retiring Pods* section [here](https://www.soothsawyer.com/ryan-smith-uses-backblazes-smart-data-to-illustrate-the-power-of-data/) for a case study.

# Baloo file indexer

How to disable:

```
$ balooctl suspend
$ balooctl disable
```

# Bash

* [Advanced Bash Scripting Guide](https://devconnected.com/advanced-bash-scripting-guide/)
* [bash history](https://www.unixtutorial.org/bash-history)
* [How to check version](https://www.cyberciti.biz/faq/how-do-i-check-my-bash-version/)
* [In commands, `#` means `root`, `$` means any other user](https://unix.stackexchange.com/a/291733)
* [Writing Scripts on Linux using Bash](https://devconnected.com/writing-scripts-on-linux-using-bash/)
* [Zsh/Bash startup files loading order (.bashrc, .zshrc etc.)](https://shreevatsa.wordpress.com/2008/03/30/zshbash-startup-files-loading-order-bashrc-zshrc-etc/)

# BSD

* [macOS has BSD code in the kernel](https://developer.apple.com/library/archive/documentation/Darwin/Conceptual/KernelProgramming/Architecture/Architecture.html#//apple_ref/doc/uid/TP30000905-CH1g-CACDCAGC)
* [Manpower issues](https://www.csoonline.com/article/3250653/is-the-bsd-os-dying-some-security-researchers-think-so.html)

## FreeBSD

* [Directory Structure](https://www.freebsd.org/doc/handbook/dirstructure.html)
* [FreeBSD Find Out All Installed Hard Disk Size Information](https://www.cyberciti.biz/faq/freebsd-hard-disk-information/)
* [FreeBSD 12.1 on a laptop](https://dataswamp.org/~solene/2020-05-11-freebsd-workstation.html)
* [How To Enable SSH On FreeBSD](https://www.ostechnix.com/how-to-enable-ssh-on-freebsd/)
* [How to show package post-installation notes](https://forums.freebsd.org/threads/how-to-reshow-post-installation-notes.63839/): `$ pkg info -D PackageName`
* [How to use pkg-status.freebsd.org](https://forums.freebsd.org/threads/is-it-just-me-or-is-chromium-unavailable-in-latest-pgk-repo-for-12-1-release-p2.74501/post-455633)
  1. At the main page, click the filter icon to the left of `Package Builds`
  2. Type the concatenation of the FreeBSD version and platform you're interested in, e.g. `121amd64`, into the search box
  3. Click the number in the `Build` column corresponding to the `Ports` column `pkg` repo of interest, where `default` = `latest` and `quarterly` = `quarterly`
  4. If looking for failed or skipped packages, check those headings in the page that follows
  5. If the desired package isn't there, click `previous build` and repeat iv)
* [How to switch packages from `quarterly` to `latest`](https://www.reddit.com/r/freebsd/comments/fg7598/pkg_removes_firefox_on_update_help_freebsd/fk6s2mo/)
* [Instant Workstation](https://euroquis.nl/freebsd/2019/08/12/instant-workstation.html): A script that automagically sets up KDE on a FreeBSD installation
* [Quarterly and Latest Ports Branches](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/pkgng-intro.html) (See Section 4.4.2)
* [Shells](https://www.freebsd.org/doc/handbook/shells.html)
* [Technical reasons to choose FreeBSD over GNU/Linux](https://unixsheikh.com/articles/technical-reasons-to-choose-freebsd-over-linux.html)

### Ports

* [FreshPorts](https://www.freshports.org/)
* [FreeBSD Ports Categories Listed By Groups](https://www.freebsd.org/ports/categories-grouped.html) (searchable)

## FuryBSD

* [Installation](https://github.com/furybsd/furybsd-handbook/wiki/Installing-FuryBSD)
* [Live USB creation](https://github.com/furybsd/furybsd-livecd/wiki)

### KDE

#### [How to fix keyboard keys triggering the wrong things](https://www.reddit.com/r/freebsd/comments/fjfpa5/freebsd_121releasep2_dell_xd31_usb_multimedia/fknl59g/) (such as `End` raising the Application Menu)

* Add `export XKB_DEFAULT_RULES=evdev` to `~/.xprofile`. If the file does not exist, create it first and then add the line
* Reboot

### How to enable `sudo` for a user

* Append `username ALL=(ALL) ALL` to `/etc/sudoers` or `/usr/local/etc/sudoers`

### How to mount (Debian 10.2+) NFSv4 share

In terminal, run `# mount -t nfs -o nfsv4 ServerIPAddress:/PathToServerShare /LocalMountPath`

The equivalent `/etc/fstab` entry for this is apparently `ServerIPAddress:/PathToServerShare  /LocalMountPath                     nfs     rw,nfsv4acls    0 0`

### How to set up multiple monitors on Dell OptiPlex 390 SFF

* Connect HDMI monitor only
* UEFI boot into the live USB
* Click `Xorg Setup`
* In the window that pops up, select `Intel`
* Click `OK`
* In the list that follows, select `xf86-video-intel`
* Click `OK`
* Complete installation process
* Reboot
* Connect VGA monitor
* Reboot

The 2 monitors should now have an extended desktop. Use `Meta` -> `Display Settings` to configure them.

### How to set up UEFI boot on Dell OptiPlex 390 SFF

* UEFI boot into the live USB
* Install FuryBSD
* Enter BIOS
* In the boot sequence, delete all other entries except the UEFI one, and ensure the `UEFI` radio button is selected
* Click `Add boot option`
* Browse down through each successive folder to find a file that looks like `bootx64.efi` and select it
* Name the boot method `FuryBSD`
* Click `OK`
* Ensure `FuryBSD` is checked in the UEFI boot list
* Click `Apply`
* Click `Exit`

### Resilio Sync

#### How to set up

1. Download the FreeBSD archive from the Resilio Sync website
2. Extract the FreeBSD archive
3. Place the `rslsync` binary in `/bin`

##### as root

1. Start Resilio Sync by running `cd /bin && sudo ./rslsync`
2. To run Resilio Sync at boot, add the following entry to `/etc/crontab`: `@reboot root cd /bin && ./rslsync`

##### as MyUsername

1. Complete 1) of **as root** instructions
2. Kill the `rslsync` process
3. Copy `.sync` from `/bin` to `~/`
4. Change the permissions and ownership of the `.sync` copy to grant MyUsername `rwx` and ownership
5. Start Resilio Sync by running `cd /bin && ./rslsync --storage /absolute/path/to/home/.sync/folder` ([Source](https://forum.resilio.com/topic/71858-linuxbsd-how-do-i-move-sync-from-running-as-root-to-running-as-my-user-without-having-to-setup-from-scratch/?do=findComment&comment=153863))
6. To run Resilio Sync at boot, add the following entry to `/etc/crontab`: `@reboot MyUsername cd /bin && ./rslsync --storage /absolute/path/to/home/.sync/folder`

#### How to update

##### as MyUsername

1. Download the new archive
2. Extract the new archive
3. Kill the `rslsync` process
4. Overwrite `/bin/rslsync` with the binary extracted in 2)
5. Run `# chmod +x /bin/rslsync`
6. Run `./rslsync --storage /absolute/path/to/home/.sync/folder` to start `rslsync`

## Why I might no longer run BSD

TL,DR: it's too much trouble.

* I need a DE. This eliminates NetBSD and Dragonfly BSD
* I need native ZFS support. This eliminates OpenBSD
* I need proper rc.d support. This eliminates GhostBSD, which uses OpenRC
  * I used GhostBSD for around 2 months, but eventually dropped it due to limited features (MATE is about as useless a DE as you can imagine) and stuff just not working reliably. The latter included, but it not limited to
    * I couldn't get 3rd party services to start reliably at boot. I wound up having to use an `@reboot` crontab entry as a workaround, but of course that doesn't help if the service crashes
    * I couldn't get NFS shares to mount reliably at boot, even with an `@reboot` crontab entry, or to mount at all otherwise at times
* FuryBSD is a major PITA to set up
* Instant Workstation for FreeBSD is unreliable (on legacy hardware)

# Btrfs

* [Cheatsheet](https://blog.programster.org/btrfs-cheatsheet)
* [Maximum number of snapshots per subvolume](https://btrfs.wiki.kernel.org/index.php/Gotchas#Having_many_subvolumes_can_be_very_slow) (12)

## Creation

Use default values

## fstab

Tab separated:

`UUID=Insert_UUID_Here   /path/to/Btrfs/filessystem  btrfs   defaults,autodefrag 0   0`

## Scheduled scrubs

Should be performed monthly. Put the following in the [root crontab](https://github.com/jdrch/Hardware/wiki/Useful-Links#how-to-edit-the-root-crontab-in-debian):

`@monthly btrfs scrub start /path/to/Btrfs/filessystem`

# Bufferbloat

[*A priori* avoidance of Bufferbloat (buffering-induced latency spikes) in wireless routers and access points](https://www.reddit.com/r/HomeNetworking/comments/g4upyw/how_to_determine_if_a_wireless_router_or_access/)

# `chkrootkit`

[`INFECTED: Possible Malicious Linux.Xor.DDoS installed` false positive occurs whenever there is an executable in /tmp](https://www.linuxquestions.org/questions/slackware-14/possible-infection-chrootkit-reports-linux-xor-ddos-4175605450/#post5707549)

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

e.g. `cp /sdcard/Sync/Scripts/Shell/MoveFilesToSync.sh ~/.termux/tasker/MoveFilesToSync.sh`

# cron

[How to Schedule and Automate tasks in Linux using Cron Jobs](https://www.linuxtechi.com/schedule-automate-tasks-linux-cron-jobs/)

# crontab

## How to edit the root crontab in Debian

Pretty much anything that requires `sudo` needs to be put here:

`# crontab -u root -e`

# CVEs

[Search CVE List](https://cve.mitre.org/cve/search_cve_list.html)

# `dd`

[Full Metal Backup Using the dd Command](https://www.linux.com/tutorials/full-metal-backup-using-dd-command/)

# Debian

* [The Debian Administrator's Handbook](https://debian-handbook.info/browse/stable/)
* [Don't Break Debian](https://wiki.debian.org/DontBreakDebian)
* [systemd documentation index](https://wiki.debian.org/systemd/documentation)

# Dell

## BIOS updates using a USB stick

1. Follow Steps 2.1 to 2.6 [here](https://www.dell.com/support/article/us/en/19/sln143196/how-to-create-a-bootable-usb-flash-drive-using-dell-diagnostic-deployment-package-dddp?lang=en)
2. Follow these [instructions](https://www.dell.com/support/article/us/en/19/sln129956/dell-bios-updates?lang=en#Five)

# Desktop Environments

[My opinions on the major DEs](https://forums.freebsd.org/threads/desktop-environment-what-do-you-use.74506/post-455819)

# Disk Erasure

## Windows

[Eraser](http://eraser.heidi.ie/)

# Disqus

[What HTML tags are allowed within comments](https://help.disqus.com/en/articles/1717235-what-html-tags-are-allowed-within-comments)

# DNS

* [Guide: how to discover which app is making DNS lookup requests on Windows using Sysmon & Event Viewer](https://www.reddit.com/r/pihole/comments/gytfbm/guide_how_to_discover_which_app_is_making_dns/)
* [How to Flush and Reset the DNS Cache in Windows 10](https://www.technipages.com/flush-and-reset-the-dns-resolver-cache-using-ipconfig)

# `exim4`

[Instant fix for Exim4 ‘mailing to remote domains not supported’ error](https://bobcares.com/blog/exim4-mailing-to-remote-domains-not-supported/)

# Fans

[Effects of Grill Patterns on Fan Performance/Noise](https://www.pugetsystems.com/labs/articles/Effects-of-Grill-Patterns-on-Fan-Performance-Noise-107/)

# `find`

## Syntax

* [Exclude a directory or multiple directories while using find command](https://www.crybit.com/exclude-directories/): `find /PathToBeSearched -options WhatYouAreLookingForIfNecessary ! -path /PathToBeExcluded1/* /PathToBeExcluded2/*`
* To find a file with a certain name in a given path: `# find /PathToBeSearched -type -f -name filename.extension`

# Firefox

* [How To Install The Latest Firefox (Non-ESR) On Debian 10 Buster (Stable) Or Bullseye (Testing)](https://www.linuxuprising.com/2019/12/how-to-install-latest-firefox-non-esr.html?m=1)
* [Firefox uses more RAM on FreeBSD than Linux because mozjemalloc (a heavily modified version of jemalloc) hasn't been ported to FreeBSD](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=244879#c1)

# fish shell

[How to Install, Configure and Run the Fish Shell](https://www.linode.com/docs/quick-answers/linux/how-to-install-configure-and-run-fish/)

# Github

[Creating releases](https://help.github.com/en/articles/creating-releases)

# GParted

[Manual](https://gparted.org/display-doc.php?name=help-manual)

# HDDs

How to tell if an HDD is SMR: 

* Windows: `Trim` should be listed under `Features` for the HDD in CrystalDiskInfo
* Linux: `TRIM` should be listed under `Commands/features:` in the output of `# hdparm -I /dev/DiskName`

## 4Kn vs. 512e

4Kn and 512e drives have the same performance except for when they are used with 512n apps and OSes. In that case, 4Kn HDDs have no support, while 512e HDDs suffer a read-modify-write performance penalty *relative to 512n HDDs*.

In other words, a 512e HDD is a 4Kn HDD with backwards compatibility with 512n apps and OSes. 

Per an anonymous Seagate engineering source, 512e HDDs outsell 4Kn HDDs by a wide margin among datacenter and hyperscale customers.

* [4k vs. 512](https://community.spiceworks.com/topic/post/6093125) ([Further discussion](https://www.techpowerup.com/forums/threads/hdd-bytes-per-sector-types-512e-vs-512n-vs-4kn.254422/))
* [512e cannot be converted to 4Kn for most HDDs](https://github.com/Seagate/ToolBin/issues/9#issuecomment-636327217)
* [Advanced format (4K) disk compatibility update](https://docs.microsoft.com/en-us/windows/win32/w8cookbook/advanced-format--4k--disk-compatibility-update)
* [Don't Know What 4K Hard Drive Is? Look Here!](https://www.partitionwizard.com/partitionmagic/what-is-4k-hard-drive.html)
* [FastFormat Technology Helps Future-Proof Systems](https://www.seagate.com/files/www-content/product-content/enterprise-performance-savvio-fam/enterprise-performance-15k-hdd/_cross-product/_shared/doc/seagate-fast-format-white-paper-04tp699-1-1701us.pdf) - Only the Exos X14 and above support this
* [Where to find FastFormat](https://github.com/Seagate/ToolBin/issues/5)

## Seagate

* [Seagate Toolbin](https://github.com/Seagate/ToolBin)
* [SeaChest Utilities](https://www.seagate.com/support/software/seachest/)

## SMR HDDs

* [The HDD Platter Capacity Database](https://rml527.blogspot.com/)
* [On WD Red NAS Drives](https://blog.westerndigital.com/wd-red-nas-drives/)
* [WD Internal Client SMR HDDs](https://blog.westerndigital.com/wp-content/uploads/2020/04/2020_04_22_WD_SMR_SKUs_1Slide.pdf) (PDF warning)

# Homelab

[Home Lab Beginners guide – Hardware](https://haydenjames.io/home-lab-beginners-guide-hardware/)

# Illumos

## OpenIndiana

### General documentation

* [Oracle Solaris Information Library](https://docs.oracle.com/cd/E37838_01/)
* [OpenIndiana Docs](http://docs.openindiana.org/)
* [OpenIndiana Wiki](https://wiki.openindiana.org/)

### [How to get notified of things going wrong](https://docs.oracle.com/cd/E37838_01/html/E60998/fddwy.html#scrolltoc)

`# svccfg setnotify -g to-maintenance,to-offline,to-degraded mailto:MyEmailAddress@gmail.com`

### How to set up and customize Bash 

Per this [reference](https://shreevatsa.wordpress.com/2008/03/30/zshbash-startup-files-loading-order-bashrc-zshrc-etc/), interactive login shells (e.g. SSH) read from `~/.bash_profile`, while interactive non-login shells (e.g. terminal window) read from `~/.bashrc`. OpenIndiana lacks a default `~/.bash_profile`, so create that first. Assuming you want both shell types to look the same, both files should have the exact same *non-commented* content.

If your history isn't persistent across sessions, change ownership of `.bash_history` to yourself via `# chown YourUsername .bash_history`. Your history settings should follow this format (the last line should always be there):

```
export HISTSIZE=1000
export HISTFILESIZE=2000
export HISTTIMEFORMAT='%F %T '

shopt -s histappend
```

To customize your root shells, exit `/root/.bash_profile` (create it if it doesn't exist) and `/root/.bashrc` in the same manner.

Log out and login again (via SSH or locally) to force your changes to take effect and test them.

### Packages and publishers (repositories)

* [How to update all packages & system](https://wiki.openindiana.org/oi/3.+Installing+software+and+package+management)
  * Run the following:
    * `# pkgin upgrade` ([this is sufficient to keep packages from that repo updated](https://github.com/joyent/pkgsrc/issues/253))
    * `# pkgin autoremove`
    * `# pkg update -v -r`
    * Check the output of the last command to see if there's a new boot environment to boot into. If there is, reboot the machine
* [Publishers (repos) and how to set them](https://www.openindiana.org/packages/)
* [How to set up the pkgsrc repository](https://pkgsrc.joyent.com/install-on-illumos/) (This needs to be done only once. From then on `# pkgin -y update` and `# pkgin -y upgrade` will keep you on the latest package releases)
* [List of all available pkgsrc packages](https://pkgsrc.joyent.com/packages/SmartOS/trunk/x86_64/All/)
* [How to set up SFE repository](http://sfe.opencsw.org/quickrepolinks)
  * Run `# pfexec pkg set-publisher -G '*' -g http://sfe.opencsw.org/localhostoih localhostoih`

### crontab

* [Creating and Editing crontab Files](https://docs.oracle.com/cd/E37838_01/html/E60997/sysrescron-24589.html#scrolltoc)
* [Syntax of crontab File Entries](https://docs.oracle.com/cd/E37838_01/html/E60997/sysrescron-62861.html#scrolltoc)

### ZFS

#### How to determine which drives a zpool is on

`$ zpool status -v ZPoolName`

# initramfs

Recreate initramfs: `update-initramfs -u -k all`

# ISA

[The final ISA showdown: Is ARM, x86, or MIPS intrinsically more power efficient?](https://www.extremetech.com/extreme/188396-the-final-isa-showdown-is-arm-x86-or-mips-intrinsically-more-power-efficient/3) Answer: power efficiency is largely independent of ISA

# Jupyter

## How to install

### Linux

[Instructions](https://jupyter.readthedocs.io/en/latest/install.html#alternative-for-experienced-python-users-installing-jupyter-with-pip)

### BSD

#### FreeBSD

`# pkg install py37-jupyterlab py37-graphviz py37-twisted`

# KDE

* [Documentation](https://docs.kde.org/)
* How to Restart KDE Plasma Desktop without Rebooting: `plasmashell --replace`

# KeePass

[How to update plugins](https://keepass.info/help/v2/plugins.html)

# Latency

[Latency Numbers Every Programmer Should Know](https://colin-scott.github.io/personal_website/research/interactive_latency.html)
* Note: this analysis is not exhaustive. There are other considerations, [such as memory bandwidth upper and lower limits](https://github.com/jdrch/Hardware/wiki/Useful-Links#bandwidth)

# Linux

* [Basic Linux Commands](https://linuxize.com/post/basic-linux-commands/)
* Documentation parody: [You Figure It Out](https://www.youtube.com/watch?v=ZZtu6c_c3W8)
* [How to Remove (Delete) Directory in Linux](https://linuxize.com/post/remove-directory-linux/)
* [Linux Boot Process: What You Should Know](https://www.maketecheasier.com/linux-boot-process/)
* Mark all `username`'s mail as read (delete):
  * In mail, enter `delete *`, then enter `quit`

# Logical Volume Management

[Logical Volume Management Explained on Linux](https://devconnected.com/logical-volume-management-explained-on-linux/)

# LTO-8 

* [Backwards compatibility](https://www.lto.org/solutions/benefits/compatibility/)
* [Recommended models](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#internal)

# `mail`

* [How to delete mail](https://forums.freebsd.org/threads/how-to-delete-mails.4544/)
  * Enter `delete n`, where n is the number of the message. You can also specify a range, such as `1-4`
  * Hit `Enter`
  * Enter `quit` (do not enter `exit` or your changes will not be saved)
  * Hit `Enter`   
* [`/var/mail/username` can be safely deleted](https://community.spiceworks.com/topic/434032-is-it-safe-to-delete-the-files-in-var-mail-in-linux)

# Memory

## Bandwidth

[Memory Bandwidth Napkin Math](https://www.forrestthewoods.com/blog/memory-bandwidth-napkin-math/)

# Microsoft Excel

## How to batch delete Excel columns whose top cell does not contain a given string?

If given string = "GivenString":

1. Press `Alt` + `F11` keys simultaneously to open the Microsoft Visual Basic Application window
2. In the Microsoft Visual Basic Application window, click `Insert` > `Module`
3. Enter the following code into the Module window:

```
Sub DeleteSpecifcColumn()
    Dim lastCol As Long
    Dim i As Long
    Dim ws As Worksheet
    Dim strSearch As String
    
    'What worksheet should we use?
    Set ws = ActiveSheet
    'What are we looking for?
    strSearch = "GivenString"
    
    Application.ScreenUpdating = False
    
    With ws
        'How many columns are there?
        lastCol = .Cells(1, .Columns.Count).End(xlToLeft).Column
        
        'Cycle right to left since we're deleting stuff
        For i = lastCol To 1 Step -1
            If InStr(1, .Cells(1, i).Value, strSearch) > 0 Then
                'Keep it, do nothing
            Else
                .Cells(1, i).EntireColumn.Delete
            End If
        Next i
    End With
    
    Application.ScreenUpdating = True
End Sub
```

4. Press the `F5` key to run the code 

Sources:

* https://www.extendoffice.com/documents/excel/3086-excel-delete-columns-based-on-header.html
* https://www.reddit.com/r/excel/comments/g63767/how_do_i_batch_delete_excel_columns_whose_top/fo71e1m/

# Microsoft Windows 

* [How to perform a clean boot in Windows](https://support.microsoft.com/en-us/help/929135/how-to-perform-a-clean-bot-in-windows)
* [Release channels](https://www.reddit.com/r/sysadmin/comments/e8k8jt/the_release_ring_sku_combo_completely_specify_an/fadyfq3/)

## Admin Center

* [How to manage Windows Server 2019 like a boss](https://techcommunity.microsoft.com/t5/itops-talk-blog/how-to-manage-windows-server-2019-like-a-boss/ba-p/1190784)
* [Windows Admin Center Overview](https://docs.microsoft.com/en-us/windows-server/manage/windows-admin-center/overview)

## Maintenance

How to keep your Windows installation healthy over the years without ever having to reinstall

### Do

* Ensure the latest *stable* BIOS and driver releases are installed. You can subscribe to email or RSS notifications from many OEMs
* Install updates as soon as they are offered for your PC
* Ensure the latest application releases are installed
* Be patient

### Don't

* Run unsupported configurations
* Edit the Windows registry directly unless it's for a mission critical feature
* Enable optional features (under `Turn Windows Features On or Off`) unless they are mission critical
* Install beta drivers unless they are mission critical or they address a mission critical bug
* Use Windows customizers
* Force updates on machines for whom the update hasn't been offered via Microsoft Update
* Delete your recovery partition
* Multiboot. Aside from Boot Camp, Windows is neither developed nor tested for this
* Be impatient, such as turning off your computer during an update unless it's stalled for literally 24 hours

## Microsoft Update

[Windows 10: How long will your next feature update take to install?](https://www.zdnet.com/article/windows-10-how-long-will-your-next-feature-update-take-to-install/) Answer: 7 minutes

## [[Pro for Workstations] and Enterprise] vs. Pro performance

[The Windows and Multithreading Problem (A Must Read)](https://www.anandtech.com/show/15483/amd-threadripper-3990x-review/3)

## [Storage](https://docs.microsoft.com/en-us/windows-server/storage/storage)

### [Storage Spaces](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/overview) ([Direct](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/storage-spaces-direct-overview))

[Storage Spaces benchmarks](https://hardforum.com/threads/storage-spaces-3x10-tb-120-gb-ssd-cache-refs.1922186/)

#### Current

* [Deploy Storage Spaces on a stand-alone server](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces)

#### Legacy

These are articles based on previous gen Windows releases. While they may not be 100% accurate with respect to current releases, they do a fairly good job of giving a general idea of how Storage Spaces behaves and functions internally.

* [Deep Dive: The Storage Pool in Storage Spaces Direct](https://techcommunity.microsoft.com/t5/storage-at-microsoft/deep-dive-the-storage-pool-in-storage-spaces-direct/ba-p/425959#)
* [Storage Spaces - Designing for Performance](https://social.technet.microsoft.com/wiki/contents/articles/15200.storage-spaces-designing-for-performance.aspx)
* [Storage Spaces Frequently Asked Questions (FAQ)](https://social.technet.microsoft.com/wiki/contents/articles/11382.storage-spaces-frequently-asked-questions-faq.aspx)
* [Virtualizing storage for scale, resiliency, and efficiency](https://docs.microsoft.com/en-us/archive/blogs/b8/virtualizing-storage-for-scale-resiliency-and-efficiency)

## Word

[How to Backup and Restore Unsaved Word Documents – Windows 10 Tips](https://wccftech.com/how-to/how-to-backup-and-recover-lost-files-in-office-on-windows-10/)

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

# Networking

[DSLReports Speed Test](http://www.dslreports.com/speedtest)

# `nnn`

[Keyboard and mouse](https://github.com/jarun/nnn#keyboard-and-mouse)

# Open Source

* [Open source licenses: What, which, and why](https://arstechnica.com/gadgets/2020/02/how-to-choose-an-open-source-license)
* [List of Open Source Initiative approved licenses](https://opensource.org/licenses/alphabetical)

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

# pfSense

* [2-4 Gb/s kernel routing performance limitation limit](https://www.reddit.com/r/HomeServer/comments/9yx7ct/lets_get_crazy_hypothetical_10_gbs_firewall/ea4vc2a/)
* [pfSense Hardware Requirements and Guidance](https://www.pfsense.org/products/#requirements)

# Phones

## Mobile

### Smart

#### Why compact smartphones are dead

See [here](https://www.reddit.com/r/Android/comments/fr4j9t/on_compact_android_phones_and_the_reason_we_arent/) and [here](https://www.reddit.com/r/Android/comments/fr4j9t/on_compact_android_phones_and_the_reason_we_arent/flvdnrc/)

# Pi-hole

* [How do I update Pi-hole?](https://discourse.pi-hole.net/t/how-do-i-update-pi-hole/249/13): `# pihole -up`
* Restart FTL: `# pihole restartdns`
* [If FTL isn't running in the web console but has high CPU usage](https://discourse.pi-hole.net/t/pihole-ftl-using-all-my-cpu-and-breaks-all-internet-connectivity/15672/6?u=jdrch):
  * `# service pihole-FTL stop`
  * `# mv /etc/pihole/pihole-FTL.db /etc/pihole/pihole-FTL.db.old`
  * `# service pihole-FTL start`

# `pip` for Python 3

## Installation

* [Debian 10](https://linux4one.com/how-to-install-pip-on-debian-10/)
* [Ubuntu 19.04](https://www.serverlab.ca/scripting-programming/install-python-pip-on-ubuntu-19-04/)

## Updating

Run:

`pip3 install -U pip`

# Postfix

[Ubuntu documentation](https://help.ubuntu.com/lts/serverguide/postfix.html)

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

# Raspberry Pi

[Which logs to check](https://raspberrypi.stackexchange.com/a/38005/97063) in case of crashes and other problems:
* `/var/log/messages`
* `/var/log/kern.log`

# Raspbian

[How to enable X11 forwarding for GUI apps launched with `sudo`](https://www.raspberrypi.org/forums/viewtopic.php?p=1623628#p1623628)

# Reddit

[Markdown syntax](https://www.reddit.com/wiki/markdown)

# ReFS

[ReFS integrity streams](https://docs.microsoft.com/en-us/windows-server/storage/refs/integrity-streams)

# Resilio Sync

## Android

[Sync interface on Android](https://help.resilio.com/hc/en-us/articles/213500383-Sync-interface-on-Android-)

## Linux

[How to determine which config file Resilio Sync is using and allow web UI access from other machines](https://forum.resilio.com/topic/72205-solved-ubuntu-2004-changing-listen-1270018888-to-listen-00008888-in-etcresilio-syncconfigjson-has-no-effect-on-allowing-other-machines-to-access-web-ui/)

# `restic`

* [Including and excluding files](https://restic.readthedocs.io/en/latest/040_backup.html#including-and-excluding-files)
* [Scripting](https://restic.readthedocs.io/en/latest/075_scripting.html)

# Routers

[SmallNetBuilder Router Charts](https://www.smallnetbuilder.com/tools/charts/router/view)

* [WAN to LAN Throughput - TCP](https://www.smallnetbuilder.com/tools/charts/router/bar/179-wan-to-lan-tcp/35)

# `rsync`

[How to fix the `rsync: set_acl: sys_acl_set_file(var/log/journal, ACL_TYPE_ACCESS): Operation not supported (95)` error](https://github.com/bit-team/backintime/issues/1096#issuecomment-647148330)

# S.M.A.R.T.

[ATA S.M.A.R.T. attributes](https://en.wikipedia.org/wiki/S.M.A.R.T.#ATA_S.M.A.R.T._attributes)

# Scripting (Linux)

* [How to make a script executable](https://stackoverflow.com/a/43530252/3754100): at script location, run `chmod +x <script-file-name-including-extension>`
* How to execute script: `$ ./script.sh` or `# ./script.sh`
* [How to chain commands using booleans](https://unix.stackexchange.com/questions/37069/what-is-the-difference-between-and-when-chaining-commands)
* [Place `set -u` just below the shebang of each script](https://towardsdatascience.com/this-will-make-you-a-command-line-ninja-93a51cdb16b1) (or at the top of the script if there's no shebang)
* [Try It Online](https://tio.run/#) - Test code snippets with inputs and arguments online for many languages

# smartmontools

https://www.smartmontools.org/wiki/TocDoc

# Snapper

* [`snapper` man page](http://snapper.io/manpages/snapper.html)
* [`snapper-configs` man page](http://snapper.io/manpages/snapper-configs.html)
* [ArchWiki `snapper` documentation](https://wiki.archlinux.org/index.php/Snapper)

# SSDs

* [A Study of SSD Reliability in Large Scale Enterprise Storage Deployments](https://www.usenix.org/system/files/fast20-maneas.pdf)
* [The SSD Endurance Experiment: They’re all dead](https://techreport.com/review/27909/the-ssd-endurance-experiment-theyre-all-dead/)
* [Some Observations on SSD Bit Rot](https://www.dropbox.com/sh/30hr2cd0rsu17a8/AACsr0shX7IiHjk9Ze4m8QkMa?dl=0)

# Structured Cabling

[When you need plenum cable](https://www.reddit.com/r/homelab/comments/ejkrrq/using_solid_core_cat6_cable_with_ip_security/fczrxbs/)

# `sudo`

[How to run multiple `sudo` commands on the same line](https://askubuntu.com/a/634626): `sudo some-command && sudo some-other-command` or `sudo sh -c "some-command && some-other-command"`


# Synology

[RAID Calculator](https://www.synology.com/en-us/support/RAID_calculator)

# systemd

* [How to create a new systemd service](https://www.redhat.com/sysadmin/replacing-rclocal-systemd)
* [vs. init](https://retrocomputing.stackexchange.com/a/14163/16563)

# Telegram

## Ubuntu

### [If the Telegram launch window has an error message only that says `FATAL: Could not open `~/.local/share/TelegramDesktop/log_startXX.txt' for writing log!`](https://github.com/telegramdesktop/tdesktop/issues/7481#issuecomment-605695563)

* Close the desktop app window
* Delete `~/.local/share/TelegramDesktop/`
* Launch the desktop app again

# Termux

To remove orphaned packages, use `apt autoremove`

# tsch

* [Add a splash of color to your command line environment](https://blogs.aalto.fi/marijn/2016/07/05/add-a-splash-of-color-to-your-command-line-environment/)
* [Coloring the tcsh prompt](https://www.cs.umd.edu/~srhuang/teaching/code_snippets/prompt_color.tcsh.html)
  * Comment out the 2nd prompt option  
  * To color the root crontab, make the 1st prompt option `set prompt="${green}%N${blue}@%m ${white}%~ ${green}%%${end} "` & place the file in `/root/.cshrc`
* [Customizing your shell prompt](http://www.nparikh.org/unix/prompt.php)
* [Special shell variables](https://nature.berkeley.edu/~casterln/tcsh/Special_shell_variables.html)

# TPM

[TPM 1.2, 2.0 and fTPM (firmware-based TPM) Information](http://aps2.toshiba-tro.de/kb0/TSB8B03XO0000R01.htm)

# Ubiquiti

## UniFi

### Controller

* [Transition from MongoDB](https://community.ui.com/user/di3/f30234be-4be5-45e5-abf9-a4c2320f7080) in version 5.13.x
* [EOL Definitions](https://community.ui.com/questions/Announcement-EOL-for-some-UniFi-AP-models/65487283-ce9d-49f4-85b9-b6aa54659ef7)

### Cloud Key

[Cloud Keys are easily corrupted by power failures](https://www.reddit.com/r/Ubiquiti/comments/f2wg2f/devices_keep_getting_lost/fhfn31p/)

# Ubuntu

* [How to Easily Add Users to Groups in Ubuntu](https://www.maketecheasier.com/add-remove-user-to-groups-in-ubuntu/) (See Section 2)
* [How to Upgrade SSD](https://github.com/jdrch/Hardware/issues/127#issuecomment-646820009)
* [Where the trash folder is located](https://askubuntu.com/a/102106/932418)

# `unattended-upgrades`

[GitHub](https://github.com/mvo5/unattended-upgrades)

# UNIX

[What UNIX Cost Us](https://www.youtube.com/watch?v=9-IWMbJXoLM) - A talk about how "the UNIX way" makes a lot of stuff much more difficult than it needs to be

# unRAID

[Calculator](http://unraid.category5.tv/)

# Veeam

[October 2019 Gartner Magic Quadrant](https://www.acronis.com/en-us/blog/posts/acronis-earns-its-spot-gartner-2019-magic-quadrant-enterprise-datacenter-backup-and-recovery)

## Agent for

### Linux FREE

* [System Requirements](https://helpcenter.veeam.com/docs/agentforlinux/userguide/system_requirements.html?ver=30)
* [User Guide](https://helpcenter.veeam.com/docs/agentforlinux/userguide/overview.html?ver=30)

### Windows FREE

[User Guide](https://helpcenter.veeam.com/docs/agentforwindows/userguide/overview.html?ver=30)

## Backup & Replication

[User Guide](https://helpcenter.veeam.com/docs/backup/vsphere/overview.html?ver=100)

# `vi`

[vi Editor in UNIX](https://www.geeksforgeeks.org/vi-editor-unix/)

# `vifm`

[Cheatsheet](https://vifm.info/cheatsheets.shtml)

# `vim`

[How to enable syntax highlighting](https://linuxhint.com/best_vim_color_schemes/)
* Press `Esc`
* Type `:syntax on`
* Press `Enter`

# Volume Shadow Copy

* [How to set it up](http://itsimple.info/?p=258)
  * Author made a mistake in the screenshots; [here's the correction](http://itsimple.info/?p=258#comment-912)
* [Shadow Explorer (shadow copies browsing tool)](https://www.shadowexplorer.com/downloads.html)

# Wi-Fi

* [Advanced Intel® Wireless Adapter Settings](https://www.intel.com/content/www/us/en/support/articles/000005585/network-and-i-o/wireless-networking.html)
* [Official IEEE Working Group Project Timelines](http://www.ieee802.org/11/Reports/802.11_Timelines.htm)
   * See the 802.11ax line for when the standard is likely to be ratified. It isn't as of yet
* [Wi-Fi 4/5/6 (802.11 n/ac/ad/ax)](https://www.duckware.com/tech/wifi-in-the-us.html)
* [WiFi Alliance Product Finder](https://www.wi-fi.org/product-finder)
* [What's Missing From Your Wi-Fi 6 Router? OFDMA](https://www.smallnetbuilder.com/wireless/wireless-features/33221-what-s-missing-from-your-wi-fi-6-router-ofdma)
* [What’s the Difference Between 802.11ac Wave 1 and Wave 2? [FAQ’s]](https://www.securedgenetworks.com/blog/whats-the-difference-between-802.11ac-wave-1-and-wave-2-faqs)
* [Why mesh networking is bad (example)](https://www.reddit.com/r/HomeNetworking/comments/h9igbh/will_a_mesh_network_do_its_job_if_it_can_only_use/fv4vdx6/)

## Access Point Placement

[The Ars Technica semi-scientific guide to Wi-Fi Access Point placement](https://arstechnica.com/gadgets/2020/02/the-ars-technica-semi-scientific-guide-to-wi-fi-access-point-placement/)

The above article also explains that mesh wireless systems underperform under heavy network load (one of the problems they are marketed as solving.) FTA:

>  Under heavy network load, cheap wired access points like Ubiquiti UAP-AC-Lites or TP-Link EAP-225v3s absolutely smoke even the best mesh kits, if the mesh kits are limited to Wi-Fi backhaul only.

## DFS

[SmallNetBuilder's Wi-Fi Dynamic Frequency Selection (DFS) FAQ](https://www.smallnetbuilder.com/basics/wireless-basics/33082-smallnetbuilder-s-wi-fi-dynamic-frequency-selection-dfs-faq)

## Performance

[Deriving max theoretical Wi-Fi data rates from (near-)1st principles](https://www.reddit.com/r/hardware/comments/fvthqj/deriving_max_theoretical_wifi_data_rates_from/)

## Troubleshooting

* [Access Point Placement](https://github.com/jdrch/Hardware/wiki/Useful-Links#access-point-placement)
* [Troubleshooting 'slow' Wi-Fi](https://www.duckware.com/tech/wifi-in-the-us.html#troubleshooting)

# [The XY Problem](http://xyproblem.info/)

# Zabbix

[Documentation](https://www.zabbix.com/documentation/current/start)

# ZFS 

* [Feature Matrix](https://zgrep.org/zfs.html)
* [Latest OpenZFS development status and relationship among projects](https://drive.google.com/file/d/197jS8_MWtfdW2LyvIFnH58uUasHuNszz/view)
* [Linus Torvalds recommends against ZFS (on Linux)](https://www.realworldtech.com/forum/?threadid=189711&curpostid=189841)
* [Performance, Part 1](https://www.ixsystems.com/blog/zfs-pool-performance-1/)
* [Performance, Part 2](https://www.ixsystems.com/blog/zfs-pool-performance-2/)
* [Quickstart (See Steps 3 to 6)](https://github.com/jdrch/Hardware/wiki/How-to-Set-Up-Regular,-Recurring,-Incremental,-Online-Filesystem-Backups-using-Restic)
* [RAIDZ*x* vs. mirroring resilience to *F* drive destruction](https://github.com/jdrch/Hardware/wiki/How-to-Calculate-the-Odds-of-Physical-Attack-Data-Loss-for-a-ZFS-Array)
* [When To (and Not To) Use RAID-Z](https://blogs.oracle.com/roch/when-to-and-not-to-use-raid-z)
* [ZFS 101—Understanding ZFS storage and performance](https://arstechnica.com/information-technology/2020/05/zfs-101-understanding-zfs-storage-and-performance/)
* [ZFS versus RAID: Eight Ironwolf disks, two filesystems, one winner](https://arstechnica.com/gadgets/2020/05/zfs-versus-raid-eight-ironwolf-disks-two-filesystems-one-winner/)

## Deduplication

[How to check whether a zpool would benefit from deduplication](https://docs.oracle.com/cd/E37838_01/html/E61017/gazss.html#SVZFSgjhav):

* `# zdb -S zpoolName`
* Check the value of the `dedup` output. Do not enable deduplication if `dedup` ≤ 2

# `zfsnap`

* [Homepage](https://www.zfsnap.org/)
* [Github](https://github.com/zfsnap/zfsnap.org)

# zrep

* [Homepage](http://www.bolthole.com/solaris/zrep/)
* [Github](https://github.com/bolthole/zrep)