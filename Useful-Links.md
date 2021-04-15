# WARNING: The links on this page are not necessarily exhaustive with respect to each heading/topic

# AMOLED

[No, “AMOLED Black” Does NOT Save More Battery Than Dark Gray](https://www.xda-developers.com/amoled-black-vs-gray-dark-mode/)

# Android

* [Cell Phone Brand Loyalty Survey 2021](https://www.sellcell.com/blog/cell-phone-brand-loyalty-2021/)
* [OEM support windows](https://www.reddit.com/r/Android/comments/gd35u6/are_we_and_all_the_tech_reviewers_counting/fpg32oe/)
* [Samsung security updates](https://security.samsungmobile.com/workScope.smsb)
* [Samsung updates Galaxy Tab S2 5.3 years after release](https://www.verizon.com/support/samsung-galaxy-tab-s2-refresh-update/)

## Developer Options

### Minimum Width

#### [Convert dp units to pixel units](https://developer.android.com/training/multiscreen/screendensities.html#dips-pels)

`px = dp(dpi/160)`

`dp = 160px/dpi`

* Use [DisplayInfo](https://play.google.com/store/apps/details?id=it.gerdavax.displayinfo) to find `dpi`
* `px` is display horizontal resolution

## Kernel

[State of Android on Mainline Kernels](https://linuxplumbersconf.org/event/7/contributions/785/attachments/532/946/State_of_Android_on_Mainline_Kernels__LPC.pdf)

### Updates

* [Android devices do NOT receive kernel version updates (see Paragraph 3)](https://arstechnica.com/gadgets/2019/11/google-outlines-plans-for-mainline-linux-kernel-support-in-android/)
* [Generic bootable kernels are coming](https://android-developers.googleblog.com/2020/07/accelerating-android-updates.html)
* [How Android updates work + how Projects Treble & Mainline fit into that](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/fxgen61/)

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

[Extreme Thermal Expansion Modeling in ANSYS Mechanical (Workbench)](https://www.simutechgroup.com/tips-and-tricks/fea-articles/139-extreme-thermal-expansion-modeling-in-ansys-mechanical)

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

* [Intro to ANSYS ACT for Mechanical](https://www.robsiegwart.com/blog/posts/intro_to_ansys_act_for_mechanical/)
* [Get Cracking with ANSYS Workbench 19.2](https://www.digitalengineering247.com/article/get-cracking-with-ansys-workbench-19.2/)

# APIs

[How to Use APIs (explained from scratch)](https://www.secjuice.com/how-to-use-apis/)

# `apt`

* [Fixing “The following packages have been kept back” Error While Updating Ubuntu and Debian-based Linux Distributions](https://itsfoss.com/following-packages-have-been-kept-back/)
* [How to clean up sources](https://askubuntu.com/a/762815/932418)
* How to find a package's installed dependencies: `# apt-cache rdepends --installed PackageName`. For soft dependencies (which may or may not be already installed) use `# apt show PackageName`

# Aquantia

## Drivers

[Marvell acquired Aquantia in late 2019](https://www.marvell.com/company/newsroom/marvell-completes-acquisition-of-aquantia.html), and so drivers are now found at the Marvell website. Unfortunately, they haven't made it easy to find support or drivers for legacy Aquantia products. To do so:

1. Find your Aquantia NIC part number
2. Go [here](https://www.marvell.com/support/downloads.html#) and filter by your OS and the part number from 1) above

You should find the driver download there. From what I've seen in various forum threads, the direct from the OEM driver update typically fixes link rate/stability issues.

# ARM

[How to ensure your board can boot generic kernels](https://marcin.juszkiewicz.com.pl/2021/01/20/standards-are-boring/)

# Artifical Gravity

* [SpinCalc](https://www.artificial-gravity.com/sw/SpinCalc/)
* [Space Calc](https://space.geometrian.com/calcs/artificial-gravity.php)
* [Targeting myostatin/activin A protects against skeletal muscle and bone loss during spaceflight](https://www.pnas.org/content/early/2020/09/01/2014716117)

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

# BIOS

[SOLUTION: Switch Windows 10 from RAID/IDE to AHCI operation](http://triplescomputers.com/blog/uncategorized/solution-switch-windows-10-from-raidide-to-ahci-operation/). Not that you will also have to [switch to AHCI in the BIOS](https://www.dell.com/community/XPS-Desktops/XPS-8500-boot-32GB-SSD-to-1TB-SSD-procedure/m-p/7687181/highlight/true#M53590).

# Brother

## [MFC-L3770CDW](https://www.brother-usa.com/products/mfcl3770cdw)

* [Support](https://www.brother-usa.com/support/mfcl3770cdw)
  * [Downloads (Windows 10 64-bit)](https://support.brother.com/g/b/downloadlist.aspx?c=us&lang=en&prod=mfcl3770cdw_us_eu_as&os=10013)
  * [Manuals](https://support.brother.com/g/b/manualtop.aspx?c=us&lang=en&prod=mfcl3770cdw_us_eu_as)
    * [Online User's Guide](https://support.brother.com/g/s/id/htmldoc/mfc/cv_hll3290cdw/use/manual/index.html)


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
  1. At the [main page](https://pkg-status.freebsd.org/), click the filter icon to the left of `Package Builds`
  2. Type the concatenation of the FreeBSD version and platform you're interested in, e.g. `121amd64`, into the search box
  3. Click the number in the `Build` column corresponding to the `Ports` column `pkg` repo of interest, where `default` = `latest` and `quarterly` = `quarterly`
  4. If looking for failed or skipped packages, check those headings in the page that follows
  5. If the desired package isn't there, click `previous build` and repeat iv)
* [How to switch packages from `quarterly` to `latest`](https://www.reddit.com/r/freebsd/comments/fg7598/pkg_removes_firefox_on_update_help_freebsd/fk6s2mo/)
* [Instant Workstation](https://euroquis.nl/freebsd/2020/09/17/instant-workstation.html): A [script](https://github.com/adriaandegroot/FreeBSDTools/blob/main/bin/instant-workstation) that automagically sets up KDE on a FreeBSD installation
* [Quarterly and Latest Ports Branches](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/pkgng-intro.html) (See Section 4.4.2)
* [Shells](https://www.freebsd.org/doc/handbook/shells.html)
* [Technical reasons to choose FreeBSD over GNU/Linux](https://unixsheikh.com/articles/technical-reasons-to-choose-freebsd-over-linux.html)

### How to enable `sudo` for a user

Append `username ALL=(ALL) ALL` to `/etc/sudoers` or `/usr/local/etc/sudoers`

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

### KDE

#### [How to fix keyboard keys triggering the wrong things](https://www.reddit.com/r/freebsd/comments/fjfpa5/freebsd_121releasep2_dell_xd31_usb_multimedia/fknl59g/) (such as `End` raising the Application Menu)

* Add `export XKB_DEFAULT_RULES=evdev` to `~/.xprofile`. If the file does not exist, create it first and then add the line
* Reboot

### Ports

* [FreshPorts](https://www.freshports.org/)
* [FreeBSD Ports Categories Listed By Groups](https://www.freebsd.org/ports/categories-grouped.html) (searchable)

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

## FuryBSD

Note: FuryBSD was discontinued in Q3 2020. Because FuryBSD is just an installation image that includes an integrated DE with the FreeBSD base install, it's really just FreeBSD once the installation is complete. This means you can still use it to get to the latest FreeBSD release by installing [the latest image](https://sourceforge.net/projects/furybsd/files/12.1-2020Q3-KDE/) and then updating the OS in-place.

* [Installation](https://github.com/furybsd/furybsd-handbook/wiki/Installing-FuryBSD)
* [Live USB creation](https://github.com/furybsd/furybsd-livecd/wiki)

## Why I might no longer run BSD

TL,DR: it's too much trouble.

* I need a DE. This eliminates NetBSD and Dragonfly BSD
* I need native ZFS support. This eliminates OpenBSD
* I need proper rc.d support. This eliminates GhostBSD, which uses OpenRC
  * I used GhostBSD for around 2 months, but eventually dropped it due to limited features (MATE is about as useless a DE as you can imagine) and stuff just not working reliably. The latter included, but it not limited to
    * I couldn't get 3rd party services to start reliably at boot. I wound up having to use an `@reboot` crontab entry as a workaround, but of course that doesn't help if the service crashes
    * I couldn't get NFS shares to mount reliably at boot, even with an `@reboot` crontab entry, or to mount at all otherwise at times
* ~~FuryBSD is a major PITA to set up~~
* Instant Workstation for FreeBSD is unreliable (on legacy hardware)

# Btrfs

* [Cheatsheet](https://blog.programster.org/btrfs-cheatsheet)
* [Scrubbing and Balancing Maintenance Guidelines](https://www.spinics.net/lists/linux-btrfs/msg90536.html)
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

# Cable Internet Service

[Effect of poor cabling on a service loop](https://www.reddit.com/r/HomeNetworking/comments/ig0kxr/would_like_casual_advice_regarding_comcast_cable/g2u759c/)

# Car Sales Numbers

* [CarSalesBase](https://carsalesbase.com/)
* [GoodCarBadCar](https://www.goodcarbadcar.net/)

# `chkrootkit`

[`INFECTED: Possible Malicious Linux.Xor.DDoS installed` false positive occurs whenever there is an executable in /tmp](https://www.linuxquestions.org/questions/slackware-14/possible-infection-chrootkit-reports-linux-xor-ddos-4175605450/#post5707549)

# CGNAT

[How to check if the ISP uses Carrier-grade NAT (CGN)](https://www.remoterig.com/wp/?page_id=3494)

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
2. Download the BIOS file into the top level of the bootable USB
3. Follow these [instructions](https://www.dell.com/support/article/us/en/19/sln129956/dell-bios-updates?lang=en#Five)

# Desktop Environments

* [My opinions on the major DEs](https://forums.freebsd.org/threads/desktop-environment-what-do-you-use.74506/post-455819)
* [Memory usage comparison](https://www.ubuntubuzz.com/2020/07/memory-comparison-ubuntu-2004-family.html)

# Disk Erasure

## Windows

[Eraser](http://eraser.heidi.ie/)

# Disqus

[What HTML tags are allowed within comments](https://help.disqus.com/en/articles/1717235-what-html-tags-are-allowed-within-comments)

# DNA

[When Bad DNA Tests Lead to False Convictions](https://gizmodo.com/when-bad-dna-tests-lead-to-false-convictions-1797915655)

# DNS

* [Guide: how to discover which app is making DNS lookup requests on Windows using Sysmon & Event Viewer](https://www.reddit.com/r/pihole/comments/gytfbm/guide_how_to_discover_which_app_is_making_dns/)
* [How to Flush and Reset the DNS Cache in Windows 10](https://www.technipages.com/flush-and-reset-the-dns-resolver-cache-using-ipconfig)

# Dolby 

## Atmos

[5.1 Virtual speaker setup](https://www.dolby.com/about/support/guide/speaker-setup-guides/5.1-virtual-speakers-setup-guide/)

# Electrical Engineering

[A Plug-and-Play Microgrid for Rooftop Solar](https://spectrum.ieee.org/green-tech/solar/a-plugandplay-microgrid-for-rooftop-solar) - An excellent description of the power quality/power factor issues inherent in renewable energy sources, and how to overcome them

# Ethernet

## How to connect pre-wired Ethernet ports

Situation: you find out your home has been prewired for Ethernet. How do you use the ports to connect your devices?

1. Each Ethernet wall port should be fed by an Ethernet cable run from the port to a central location. That central location, which we'll call a junction box, is usually in the basement, a closet, the attic, or in the garage. **Locate the patch panel before you move in and place items that might make it harder to find**
2. Determine which Category (5, 5E, 6, 6A, 7, 7A, or 8) of cable you have. It is usually printed along the length of the cables. This will determine your network's top (theoretical) speed. Cat 5 is good for 100 Mb/s, 5E & above for 1 Gb/s, Cat 6A & above for 10 Gb/s, and Cat 8 for 20 Gb/s
3. If the cables aren not yet terminated (read: if they do not end in a male or female Ethernet jack), terminate them with a [patch panel](https://community.fs.com/blog/what-is-a-patch-panel-and-why-use-it.html). You can either DIY this or have a structured cabling contractor do it for you
4. Use [cable testing tools](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#testers) to match the cables at the patch panel with other terminations in the home
5. Connect your router (or switch downstream of your router) to the patch panel ports that have matches in the previous step

If there is no junction box in step 1, then detach the wall plates from the wall and ensure they're being fed by Ethernet cable. If they aren't, then consider [these options](https://github.com/jdrch/Hardware/wiki/Useful-Links#improvement). If they are, then your cabling may be point-to-point. Locate all cable terminations in the home and test them round-robin with the testing tools from Step 4, making notes as you go along to match ports with each other. A network connection can be established between any 2 matching port pairs. If you're unable to find any matching pairs, then your cables are *somewhere* that's not a junction box. Scour all closets, attics, cupboards, basements, sheds, and garages. Use the tracing probe to help. If you still can't find where your cables are going, contact a structured cabling contractor to see what's going on.

## Cables

[Troubleshooting speed differences](https://www.reddit.com/r/HomeNetworking/comments/jxr6i4/10g_15_year_old_cat5e_is_faster_than_cat6/gcylfn9/?utm_source=reddit&utm_medium=web2x&context=3)

# Evernote

[Move from Evernote to OneNote](https://discussion.evernote.com/forums/topic/123650-move-from-evernote-to-onenote/) - The official Microsoft guide for this omits a lot of important details. This will fill you in. 

# `exim4`

[Instant fix for Exim4 ‘mailing to remote domains not supported’ error](https://bobcares.com/blog/exim4-mailing-to-remote-domains-not-supported/)

# Fans

[Effects of Grill Patterns on Fan Performance/Noise](https://www.pugetsystems.com/labs/articles/Effects-of-Grill-Patterns-on-Fan-Performance-Noise-107/)

# `find`

## Syntax

* [Exclude a directory or multiple directories while using find command](https://www.crybit.com/exclude-directories/): `find /PathToBeSearched -options WhatYouAreLookingForIfNecessary ! -path /PathToBeExcluded1/* /PathToBeExcluded2/*`
* To find a file with a certain name in a given path: `# find /PathToBeSearched -type -f -name filename.extension`

# Finite Element Analysis (FEA)

* [Accuracy and Checking in FEA, Part 1](https://www.digitalengineering247.com/article/accuracy-and-checking-in-fea-part-1)
* [Accuracy and Checking in FEA, Part 2](https://www.digitalengineering247.com/article/accuracy-and-checking-in-fea-part-2)
* [Free-Floating FEA Models](https://www.digitalengineering247.com/article/free-floating-fea-models)
* [The Forbidden Simulation Riff](https://read.nxtbook.com/peerless_media/digital_engineering/march_2020/the_forbidden_simulation_riff.html) (Or how to set up fixed boundary conditions properly)

# Firefox

* [Firefox uses more RAM on FreeBSD than Linux because mozjemalloc (a heavily modified version of jemalloc) hasn't been ported to FreeBSD](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=244879#c1)
* [How To Install The Latest Firefox (Non-ESR) On Debian 10 Buster (Stable) Or Bullseye (Testing)](https://www.linuxuprising.com/2019/12/how-to-install-latest-firefox-non-esr.html?m=1)
* [Lastest Nightly builds](http://ftp.mozilla.org/pub/mozilla.org/firefox/nightly/latest-mozilla-central/)

# fish shell

[How to Install, Configure and Run the Fish Shell](https://www.linode.com/docs/quick-answers/linux/how-to-install-configure-and-run-fish/)

# Fuchsia

[Playing Around With The Fuchsia Operating System](https://blog.quarkslab.com/playing-around-with-the-fuchsia-operating-system.html)

# Github

[Creating releases](https://help.github.com/en/articles/creating-releases)

# Google Calendar

[How to sync ALL shared Google Calendars to Windows 10 Calendar app](https://calendar.google.com/calendar/syncselect)

# Google Messages

[Messages Community](https://support.google.com/messages/community)

# GParted

[Manual](https://gparted.org/display-doc.php?name=help-manual)

# HDDs

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

## How to tell if an HDD is SMR 

* Windows: `Trim` should be listed under `Features` for the HDD in CrystalDiskInfo
* Linux: `TRIM` should be listed under `Commands/features:` in the output of `# hdparm -I /dev/DiskName`

## Power consumption

How to calculate HDD max power consumption (you will need the HDD user manual to find the needed input data): 

### Method 1

This is the easiest method, but it is conservative and therefore may unrealistically overestimate power usage by adding the max powers for each voltage under different conditions that are unlikely to occur simultanously:

1. Find the input voltages (usually 5 VDC and 12 VDC)
2. Multiply each input voltage by its maximum corresponding current value
3. Sum all the results of 2) above. 

[Example](https://www.seagate.com/files/www-content/product-content/enterprise-hdd-fam/exos-x18/_shared/en-us/docs/100865854a.pdf) (p. 12, Table 6):

`Max Power = (5 VDC *1.22 A) + (12 VDC *2.88 A) = 40.66 W`

### Method 2

1. Same as above
2. Multiple each input voltage by each listed corresponding current
3. Sum the results of the above *per condition*. Using the previous example, sum the 5 VDC and 12 VDC powers (voltage x current) for each line in Table 6 separately
4. Pick the highest result from Step 3

## Recovery

1. If the HDD is in an enclosure, shuck it and connect it to a SATA dock or (preferably) an internal SATA port. If the HDD is already internal, try it on or in a different PC.
2. If the host OS detects the HDD as newly connected in 1) above, copy all the data off it. If the OS does not detect the drive, you'll need a professional data recovery service.

## Seagate

* [Seagate Toolbin](https://github.com/Seagate/ToolBin)
* [SeaChest Utilities](https://www.seagate.com/support/software/seachest/)

## SMR HDDs

* [The HDD Platter Capacity Database](https://rml527.blogspot.com/)
* [On WD Red NAS Drives](https://blog.westerndigital.com/wd-red-nas-drives/)
* [Seagate CMR and SMR Hard Drives](https://www.seagate.com/internal-hard-drives/cmr-smr-list/)
* [WD Internal Client SMR HDDs](https://blog.westerndigital.com/wp-content/uploads/2020/04/2020_04_22_WD_SMR_SKUs_1Slide.pdf) (PDF warning)

# HDR

[VESA DisplayHDR Certified Products](https://displayhdr.org/certified-products/)

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

Per this [reference](https://shreevatsa.wordpress.com/2008/03/30/zshbash-startup-files-loading-order-bashrc-zshrc-etc/), interactive login shells (e.g. SSH) read from `~/.bash_profile`, while interactive non-login shells (e.g. terminal window) read from `~/.bashrc`. OpenIndiana lacks a default `~/.bash_profile`, so create that first using `touch .bash_profile`.

Put the following in `.bash_profile` and then save it:

```
# Point .bash_profile to .bashrc if Bash is the current shell

# If running bash
if [ -n "$BASH_VERSION" ]; then
    # Include .bashrc if it exists
    if [ -f "$HOME/.bashrc" ]; then
	. "$HOME/.bashrc"
    fi
fi
```

An example of `.bashrc` file is shown below:

```
#
# Define default prompt to <username>@<hostname>:<path><"($|#) ">
# and print '#' for user "root" and '$' for normal users.
#

# Standardized Bash prompt: https://github.com/jdrch/Hardware/issues/113
typeset +x PS1="\[\033[01;32m\]\u\[\033[01;34m\]@\h \[\033[35m\]\D{%F %T}\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ "

# Useful aliases
alias ls='ls --color=auto'
# alias dir='dir --color=auto'
# alias vdir='vdir --color=auto'

# alias grep='grep --color=auto'
# alias fgrep='fgrep --color=auto'
# alias egrep='egrep --color=auto'

alias ll='ls -l'
alias la='ls -A'
alias l='ls -CF'

# for setting history length see HISTSIZE and HISTFILESIZE in bash(1)
export HISTSIZE=1000
export HISTFILESIZE=2000
export HISTTIMEFORMAT='%F %T '

shopt -s histappend

# Tell OS where to find packages
export PATH="/usr/gnu/bin:/usr/bin:/usr/sbin:/sbin:/opt/local/sbin:/opt/local/bin:$HOME/bin:$HOME/.local/bin:/opt/local/sbin:/opt/local/bin:$PATH"

# Tell OS where to find man pages
export MANPATH=/opt/local/man:/usr/gnu/share/man:/usr/share/man:/usr/X11/share/man:$MANPATH

# Set default editor
export EDITOR=nano
```

If your history isn't persistent across sessions, change ownership of `.bash_history` to yourself via `# chown YourUsername .bash_history`. Your history settings should follow this format (the last line should always be there):

```
export HISTSIZE=1000
export HISTFILESIZE=2000
export HISTTIMEFORMAT='%F %T '

shopt -s histappend
```

To customize your root shells, repeat the same process for `/root/.bash_profile` (create it if it doesn't exist) and `/root/.bashrc`.

Log out and login again (via SSH or locally) to force your changes to take effect and test them.

### Packages and publishers (repositories)

* [Publishers (repos) and how to set them](https://www.openindiana.org/packages/)
* [How to set up SFE repository](http://sfe.opencsw.org/quickrepolinks)
  * Run `pfexec pkg set-publisher -G '*' -g https://sfe.opencsw.org/localhostoih localhostoih  #new OpenIndiana Hipster x86`
* [How to set up the pkgsrc repository](https://pkgsrc.joyent.com/install-on-illumos/) (This needs to be done only once. From then on `# pkgin -y update` and `# pkgin -y upgrade` will keep you on the latest package releases)
* [How to update all packages & system](https://wiki.openindiana.org/oi/3.+Installing+software+and+package+management)
  * Run the following:
    * `# pkgin upgrade` ([this is sufficient to keep packages from that repo updated](https://github.com/joyent/pkgsrc/issues/253))
    * `# pkgin autoremove`
    * `# pkg update -v -r`
    * Check the output of the last command to see if there's a new boot environment to boot into. If there is, reboot the machine
* [List of all available pkgsrc packages](https://pkgsrc.joyent.com/packages/SmartOS/trunk/x86_64/All/)

### crontab

* [Creating and Editing crontab Files](https://docs.oracle.com/cd/E37838_01/html/E60997/sysrescron-24589.html#scrolltoc)
* [Syntax of crontab File Entries](https://docs.oracle.com/cd/E37838_01/html/E60997/sysrescron-62861.html#scrolltoc)

### ZFS

#### How to determine which drives a zpool is on

`$ zpool status -v ZPoolName`

# initramfs

Recreate initramfs: `update-initramfs -u -k all`

# IoT

[Why Smart TVs, x86-64, Raspberry Pis, and consoles are the only IoT devices allowed in my house](https://www.reddit.com/r/HomeNetworking/comments/lz35fs/isolating_smart_devices_and_general_privacy/gq1uavv/?utm_source=reddit&utm_medium=web2x&context=3)

# ISA

* [New RISC-V CPU claims recordbreaking performance per watt](https://arstechnica.com/gadgets/2020/12/new-risc-v-cpu-claims-recordbreaking-performance-per-watt/) - RISC-V vs. ARM vs. x86, single benchmark
* [The final ISA showdown: Is ARM, x86, or MIPS intrinsically more power efficient?](https://www.extremetech.com/extreme/188396-the-final-isa-showdown-is-arm-x86-or-mips-intrinsically-more-power-efficient/3) Answer: power efficiency is largely independent of ISA

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

# KSysGuard

[Explanation of memory usage as displayed, and workaround](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=245293)

# KeePass

[How to update plugins](https://keepass.info/help/v2/plugins.html)

# Latency

* [Acceptable latency values](https://www.actiontec.com/wifihelp/wifibooster/how-to-reduce-latency-or-lag-in-gaming-2/) (<= 100 ms)
* [Latency Numbers Every Programmer Should Know](https://colin-scott.github.io/personal_website/research/interactive_latency.html)
  * Note: this analysis is not exhaustive. There are other considerations, [such as memory bandwidth upper and lower limits](https://github.com/jdrch/Hardware/wiki/Useful-Links#bandwidth)

# Lenovo

[How to fix excessive reverse DNS lookups](https://www.reddit.com/r/pihole/comments/gytfbm/guide_how_to_discover_which_app_is_making_dns/)

# Linux

* [Basic Linux Commands](https://linuxize.com/post/basic-linux-commands/)
* Documentation parody: [You Figure It Out](https://www.youtube.com/watch?v=ZZtu6c_c3W8)
* [GitStats](https://phoronix.com/misc/linux-eoy2019/authors.html)
* [How To Add/Remove A Software Repository In Linux?](https://www.explorelinux.com/how-to-add-remove-a-software-repository-in-linux)
* [How to Remove (Delete) Directory in Linux](https://linuxize.com/post/remove-directory-linux/)
* [Linux Boot Process: What You Should Know](https://www.maketecheasier.com/linux-boot-process/)
* Mark all `username`'s mail as read (delete):
  * In mail, enter `delete *`, then enter `quit`
* [The Linux Kernel, CDDL and Related Issues](https://www.softwarefreedom.org/resources/2016/linux-kernel-cddl.html)

# Logical Volume Management

[Logical Volume Management Explained on Linux](https://devconnected.com/logical-volume-management-explained-on-linux/)

# Logitech 

If the mouse wheel scroll functionality randomly stops working, disable smooth scrolling in Logitech Options

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

[Try LAMBDA: Custom functions without code](https://insider.office.com/en-us/blog/lambda-excel-custom-functions)

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

**NOTE:** Admin Center works on FQDN environments only.

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

* [Storage Spaces benchmarks](https://hardforum.com/threads/storage-spaces-3x10-tb-120-gb-ssd-cache-refs.1922186/)
* [Reddit guide](https://www.reddit.com/r/DataHoarder/comments/hp54pm/getting_started_with_refs_and_storage_spaces_on/)

#### Current

* [Deploy Storage Spaces on a stand-alone server](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces)

#### Legacy

These are articles based on previous gen Windows releases. While they may not be 100% accurate with respect to current releases, they do a fairly good job of giving a general idea of how Storage Spaces behaves and functions internally.

* [Deep Dive: The Storage Pool in Storage Spaces Direct](https://techcommunity.microsoft.com/t5/storage-at-microsoft/deep-dive-the-storage-pool-in-storage-spaces-direct/ba-p/425959#)
* [Storage Spaces - Designing for Performance](https://social.technet.microsoft.com/wiki/contents/articles/15200.storage-spaces-designing-for-performance.aspx)
* [Storage Spaces Frequently Asked Questions (FAQ)](https://social.technet.microsoft.com/wiki/contents/articles/11382.storage-spaces-frequently-asked-questions-faq.aspx)
* [Virtualizing storage for scale, resiliency, and efficiency](https://docs.microsoft.com/en-us/archive/blogs/b8/virtualizing-storage-for-scale-resiliency-and-efficiency)

#### How to create a Storage Pool using PowerShell

Use this method if you're getting weird errors creating a storage pool in Control Panel's Storage Spaces GUI.

**WARNING:** Be careful when copying and pasting PowerShell code as sometimes important characters such as dashes or quotes get removed during the operation. Why? Your guess is as good as mine.

This example assumes you'll be using all poolable drives in your storage pool.

1. Ensure the target drives are not part of a DrivePool or any similar volume spanning solution. If they are, remove them from the spanned volume or DrivePool
2. Delete any volumes on the target drives in Windows Disk Management
3. If it's not installed already, download and install the latest stable [PowerShell release](https://github.com/PowerShell/PowerShell/releases)
4. Run PowerShell as Administrator
5. Find out if your target target drives can be pooled by running `Get-PhysicalDisk` and checking the `Can Pool` column value. If it's `True`, skip to Step 8. If it's `False`:
6. Run `Reset-PhysicalDisk -FriendlyName "PhysicalDiskn"` for each drive, where `n` is the number in the `Number` column of `Get-PhysicalDisk`'s output in Step 5
7. Reboot the PC
8. Run `Get-StoragePool -IsPrimordial $true | Get-PhysicalDisk | Where-Object CanPool -eq $True`. The output should be the drives you reset in Step 6, e.g.

```
PS C:\Windows\System32> Get-StoragePool -IsPrimordial $true | Get-PhysicalDisk | Where-Object CanPool -eq $True

Number FriendlyName         SerialNumber MediaType CanPool OperationalStatus HealthStatus Usage           Size
------ ------------         ------------ --------- ------- ----------------- ------------ -----           ----
0      ST12000NM0007-2A1101 12345678     HDD       True    OK                Healthy      Auto-Select 10.91 TB
1      ST12000DM0007-2GR116 87654321     HDD       True    OK                Healthy      Auto-Select 10.91 TB
```

9. Run [`Get-StorageSubsystem`](https://docs.microsoft.com/en-us/powershell/module/storage/get-storagesubsystem?view=win10-ps), e.g.

```
PS C:\Windows\System32>  Get-StorageSubSystem

FriendlyName                     HealthStatus OperationalStatus
------------                     ------------ -----------------
StorageSubsystemFriendlyNameString Healthy      OK
```

10. Create the storage pool by running `New-StoragePool -FriendlyName YourDesiredPoolName -StorageSubsystemFriendlyName 'StorageSubsystemFriendlyNameString' -PhysicalDisks (Get-PhysicalDisk -CanPool $True)`. Alternatively, if you want to use a specified subset of the eligible disks, run a command of the form `New-StoragePool –FriendlyName YourDesiredCamelCasePoolName –StorageSubsystemFriendlyName 'StorageSubsystemFriendlyNameString' –PhysicalDisks (Get-PhysicalDisk PhysicalDiska, PhysicalDiskb, PhysicalDiskc)`, where `a`, `b`, and `c` have the same definiton as `n` in Step 6

Your storage pool should now be created, and you can create storage spaces on it using Control Panel's Storage Spaces GUI.

[Reference](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces#windows-powershell-equivalent-commands-for-creating-storage-pools) (Good luck understanding it.)

#### How to create a Storage Space using PowerShell

The following will create a single column, 2-way mirror storage space that consumes all the available space on the pool using the same parameters as above:

1. Open an elevated PowerShell prompt
2. Run `New-VirtualDisk -StoragePoolFriendlyName YourDesiredPoolName -FriendlyName YourDesiredVirtualDiskName -ResiliencySettingName Mirror -NumberOfDataCopies 2 -ProvisioningType Fixed -UseMaximumSize -NumberOfColumns 1 -Verbose`

Note that `-UseMaximumSize` cannot be invoked with `-ProvisioningType Thin` spaces, as thin spaces dynamically expand *in situ* with storage demand.

Confirm that the virtual disk has been created as specified:

```
PS C:\Windows\System32> Get-VirtualDisk

FriendlyName ResiliencySettingName FaultDomainRedundancy OperationalStatus HealthStatus     Size FootprintOnPool StorageEfficiency
------------ --------------------- --------------------- ----------------- ------------     ---- --------------- -----------------
YourDesiredVirtualDiskName  Mirror                1                     OK                Healthy      10.91 TB        21.82 TB            50.00%
```

To create a volume on the storage space, simply open Disk Manager. You'll get a prompt to initialize the new disk you created. Initialize it as GPT and then proceed to create a volume on it as you would otherwise. You then need to enable [ReFS integrity streams](https://docs.microsoft.com/en-us/windows-server/storage/refs/integrity-streams) on the volume via `Set-FileIntegrity H:\ -Enable $True`. Do not forget this step as otherwise ReFS will not have data checksumming, which is pretty much the #1 reason to use it instead of NTFS.

Reference: [Step By Step: How To Create A Two-Way Mirrored Storage Space via PowerShell? #StorageSpaces #PowerShell](https://charbelnemnom.com/2014/09/step-by-step-how-to-create-a-two-way-mirrored-storage-space-via-powershell-storagespaces-powershell/)

#### How to extend an ReFS volume

The information available on this is sparse and a bit confusing, but basically it appears you can only expand volumes by 20% at time. This just means it will take multiple expansions when you add new disks. Threads on the subject:

* https://social.technet.microsoft.com/Forums/lync/en-US/c1cbb589-cd60-4147-ad22-855a28f9bc9e/cannot-extend-refs-volume-windows-2012-r2?forum=winservergen
* https://social.technet.microsoft.com/Forums/en-US/af4db752-b336-4d4e-80bb-8c8642c94eff/extended-refs-partition-but-new-sizefree-space-doesnt-show-in-explorer?forum=winserverfiles
* https://social.technet.microsoft.com/Forums/en-US/e2fd8c79-c2a7-426f-81a7-19d15b036a10/best-practices-to-extend-refs-volume-windows-server-2012-64-bit?forum=winserver8gen

#### How to upgrade a storage pool

See [Option 2](https://www.tenforums.com/tutorials/83868-upgrade-storage-pool-storage-spaces-windows-10-a.html). I'd recommend you run this command after every semi annual Windows release, as ReFS/Storage Pool updates are delivered with Windows releases.

## Word

[How to Backup and Restore Unsaved Word Documents – Windows 10 Tips](https://wccftech.com/how-to/how-to-backup-and-recover-lost-files-in-office-on-windows-10/)

# MobaXterm

* How to fix the `Installer not responding` error:
  * Open an elevated PowerShell prompt at the installer's location
  * Run the installer `./MobaXterm_installer_Version_Branch.msi`
  * When the error message pops up again, click `Retry`
  * The installation should then proceed as normal

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

* [An Introduction to Computer Networks](http://intronetworks.cs.luc.edu/current2/html/)
* [DSLReports Speed Test](http://www.dslreports.com/speedtest)

# NFS

For v4:

## Debian Stable Server, FreeBSD RELEASE Client

### Server

`# apt install nfs-kernel-server`

#### `/etc/exports`

Needs the following line:

`/Path/To/Shared/Folder ClientIPAddressOrHostname(rw,async,no_subtree_check,no_root_squash)`

Restart the NFS server to load your changes: `# systemctl restart nfs-kernel-server`

### Client

#### Terminal

`# mount -t nfs -o nfsv4 ServerIPAddress:/PathToServerShare /LocalMountPath`

#### `/etc/fstab`

Needs the following line:

`ServerIPAddress:/PathToServerShare  /LocalMountPath                     nfs     rw,nfsv4acls    0 0`

## OpenIndiana Hipster Server, Raspberry Pi OS Stable Client

Assuming `rpool1` is pool to be shared:

### Server

#### Terminal

Run the following command:

`# zfs set sharenfs='rw=@ClientIPAddress/32,root=@ClientIPAddress/32' rpool1`

There is no need to restart anything after running that command; the OS automatically applies the settings and publishes the new share with them.

### [Client](https://www.raspberrypi.org/documentation/configuration/nfs.md)

See **Set up an NFSv4 client** heading at the above link.

`# apt install nfs-common`

#### Terminal

`# mount -t nfs -o proto=tcp,port=2049 ServerIPAddress:/ /LocalMountPath`

#### `/etc/fstab`

Needs the following line:

`ServerIPAddress:/   /mnt   nfs    auto  0  0`

# `nnn`

[Keyboard and mouse](https://github.com/jarun/nnn#keyboard-and-mouse)

# NTFS

[Copying NTFS permissions between folders](https://confidentialfiles.wordpress.com/2014/03/13/copying-ntfs-permissions-between-folders/)

# OBS Studio

[How to set up background replacement with a physical green screen and a virtual camera that can be used in other apps](https://www.reddit.com/r/streaming/comments/k9uhsu/are_there_any_virtual_camera_apps_that_explicitly/)

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

# PC Shipments

## 2021

### Q1

[PC Shipments Show Continued Strength in Q1 2021 Despite Component Shortages and Logistics Issues, According to IDC](https://www.idc.com/getdoc.jsp?containerId=prUS47601721)

# pfSense

* [2-4 Gb/s kernel routing performance limitation limit](https://www.reddit.com/r/HomeServer/comments/9yx7ct/lets_get_crazy_hypothetical_10_gbs_firewall/ea4vc2a/)
* [pfSense Hardware Requirements and Guidance](https://www.pfsense.org/products/#requirements)

# Phones

## Mobile

### Smart

#### Why compact smartphones are dead

See [here](https://www.reddit.com/r/Android/comments/fr4j9t/on_compact_android_phones_and_the_reason_we_arent/) and [here](https://www.reddit.com/r/Android/comments/fr4j9t/on_compact_android_phones_and_the_reason_we_arent/flvdnrc/)

# Physics

[dB: What is a decibel?](https://www.animations.physics.unsw.edu.au/jw/dB.htm)

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

# Power over Ethernet

* [Power over Ethernet - Everything you need to know](https://intellinetnetwork.eu/pages/power-over-ethernet)
* Cable length and material matter greatly for PoE. See this [troubleshooting example](https://www.reddit.com/r/HomeNetworking/comments/hpes0t/issue_with_ethernet_negotiation_speed/fxr8g02/)

# PowerShell

* How to run an executable
  * `./ExecutableFileName`

# Privacy

[Mozilla Privacy Buying Guide](https://foundation.mozilla.org/en/privacynotincluded/)

# PSUs

[What is PSU Efficiency and Why is it Important?](https://www.velocitymicro.com/blog/what-is-psu-efficiency-and-why-is-it-important/)

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

* [How to determine which config file Resilio Sync is using and allow web UI access from other machines](https://forum.resilio.com/topic/72205-solved-ubuntu-2004-changing-listen-1270018888-to-listen-00008888-in-etcresilio-syncconfigjson-has-no-effect-on-allowing-other-machines-to-access-web-ui/)
* [How to fix Resilio Sync launching under *both* `rslsync` and another user](https://forum.resilio.com/topic/72711-solved-ubuntu-debian-repo-installation-sync-loads-new-user-profile-after-system-reboots-from-kernel-update/?do=findComment&comment=156412)
* [How to run multiple instances under different users](https://forum.resilio.com/topic/72681-linux-server-multiple-users-with-multiple-instances/?do=findComment&comment=155947)

# `restic`

* How to unlock a repo
  * If you are getting the `Fatal: unable to create lock in backend: repository is already locked by PID` error, run `# restic -p /Path/To/Repo/Password/File -r /Path/to/Repo unlock` to unlock it
* [Including and excluding files](https://restic.readthedocs.io/en/latest/040_backup.html#including-and-excluding-files)
* [Scripting](https://restic.readthedocs.io/en/latest/075_scripting.html)

# Routers

[SmallNetBuilder Router Charts](https://www.smallnetbuilder.com/tools/charts/router/view)

* [WAN to LAN Throughput - TCP](https://www.smallnetbuilder.com/tools/charts/router/bar/179-wan-to-lan-tcp/35)

# `rpi-clone`

If you get the `already mounted or mount point busy.` error:

(Assuming the target card is `/dev/sda`

1. Create a new partitional table on the target card in GParted (this will format the target card)
2. Ensure the card isn't mounted:
   1. `$ df -l`.
   2. If the card isn't listed, proceed to next step. If it is listed, unmount it via `# umount /dev/sda`
3. Run `rpi-clone`

# `rsync`

[How to fix the `rsync: set_acl: sys_acl_set_file(var/log/journal, ACL_TYPE_ACCESS): Operation not supported (95)` error](https://github.com/bit-team/backintime/issues/1096#issuecomment-647148330)

# S.M.A.R.T.

[ATA S.M.A.R.T. attributes](https://en.wikipedia.org/wiki/S.M.A.R.T.#ATA_S.M.A.R.T._attributes)

# Sales/Shipments

[2020-09-01 - IDC - Desktop vs. Detachable Tablet vs. Notebook vs. Slate Tablet vs. Workstation](https://www.businesswire.com/news/home/20200901005988/en/IDC-Forecasts-PC-and-Tablet-Shipments-to-Grow-3.3-in-2020-Before-Resuming-Their-Long-Term-Decline-in-2021)

# Scheduled Tasks

* How to fix `Task Start Failed` & `Launch Failure` errors
  * Select the problematic task
  * Click `Properties`
  * In the `Triggers` tab, highlight the trigger
  * Click `Edit...`
  * In the `Edit Trigger` window, in the `Begin the task:` dropdown menu, select `On a schedule`
  * Select the `One time` radio button
  * In the `Advanced Settings` section, check the `Repeat task every:` box
  * In the `Repeat task every:` dropdown menu, select your preferred interval
  * In the `for a duration of:` dropdown menu, select `Indefinitely`
  * Check the `Enabled` box
  * Click `OK`
  * Click `OK`

[Reference](https://social.technet.microsoft.com/Forums/windowsserver/en-US/29a37921-3e27-4c88-b387-3dd394302298/strange-problem-in-windows-2008-task-scheduler?forum=winservergen)

Task names are both unique *and* persistent. What the latter means is that *even if you delete a task*, if you create another task with the same name it will inherit all the history (and behavior!!!) of the deleted task. 

Often, the best fix for a malfunctioning task is to completely delete it, then recreate it from scratch directly on the target machine using a different unique task name.

# Scripting (Linux)

* [How to make a script executable](https://stackoverflow.com/a/43530252/3754100): at script location, run `chmod +x <script-file-name-including-extension>`
* How to execute script: `$ ./script.sh` or `# ./script.sh`
* [How to chain commands using booleans](https://unix.stackexchange.com/questions/37069/what-is-the-difference-between-and-when-chaining-commands)
* [Place `set -u` just below the shebang of each script](https://towardsdatascience.com/this-will-make-you-a-command-line-ninja-93a51cdb16b1) (or at the top of the script if there's no shebang)
* [Try It Online](https://tio.run/#) - Test code snippets with inputs and arguments online for many languages

# Signal transmission speeds

[Velocity Factors](https://en.wikipedia.org/wiki/Velocity_factor#Typical_velocity_factors) for various media

# smartmontools

https://www.smartmontools.org/wiki/TocDoc

# Snapper

* [`snapper` man page](http://snapper.io/manpages/snapper.html)
* [`snapper-configs` man page](http://snapper.io/manpages/snapper-configs.html)
* [ArchWiki `snapper` documentation](https://wiki.archlinux.org/index.php/Snapper)

# Sony PlayStation 5

[Runs FreeBSD 12](https://www.reddit.com/r/PS5/comments/juggo1/has_anyone_done_an_nmap_scan_of_the_ps5_to/)

# Speed tests

## [DSLReports.com](http://www.dslreports.com/speedtest)

* This is the premier, most realistic internet connection diagnostic test online
* Run this test on a wired connection to your router or modem, if you can. **Tests run on wireless connections are inconclusive due to the basic physics limitations of Wi-Fi**
* If you were sent to this link from a discussion thread containing a problem you're having, **please post your results (link on the results page) back in the thread. Doing so will help users on the thread diagnose your issues. The quality of the advice you receive is directly proportional to the quality of the information you provide**

### How to fix scores

≥ A: Nothing to worry about for Bufferbloat or Quality

#### [Bufferbloat](https://www.bufferbloat.net/projects/)

In the downstream direction:

1. Check your modem's specifications to ensure it can handle the connection speed you're paying for. If you're on a cable connection, you should have a DOCSIS 3.1 modem at the very least. If not, get a [new modem](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#modems)
2. Flash your existing router with [DD-WRT](https://dd-wrt.com/), if [supported](https://dd-wrt.com/support/router-database/) 
   * **WARNING:** 
     * Although DD-WRT supports SQM, DD-WRT itself may not be stable or performant on your particular router
     * Flashing 3rd party firmware may cause other issues with your router. If you are not willing to work around, [report](https://forum.dd-wrt.com/phpBB2/), and debug these [issues](https://svn.dd-wrt.com/), do Option 2 below instead
     * DD-WRT builds may have been tested with your router's chipset, but not necessarily with your exact router model
2. Get a new [standalone wired](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#standalone-routers) (you will need a separate [wireless AP](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#access-points) if you choose this) or [combo wired + wireless](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#routers) router with a faster CPU and more RAM. A router that supports later specs and/or higher speeds will typically fulfill this 

#### Quality

Quality scores are typically indicative of internet connection signal strength at your modem (from your ISP). Unfortunately, most of the time this not something you can fix on your own. Contact your ISP, describing your symptoms, and tell them your modem (or ONT, if you have a fiber connection) may be experiencing low signal strength. They may either send a tech out for an onsite visit or  otherwise fix the problem remotely via changes upstream of your modem. If you are indeed experiencing low signal strength and/or the issue is on their end most ISPs will not charge for the onsite visit.

A typical "good" signal strength for cable modems is somewhere between +/- 7 dB.

### Still having problems despite OK scores

Try using a VPN with an endpoint in a major city nearby or in a major city near the datacenter of the service you're trying to use. 

## Speedtest.net

Good indicator of ping; some ISPs don't like it because they think it underestimates speed.

[Speedtest Global Index](https://www.speedtest.net/global-index): Good way of seeing how fast your connection is compared to the average in your country and worldwide. The further below your country or worldwide aveage your connection speed is, the more likely you are to have problems.

## Your ISP

e.g. [Mediacom Cable Speed Test](http://speedtest.mediacomtoday.com/)

This is the speedtest your ISP is most likely to believe. They're not entirely wrong; the other tests have a lot of variables the ISP arguably has no control over. However, if your results here are frequently significantly lower than what you pay for, you certainly have grounds to contact your ISP about it.

# SSDs

* [A Study of SSD Reliability in Large Scale Enterprise Storage Deployments](https://www.usenix.org/system/files/fast20-maneas.pdf)
* [The SSD Endurance Experiment: They’re all dead](https://techreport.com/review/27909/the-ssd-endurance-experiment-theyre-all-dead/)
* [Some Observations on SSD Bit Rot](https://www.dropbox.com/sh/30hr2cd0rsu17a8/AACsr0shX7IiHjk9Ze4m8QkMa?dl=0)

# Stress Analysis

[Lug Analysis](https://mechanicalc.com/reference/lug-analysis#air-force-method)

# Structured Cabling

[When you need plenum cable](https://www.reddit.com/r/homelab/comments/ejkrrq/using_solid_core_cat6_cable_with_ip_security/fczrxbs/)

# `sudo`

[How to run multiple `sudo` commands on the same line](https://askubuntu.com/a/634626): `sudo some-command && sudo some-other-command` or `sudo sh -c "some-command && some-other-command"`


# Synology

[RAID Calculator](https://www.synology.com/en-us/support/RAID_calculator)

# systemd

* [How to create a new systemd service](https://www.redhat.com/sysadmin/replacing-rclocal-systemd)
* [Using systemd journals to troubleshoot transient problems](https://opensource.com/article/20/8/journals-systemd)
* [vs. init](https://retrocomputing.stackexchange.com/a/14163/16563)

# Telegram

## Ubuntu

### [If the Telegram launch window has an error message only that says `FATAL: Could not open `~/.local/share/TelegramDesktop/log_startXX.txt' for writing log!`](https://github.com/telegramdesktop/tdesktop/issues/7481#issuecomment-605695563)

* Close the desktop app window
* Delete `~/.local/share/TelegramDesktop/`
* Launch the desktop app again

# Termux

* [Backing up Termux](https://wiki.termux.com/wiki/Backing_up_Termux)
* [Package Management](https://wiki.termux.com/wiki/Package_Management)

## Termux:Tasker

* [ Google Play to F-Droid Migration & Setup of Termux, Termux:Tasker, & Termux:Styling](https://dev.to/jdrch/google-play-to-f-droid-migration-setup-of-termux-termux-tasker-termux-styling-503g)

# Todoist 

[Set a recurring due date](https://todoist.com/help/articles/set-a-recurring-due-date)

# TPM

[TPM 1.2, 2.0 and fTPM (firmware-based TPM) Information](http://aps2.toshiba-tro.de/kb0/TSB8B03XO0000R01.htm)

# tsch

* [Add a splash of color to your command line environment](https://blogs.aalto.fi/marijn/2016/07/05/add-a-splash-of-color-to-your-command-line-environment/)
* [Coloring the tcsh prompt](https://www.cs.umd.edu/~srhuang/teaching/code_snippets/prompt_color.tcsh.html)
  * Comment out the 2nd prompt option  
  * To color the root crontab, make the 1st prompt option `set prompt="${green}%N${blue}@%m ${white}%~ ${green}%%${end} "` & place the file in `/root/.cshrc`
* [Customizing your shell prompt](http://www.nparikh.org/unix/prompt.php)
* [Special shell variables](https://nature.berkeley.edu/~casterln/tcsh/Special_shell_variables.html)

# Ubiquiti

## UniFi

### Controller

* [Transition from MongoDB](https://community.ui.com/user/di3/f30234be-4be5-45e5-abf9-a4c2320f7080) in version 5.13.x
* [EOL Definitions](https://community.ui.com/questions/Announcement-EOL-for-some-UniFi-AP-models/65487283-ce9d-49f4-85b9-b6aa54659ef7)

### Cloud Key

[Cloud Keys are easily corrupted by power failures](https://www.reddit.com/r/Ubiquiti/comments/f2wg2f/devices_keep_getting_lost/fhfn31p/)

# Ubuntu

* [How to Easily Add Users to Groups in Ubuntu](https://www.maketecheasier.com/add-remove-user-to-groups-in-ubuntu/) (See Section 2)
* [How to fix `symbol 'grub_calloc' not found` grub boot error](https://bugs.launchpad.net/ubuntu/+source/grub2/+bug/1889509/comments/60)
* [How to Upgrade SSD](https://github.com/jdrch/Hardware/issues/127#issuecomment-646820009)
* [Where the trash folder is located](https://askubuntu.com/a/102106/932418)

# `unattended-upgrades`

[GitHub](https://github.com/mvo5/unattended-upgrades)

# UNIX

[What UNIX Cost Us](https://www.youtube.com/watch?v=9-IWMbJXoLM) - A talk about how "the UNIX way" makes a lot of stuff much more difficult than it needs to be

# unRAID

[Calculator](http://unraid.category5.tv/)

# Veeam

* [How to place Veeam Agent for Windows backup chain on Veeam backup repository, so backup job continues chain](https://www.veeam.com/kb2321)
* The Backup & Replication installer [chokes on compressed volumes](https://forums.veeam.com/vmware-vsphere-f24/veem-backup-and-replication-9-5-update-4-fails-to-install-support-case-id-03408596-t57166.html)
* [October 2019 Gartner Magic Quadrant](https://www.acronis.com/en-us/blog/posts/acronis-earns-its-spot-gartner-2019-magic-quadrant-enterprise-datacenter-backup-and-recovery)

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

# VLC

[Builds](http://download.videolan.org/pub/videolan/vlc/)

# Volume Shadow Copy

* [How to schedule it](http://itsimple.info/?p=258)
  * Author made a mistake in the screenshots; [here's the correction](http://itsimple.info/?p=258#comment-912)
* [Powershell commands & ReFS setup](https://superuser.com/a/1261589/264738)
* [Shadow Explorer (shadow copies browsing tool)](https://www.shadowexplorer.com/downloads.html)

# Wi-Fi

* [Advanced Intel® Wireless Adapter Settings](https://www.intel.com/content/www/us/en/support/articles/000005585/network-and-i-o/wireless-networking.html)
* [The difference between a mesh, multiple APs, repeaters, and extenders](https://www.reddit.com/r/HomeNetworking/comments/jy1r1n/dlink_exo_mesh_system_or_two_routers_in_bridge/gmyk5w4/)
* [Mesh networking troubleshooting example](https://www.reddit.com/r/HomeNetworking/comments/h9r7se/ping_spikes_on_alternating_packets/)
* [Official IEEE Working Group Project Timelines](http://www.ieee802.org/11/Reports/802.11_Timelines.htm)
   * See the 802.11ax line for when the standard is likely to be ratified. It isn't as of yet
* [Wi-Fi 4/5/6 (802.11 n/ac/ad/ax)](https://www.duckware.com/tech/wifi-in-the-us.html)
* [WiFi Alliance Product Finder](https://www.wi-fi.org/product-finder)
* [What's Missing From Your Wi-Fi 6 Router? OFDMA](https://www.smallnetbuilder.com/wireless/wireless-features/33221-what-s-missing-from-your-wi-fi-6-router-ofdma)
* [What’s the Difference Between 802.11ac Wave 1 and Wave 2? [FAQ’s]](https://www.securedgenetworks.com/blog/whats-the-difference-between-802.11ac-wave-1-and-wave-2-faqs)
* [Why mesh networking is bad (example)](https://www.reddit.com/r/HomeNetworking/comments/h9igbh/will_a_mesh_network_do_its_job_if_it_can_only_use/fv4vdx6/)

## Access Point 

### Placement

[The Ars Technica semi-scientific guide to Wi-Fi Access Point placement](https://arstechnica.com/gadgets/2020/02/the-ars-technica-semi-scientific-guide-to-wi-fi-access-point-placement/)

The above article also explains that mesh wireless systems underperform under heavy network load (one of the problems they are marketed as solving.) FTA:

>  Under heavy network load, cheap wired access points like Ubiquiti UAP-AC-Lites or TP-Link EAP-225v3s absolutely smoke even the best mesh kits, if the mesh kits are limited to Wi-Fi backhaul only.

### Using a Router as an AP

**The below also applies to using a router as the downstream half of a wirless bridge**.

Do NOT do this, because most consumer routers become unreachable from the LAN when in AP mode. As such, if you want to change *any* setting at all, you have to factory reset the router and set up AP mode from scratch with your desired setting

Also, if router's Wi-Fi speed rating is less than AC1750, its performance in modern wireless environments is going to be awful.

## DFS

[SmallNetBuilder's Wi-Fi Dynamic Frequency Selection (DFS) FAQ](https://www.smallnetbuilder.com/basics/wireless-basics/33082-smallnetbuilder-s-wi-fi-dynamic-frequency-selection-dfs-faq)

## Performance

[Deriving max theoretical Wi-Fi data rates from (near-)1st principles](https://www.reddit.com/r/hardware/comments/fvthqj/deriving_max_theoretical_wifi_data_rates_from/)

## Physical blocking

If you have multipe APs and want 1 of the APs to be *exclusively* (read: clients cannot see any other AP) acessible only within a defined space, you can [Faraday Cage](https://hackaday.com/2018/09/26/building-a-hardware-store-faraday-cage/) that space.

## Range

### Improvement

As a general rule, the fewer wireless client devices you have, the better your wireless performance will be.

The following are ways to improve your wireless range, from best to worst:

1. Run Ethernet (copper or fiber) cable. Fiber is has a faster theoretical max speed, but is more brittle, requires more expensive gear, has very little client device support, cannot carry power, and has fewer capable installers. Copper cable generally has lower theoretical speeds, but has none of fiber's disadvantages. Generally speaking, unless you need network speeds in excess of 10 Gb/s, stick to Cat 6A or Cat 8 (<= 30 m runs only) copper cable. **DO NOT USE Cat 7 AS IT IS NOT A TIA STANDARD**. There are several ways to do run cable, all of which can be combined with each other:
   1. Run naked cable along the walls (in the seams between the wall and floor, floor and ceiling, or multiple walls). Use cord protectors to get the cable across foot traffic pathways, such as across doorways. **OPTIONAL**: use cable stables to attach the cable to the wall
      1. Advantages:
         1. Least expensive option
         2. Same performance as other more expensive options
         3. Easy reconfiguration
         4. If no cable staples are used, no alteration of building structure necessary (good for renters)
         5. No plenum rated cable required
      2. Disadvantages:
         1. Some people find exposed Ethernet cable and even cord protectors aesthetically unattractive
         2. Cables not in cord protectors or in unsecured cord protectors may be tripped over
         3. Cables not in cord protectors may be damaged by foot traffic, pets, children, etc.
         4. Extreme cable lengths may be needed for some runs, especially for larger homes
         5. High probability of cable tangles
         6. Secured non-velcro cord protectors need adhesive to stay put, which may damage flooring and carpeting
         7. Velcro cord protectors do not work on cut-pile carpet or non-carpet surfaces
         8. Wall alteration if cable staples are used
   2. Same as above, but adding cable raceways to hide the cable in the seams and route it around pathways
      1. Advantages:
         1. Some people find it more attractive than running naked cable
         2. Cables less likely to be damaged than if they were naked
         3. Same performance as more expensive options
         4. Lower probability of cable tangles
         5. No plenum rated cable required
         6. If no cable stables are used, no structural alteration to house needed if raceways aren't attached to the wall
      1. Disadvantages:
         1. Some people find raceways just as aesthetically unattractive as naked cable
         2. Raceways will be loose unless they are attached to the wall
         3. Attaching raceways to the wall might structurally alter the building (not good for renters)
         4. The combined thickness of cables on a given route may be too large for the raceway
         5. Wall alteration if cable staples are used
   3. [Internally wire your home for Ethernet](https://github.com/jdrch/Hardware/wiki/How-to-Get-Your-Home-Wired-For-Ethernet)
      1. Advantages:
         1. Most aesthetically attractive option
         2. More direct route to clients means shorter runs
         3. Lowest probability of cable tangles
         4. Adds value to your home (if properly finished)
         5. Minimizes need for cord protectors and raceways
      2. Disadvantages 
         1. Requires cutting into the walls of the building (not for renters)
         2. Most expensive option, even if you DIY
         3. Can reduce the value of your home if finished poorly (professional installation is a good investment)
         4. Needs special plenum-rated cable for runs routed through air ducting for fire safety
2. Use [MoCA adapters](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#moca-adapters). If you don't have an RG6 coax outlet available where you need MoCA, then either run Ethernet cable (preferred), run RG6 coax cable, or see one of the following options. Any structural cabling or electrical contractor can run RG6 cable for you
3. Get a better [combo router](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#routers) or AP (see previous AP link)
4. Use Powerline adapters. **WARNING:** Powerline adapters are very susceptible to noise and far less reliable than MoCA and Ethernet. If you do not have an electrical outlet nearby, then - in order of descending preference - run Ethernet cable, run coax cable, or install an electrical outlet. You will most likely need a licensed electrician for the outlet option for your own immediate safety and long term fire/electric shock safety of your home
5. **LAST RESORT:** Deploy a wireless backhaul (communication between the satellite and base station) mesh network. **WARNING:** Mesh networks come with their own issues and are [incredibly painful to troubleshoot](https://www.reddit.com/r/HomeNetworking/comments/h9r7se/ping_spikes_on_alternating_packets/)

For the Ethernet, MoCA, and Powerline solutions: depending on your situation you can either connect the long range client via direct cabling or place a [switch](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#switches) + [standalone AP](https://github.com/jdrch/Hardware/wiki/Recommended-Hardware#access-points) there. You can also use deploy a mesh network using the Ethernet, MoCA, or Powerline cabling for backhaul.

**NEVER** deploy a wireless extender; it will absolutely destroy your Wi-Fi performance.

## Troubleshooting

* [Access Point Placement](https://github.com/jdrch/Hardware/wiki/Useful-Links#placement)
* [Troubleshooting 'slow' Wi-Fi](https://www.duckware.com/tech/wifi-in-the-us.html#troubleshooting)

### Check for excessive DNS lookups from clients

**WARNING:** This is an advanced, involved troubleshooting method that involves network reconfiguration (setting Pi-hole as your network's DNS and DHCP server, then rebooting all your network clients for the setting to take effect).

1. Install & setup Pi-hole (see above)
2. In the Pi-hole dashboard, look for clients making an inordinate number of DNS lookups relative to their use. Check the query logs for such clients. Typically the lookups will be repetitive, such as multiple reverse lookups for another client on the LAN
3. Use [this method](https://www.reddit.com/r/pihole/comments/gytfbm/guide_how_to_discover_which_app_is_making_dns/) to find which process on each affected client is making the excessive lookups
4. Disable the process found in the above step
5. Repeat Step 2. If the excessive DNS queries are gone, you've solved the problem

# Wireless Charging

[Wirless charging uses 47% more power than wired charging](https://onezero.medium.com/wireless-charging-is-a-disaster-waiting-to-happen-48afdde70ed9)

# Xbox

[Everybody missed the point of the Showcase. Microsoft's gaming business plan is not dependent on next gen console sales or even solely on GamePass (which is what smarter bloggers have been saying). It's based on services for gamers, studios, publishers, and even Sony and Nintendo](https://www.reddit.com/r/XboxSeriesX/comments/hxwpvz/everybody_missed_the_point_of_the_showcase/)

# [The XY Problem](http://xyproblem.info/)

# Zabbix

[Documentation](https://www.zabbix.com/documentation/current/start)

# ZFS 

* [Aaron Toponce's ZFS guide](https://pthree.org/2012/04/17/install-zfs-on-debian-gnulinux/)
* [Feature Matrix](https://zgrep.org/zfs.html)
* [Latest OpenZFS development status and relationship among projects](https://drive.google.com/file/d/197jS8_MWtfdW2LyvIFnH58uUasHuNszz/view)
* [Linus Torvalds recommends against ZFS (on Linux)](https://www.realworldtech.com/forum/?threadid=189711&curpostid=189841)
* [Performance, Part 1](https://www.ixsystems.com/blog/zfs-pool-performance-1/)
* [Performance, Part 2](https://www.ixsystems.com/blog/zfs-pool-performance-2/)
* [Quickstart (See Steps 3 to 6)](https://github.com/jdrch/Hardware/wiki/How-to-Set-Up-Regular,-Recurring,-Incremental,-Online-Filesystem-Backups-using-Restic)
* [RAIDZ*x* vs. mirroring resilience to *F* drive destruction](https://github.com/jdrch/Hardware/wiki/How-to-Calculate-the-Odds-of-Physical-Attack-Data-Loss-for-a-ZFS-Array)
* [When To (and Not To) Use RAID-Z](https://blogs.oracle.com/roch/when-to-and-not-to-use-raid-z)
* [Why OpenZFS on Linux may be incompatible with Solaris ZFS](https://zfsonlinux.topicbox.com/groups/zfs-discuss/T1c57a2d200afe924-M7e33781f8e51bd16a68f737a/openzfs-renders-zfs-disks-unusable-why)
* [ZFS 101—Understanding ZFS storage and performance](https://arstechnica.com/information-technology/2020/05/zfs-101-understanding-zfs-storage-and-performance/)
* [ZFS versus RAID: Eight Ironwolf disks, two filesystems, one winner](https://arstechnica.com/gadgets/2020/05/zfs-versus-raid-eight-ironwolf-disks-two-filesystems-one-winner/)

## Deduplication

[How to check whether a zpool would benefit from deduplication](https://docs.oracle.com/cd/E37838_01/html/E61017/gazss.html#SVZFSgjhav):

* `# zdb -S zpoolName`
* Check the value of the `dedup` output. Do not enable deduplication if `dedup` ≤ 2

## How to clone an all-ZFS boot HDD

`# zfs send -R` replicates everything, including all properties you need to make the target system bootable

# `zfsnap`

* [Homepage](https://www.zfsnap.org/)
* [Github](https://github.com/zfsnap/zfsnap.org)

# zrep

* [Homepage](http://www.bolthole.com/solaris/zrep/)
* [Github](https://github.com/bolthole/zrep)