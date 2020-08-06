Note: I haven't used everything on this list. Some of these products are simply what I consider to be the best or best value for money in their category.

# Cabinets

## Ventilation

[AC Infinity](https://www.acinfinity.com/)

# Cables

## Brands

* Monoprice
* Cables2Go
* StarTech.com

## Testers

The following 2 items are highly rated and should be bought together:

* [Klein Tools Cable Tester Kit with Scout® Pro 3 Tester, Remotes, Adapter, Battery](https://www.kleintools.com/catalog/cable-testers-accessories/cable-tester-kit-scout-pro-3-tester-remotes-adapter-battery)
* [Klein Tools Probe-PRO Tracing Probe](https://www.kleintools.com/catalog/tone-probe/probe-pro-tracing-probe)

# Cases/Chassis 

These recommendations are primarily storage oriented.

## Rackmount (# of 3.5" HDDs || Max # & type of AICs)

* [Advantech](https://www.advantech.com/products/server-chassis/sub_214580ab-268b-4b3c-b02e-0c5d94d0ca14)
  * [2U Chassis](https://www.advantech.com/products/2u-chassis/sub_4u_industrial_server)
    * [HPC-7282](https://www.advantech.com/products/4u_industrial_server/hpc-7282/mod_77c9cedc-fcaf-4129-a5f0-a9ac86ac3976) (8 || 7 Low Profile)
    * [HPC-8212](https://www.advantech.com/products/4u_industrial_server/hpc-8212/mod_8e45b38f-3059-445f-b1e0-02d1eef72325) (12 || 7 Low Profile / 3 Full Height, Full Length)
  * [3U Chassis](https://www.advantech.com/products/3u-chassis/sub_9d52d6b7-f385-42de-9af4-779465d54e9a)  
    * [HPC-8316](https://www.advantech.com/products/9d52d6b7-f385-42de-9af4-779465d54e9a/hpc-8316/mod_55cbce0d-b4d2-4cef-850f-e26852685197) (16 || 6 Full Height, Full Length)
  * [4U Chassis](https://www.advantech.com/products/4u-chassis/sub_4u_server_chassis)
    * [HPC-7484](https://www.advantech.com/products/4u_server_chassis/hpc-7484/mod_bd06a4a2-46c2-4f57-aa08-bd286255d781) (8 || 7 Full Height, Full Length)
    * [HPC-8424](https://www.advantech.com/products/4u_server_chassis/hpc-8424/mod_488d4a34-a383-4346-8375-8c275e481c0c) (24 || 7 Full Height, Full Length)

* [AIC](https://www.aicipc.com/en/solutions/170-1419)
  * 2U
    * [RSC-2ET](https://www.aicipc.com/en/productdetail/84) (12 || 7 Low Profile)
  * 3U
    * [RSC-3ET](https://www.aicipc.com/en/productdetail/85) (16 || 7 Full Height)
  * 4U
    * [RSC-4BT](https://www.aicipc.com/en/productdetail/86) (36 || 7 Low Profile)
    * [RSC-4ET](https://www.aicipc.com/en/productdetail/87) (24 || 7 Full Height)
    * [RSC-4H](https://www.aicipc.com/en/productdetail/91) (60 || 7 Full Height)

* [iStarUSA](http://www.istarusa.com/en/istarusa/)
  * 3U
    * [D-3100HN](http://www.istarusa.com/en/istarusa/products.php?model=D-3100HN) (10 || 4 Full Height, Full Length(?)) **(WARNING: the first three expansion slots on an ATX motherboard cannot be used if the latter is installed in this chassis)**

* [Supermicro](https://www.supermicro.com/en/support/product-matrices)
  * [2U Super Chassis](https://www.supermicro.com/products/chassis/2U/)
    * [825](https://www.supermicro.com/products/chassis/2U/?chs=825) (8 || 7 Low Profile / 4 Full Height, Full Length / 7 Low Profile, Full Length)
    * [826](https://www.supermicro.com/products/chassis/2U/?chs=826) (8 / 12 || 7 Low Profile / 4 Full Height, Full Length)
  * [3U SuperChassis](https://www.supermicro.com/products/chassis/3U/)
    * [835](https://www.supermicro.com/products/chassis/3U/?chs=835) (8 || 7 Full Height, Full Length / 4 Full Height, Half Length)
  * [4U SuperChassis](https://www.supermicro.com/products/chassis/4U/)
    * [846](https://www.supermicro.com/products/chassis/4U/?chs=846) (24 || 7 Full Height, Full Length)
    * [847](https://www.supermicro.com/products/chassis/4U/?chs=847) (36 / 44 / 90 || 7 Low Profile / 4 Full Height, Full Length)

## Desktop

### Tower

#### Full

[Fractal Define 7 XL](https://www.fractal-design.com/products/cases/define/define-7-xl/black/)
* [HDD Drive Tray Kit – Type A](https://www.fractal-design.com/products/accessories/hdd-drive-tray-kit-type-a/black/)

# Computers

## Specifications

I do not suggest investing in anything wirless that isn't Wi-Fi 6 or higher.

### New

1. CPU: ≥ 4C/8T for mainstream use, ≥ 6C/12T for gaming
2. RAM: Max supported RAM (by motherboard) ≥ 16 GB
3. LAN: ≥ 1000BASE-T Ethernet
4. Bluetooth: ≥ 5.0
5. Wi-Fi: ≥ 2x2 802.11ax
6. USB: ≥ USB 3.1 Gen 1
7. Storage: NVMe SSD at the least
8. GPU/video out: HDMI ≥ 1.4 or DisplayPort ≥ 1.2
9. Display: ≥ 1080p for < 17 in; ≥ 2160p for ≥ 17.3 in

#### Hardened

**Note:** I'm not aware of any independent audits of the following lines, but I'm also not aware of an actively exploited unpatched vulnerabilities. Generally, as long you 

1. Aggressive patch and update:
   * your entire software stack
     * BIOS
     * drivers
     * OS
     * apps
2. Use the disk encryption with a locally stored key 
   * Linux: Veracrypt or ZFS encryption
   * Windows: Bitlocker + TPM 
   * FreeBSD: ZFS encryption
   * macOS: Default new installation of latest release on supported Apple hardware

you should be fine.

* [Apple Mac](https://www.apple.com/mac/) (macOS)    
* [Purism Librem](https://puri.sm/products/) (Linux)
* [Secured-Core PCs](https://www.microsoft.com/en-us/windowsforbusiness/windows10-secured-core-computers) (Windows)

### Used

1. CPU: ≥ 2C/4T
   * Must be either covered by speculative execution security patches (e.g. Intel Core 2nd Gen and above) or unaffected by speculative execution vulnerabilities 
2. RAM: Max supported RAM (by CPU) ≥ 8 GB
3. USB: ≥ USB 2.0
4. Storage: Available port for SATA SSD
5. GPU/video out: ≥ HDMI
6. Display: ≥ 768p
7. LAN: ≥ 1000BASE-T Ethernet
8. Wi-Fi: ≥ 2x2 802.11ax

## Enterprise desktop product lines

* Dell
   * OptiPlex
   * Precision
* Lenovo
   * ThinkCentre
   * ThinkStation
* HP
   * Elite
   * Pro
   * Z

# Displays

## Monitors

[BenQ Designer Monitor with 27 inch, 4K UHD, sRGB | PD2700U](https://www.benq.com/en-us/monitor/designer/pd2700u.html)
* High end monitor users tend to be very demanding and nitpicky, so anything with a ≥ 4/5 ⭐ rating is very, very good

# Docks

## USB 3.1 Gen 1+

[StarTech HDD Docking Stations](https://www.startech.com/HDD/Docking/?filter_IOINTERFACE=USB+3.1+Gen+2)

# NAS

## Raspberry Pi

[Penta SATA HAT](https://wiki.radxa.com/Penta_SATA_HAT)

# Networking

## Modems

### Cable

[Arris SB8200 SURFboard DOCSIS 3.1 Cable Modem](https://www.arris.com/surfboard/products/cable-modems/sb8200/) ​

## Switches

### Unmanaged

Assuming they have the specs and features you want, *always* buy NETGEAR Business for unmanaged switches. Other brands are nowhere near as reliable and NETGEAR's warranty and support are the best in the business.

[NETGEAR Gigabit Ethernet Unmanaged Switches](https://www.netgear.com/images/datasheet/switches/GS105v5_GS108v4_GS116v2.pdf)

#### PoE

[NETGEAR 8-port and 16-port Gigabit Ethernet Unmanaged PoE/PoE+ Switches](https://www.netgear.com/images/datasheet/switches/GS108LP_GS108PP_GS116LP_GS116PP_DS.pdf)

## Wired

[Not all Ethernet NICs are Created Equal - Trying to Capture Invalid Ethernet Frames](https://isc.sans.edu/diary/rss/25896) (Why Intel NICs are superior to Realtek, Broadcom, and ASIX NICs)

### MoCA adapters

[Certified products](http://www.mocalliance.org/products/index.htm)

#### MoCA 2.5

This is the 2.5 Gb/s standard.

* [Actiontec ECB6250 MoCA 2.5 Network Adapter](https://www.actiontec.com/products/home-networking/moca-2-5-network-adapter-ecb6250) (Sold to service providers only)
* [goCoax WF-803M](https://www.gocoax.com/product-page/copy-of-wf-803m)

#### MoCA 2.0

This is the 1 Gb/s standard.

* [Actiontec Bonded MoCA 2.0 Network Adapter](https://www.actiontec.com/products/home-networking/ecb6200/)
* [Hitron HT-EM2](http://www.hitron-americas.com/product/ht-em2/) (Difficult to find at retail; check service provider)

### Standalone Routers

The following routers offer enterprise level performance, line speed routing, and easy OpenVPN functionality while still covering consumer features such as UPnP.

* [Netgate SG-3100 & Above](https://store.netgate.com/Assets/Images/ChartsTables/Netgate_Hardware_Comparison_Chart.png)
* [Netgear BR500 Insight Instant VPN Router](https://www.netgear.com/images/datasheet/security/BR500.pdf)

## Wireless 

### Access points

#### High performance

If you don't absolutely need an AP right now, wait for Ubiquity UniFi Wi-Fi 6 APs ***[with OFDMA enabled](https://www.smallnetbuilder.com/wireless/wireless-features/33221-what-s-missing-from-your-wi-fi-6-router-ofdma?start=0)*** before buying. Also, bear in mind you'll need UniFi Controller for all of the following. If you want to run Controller on standalone hardware, I recommend ~~Debian 10 on a [used PC](https://github.com/jdrch/Hardware#what-are-the-minimum-specs-you-recommend-for-any-used-pc) or~~Raspbian on a Raspberry Pi 4. 

##### 802.11ac

In order of increasing performance and client density:

* [Ubiquiti UniFi AP HD](https://www.ubnt.com/downloads/datasheets/unifi/UniFi_UAP-AC-HD_DS.pdf)
* [Ubiquiti UniFi AP SHD](https://dl.ubnt.com/datasheets/unifi/UniFi_UAP-AC-SHD_DS.pdf)
* [Ubiquiti UniFi AP XG](https://dl.ubnt.com/datasheets/unifi/UniFi_XG_AP_DS.pdf)

#### Value

If you absolutely need to save money or better Windows support than what UniFi Controller offers:

[TP-Link EAP245 V3](https://www.tp-link.com/us/business-networking/ceiling-mount-access-point/eap245/v3/) + [Omada Software Controller](https://www.tp-link.com/us/business-networking/ceiling-mount-access-point/eap-controller/) + [Omada app](https://play.google.com/store/apps/details?id=com.tplink.omada)

### Routers

#### High Performance

##### 802.11ac

[Ubiquiti UniFi Dream Machine](https://store.ui.com/collections/routing-switching/products/unifi-dream-machine)

##### 802.11ax 

(Wi-Fi 6)

**CAUTION**: Although Wi-Fi Alliance certification for this has begun, the standard has not yet been finalized by the IEEE. Buy products at your own risk.

In the router/AP's Wi-Fi Alliance Wi-Fi 6 certificate, the following should be in the:

1. **Security** section:
   1. WPA3™ - Personal
2. **Wi-Fi CERTIFIED 6™** section:
   1. OFDMA
      1. DL OFDMA
      2. UL OFDMA
   2. MU-MIMO
   3. Maximum Supported Channel Width (20, 40, 80, 160 MHz)
   4. Target Wake Time (TWT)
   5. MCS 10-11 Rx (= 1024-QAM)
   6. Beamforming

[ASUS RT-AX88U](https://www.asus.com/us/Networking/RT-AX88U/) - ([Wi-Fi 6 Certificate](http://certifications.prod.wi-fi.org/pdf/certificate/public/download?cid=WFA91821))

#### Value

All products listed under this heading are [Wi-Fi certified](https://www.wi-fi.org/product-finder).

##### 802.11ac

**WARNING**: The following products [canNOT be guaranteed](https://github.com/jdrch/Hardware/wiki/Useful-Links#bufferbloat) to not be affected by Bufferbloat.

* [TP-Link Archer C8](https://www.tp-link.com/us/home-networking/wifi-router/archer-c8/) (WARNING: Firmware updates factory reset this router, and it typically locks up or needs a power cycle about once every 2 to 3 months)
* [NETGEAR R6400 AC1750 Smart WiFi Router](https://www.netgear.com/home/products/networking/wifi-routers/R6400.aspx)
* [NETGEAR R6700 Nighthawk AC1750 Smart WiFi Router](https://www.netgear.com/home/products/networking/wifi-routers/R6700.aspx) (NOTE: Despite the higher model number, get the R6400 above instead if it's available)

**WARNING**: The following product is less likely to be affected by Bufferbloat than the previous ones due to its Linux kernel version (3.x), but that cannot be guaranteed

[Synology Router RT2600ac](https://www.synology.com/en-us/products/RT2600ac)

# Scanners

## Automatic Document Feed (ADF)/Flatbed

For some reason, it's become incredibly difficult to find highly rated (≥ 4 ⭐) ADF + flatbed scanners. However, the following model comes the closest of all (the affordable ones) I've seen:

[Xerox Duplex Combo Scanner](https://www.xeroxscanners.com/en/us/products/item.asp?PN=XDCS)

# Storage

## Adapters

* [StarTech.com SATA to 2.5in or 3.5in IDE Hard Drive Adapter for HDD Docks](https://www.startech.com/HDD/Adapters/SATA-to-IDE-Hard-Drive-Adapter-for-HDD-Docks~SAT2IDEADP)
* [SYBA SATA II to IDE ATA133 Bi-directional Adapter - SD-ADA50016](http://www.sybausa.com/index.php?route=product/product&product_id=191&search=SD-ADA50016)

## Cloud

The only providers I recommend are (in alphabetical order):

* Amazon
* Backblaze
* Dropbox
* Google
* Microsoft

## HDDs

Generally speaking, all HDDs that lack a workload rating have the same reliability. The only 2.5 in HDDs with workload ratings are ≥ 15 mm thick, which means they consume (nearly) as much space as a 3.5 in HDD. Also, I have no experience with the former. Ergo, they are omitted here.

### 3.5 in

Get the 512e models of these, or the 4Kn models if the former are unavailable. Do NOT buy 512n:

* [Seagate Exos X Enterprise Hard Drives](https://www.seagate.com/enterprise-storage/exos-drives/exos-x-drives/) - X14 and above Exos X models can be converted between 512e and 4Kn using Seagate's [SeaChest Format](https://github.com/Seagate/ToolBin/tree/master/SeaChest/Format) [`--setSectorSize`](https://github.com/Seagate/ToolBin/blob/master/SeaChest/Format/v1.5.2/SeaChest_Format.152.txt) option
* Toshiba Enterprise Capacity Hard Drive – MG Series
  * [US product page](https://toshiba.semicon-storage.com/us/product/storage-products/enterprise-hdd.html) (Limited US availability, especially for higher end models) 
  * [EMEA product page](https://www.toshiba-storage.com/products/enterprise-capacity-hard-drive-mg-series/) with comprehensive [PDF spec sheet](https://www.toshiba-storage.com/wp-content/uploads/2019/09/TOSH_DS_MG_Series_print.pdf)
* Western Digital
  * [Gold Enterprise Class SATA HDD](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/internal-drives/wd-gold/product-brief-wd-gold-2579-810192.pdf)
  * Ultrastar DC HC (Ships with choice of SATA or SAS and native sector size. Both the 300 and 500 series HDDs have the same workload rating, but the 500 series is helium filled and has a lower annualized failure rate (AFR). The 2nd digit in the series number is apparently a drive raw capacity reference)
    * [320](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/data-center-drives/ultrastar-dc-hc300-series/data-sheet-ultrastar-dc-hc320.pdf)
    * [330](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/data-center-drives/ultrastar-dc-hc300-series/data-sheet-ultrastar-dc-hc330.pdf)
    * [510](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/data-center-drives/ultrastar-dc-hc500-series/data-sheet-ultrastar-dc-hc510.pdf)
    * [520](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/data-center-drives/ultrastar-dc-hc500-series/data-sheet-ultrastar-dc-hc520.pdf)
    * [530](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/data-center-drives/ultrastar-dc-hc500-series/data-sheet-ultrastar-dc-hc530.pdf)
    * [550](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/data-center-drives/ultrastar-dc-hc500-series/data-sheet-ultrastar-dc-hc550.pdf)
    
#### Accessories

[StarTech.com 3.5in Silicone Hard Drive Protector Sleeve with Connector Cap](https://www.startech.com/HDD/Brackets/35in-Silicone-Laptop-Hard-Drive-Protector-Sleeve-with-Connector-Cap~HDDSLEV35)

##### Brands

* StarTech.com (always check here first)
* IcyDock
* Vantec

## SATA controller cards (non-RAID)

### Throughput needs

The following are based on the highest known (to me) specified throughput values. Check the specs of the disks you're intending to connect to the controller card for their throughput values. To avoid bottlenecking, ensure the selected card's throughput per port exceeds your disks' maximum individual throughput.

* HDDs: ≥ 270 MB/s (estimated)
* SSDs: ≥ 550 MB/s (estimated)
  * AFAIK no SATA controller supports this much throughput per port. Users intending to use SSDs should probably use a higher end HBA instead
* SATA 3.0: 750 MB/s
  * The above comment for SSDs applies 

#### How to calculate throughput per port

1. Look up the **Throughput** value corresponding to the card's **PCI Express version** and lane count (x*n*, where *n* is an integer) in the **PCI Express link performance** table [here](https://en.wikipedia.org/wiki/PCI_Express#History_and_revisions)
2. Divide the result in 1) by the number of ports on the card

Always select the highest PCI Express version (1.0, 2.0, etc.) for your available slot (x1, x2, etc.) *OR*, if you have multiple available slots, the PCI Expression version + slot width combination that gives you the highest throughput in the **PCI Express link performance table** in 1) above.

### PCI Express version + lane count combinations to avoid

The following combinations might bottleneck the connected disks and should be avoided unless there are no other options:

* 1.0 x1,2
* 2.0 x1

### Cards

#### PCI Express 2.0 x4

* [High Point Rocket 640L](https://highpoint-tech.com/USA_new/series_r600-overview.htm) (4 ports, 500 MB/s/port)
* [SYBA 4 Port SAS/SATA 6Gbps PCI-e 2.0 x4 Card - SY-PEX40096](https://www.sybausa.com/index.php?route=product/product&path=64_181_85&product_id=827&filter=38,19,188&sort=p.price&order=ASC&limit=32) (500 MB/s/port)
  * The "PCIe 2.0 Host Interface (up to 5.0 Gbps)" on the product page appears to be a typo; PCI Express 2.0 has a 5.0 GT/s transfer rate

#### PCI Express 3.1 x2

[SYBA 5 port Non-RAID SATA III 6Gbp/s PCI-e x4 Controller Card](https://www.sybausa.com/index.php?route=product/product&path=64_181_85&product_id=1027&filter=38,19&limit=32) (340 MB/s/port) **(WARNING: this card provides x2 lane width but requires an x4 slot. Use it only if you lack the slot width for the 2 preceding picks and/or need more than 4 ports)**

## SSDs

### SATA

Unless you're using the SSD in an extremely write-heavy application (e.g. as an array cache drive) or need > 2 TB of capacity, get the Crucial MX500.

#### Performance & endurance

* [Samsung SSD 860 EVO 2.5" SATA III](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/ssd-860-evo-2-5--sata-iii-2tb-mz-76e2t0b-am/)
* [Samsung SSD 860 PRO 2.5" SATA III](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/ssd-860-pro-2-5--sata-iii-2tb-mz-76p2t0bw/)

#### Value

[Crucial MX500 3D NAND SATA 2.5" 7mm (with 9.5mm adapter) Internal SSD](https://www.crucial.com/usa/en/ct2000mx500ssd1)

### NVMe

Don't skimp on performance with NVMe. Samsung is the fastest, highest endurance, and best supported on the market.

#### PCI Express 3.0

[Samsung SSD 970 EVO Plus NVMe M.2](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/ssd-970-evo-plus-nvme-m-2-1-tb-mz-v7s1t0b-am/)

#### PCI Express 4.0

Samsung SSD 980 PRO ([Announced at CES 2020](https://www.anandtech.com/show/15352/ces-2020-samsung-980-pro-pcie-40-ssd-makes-an-appearance), not yet available)

## Tape

### LTO-8

Note: all LTO-8 drives need SAS at the minimum and do not support SATA. 

#### Drives

##### External

[HPE StoreEver LTO-8 Ultrium 30750 External Tape Drive](https://buy.hpe.com/us/en/storage/tape-storage/tape-drives-ultrium/storeever-ultrium-tape-drives/hpe-storeever-lto-ultrium-tape-drives/hpe-storeever-lto-8-ultrium-30750-external-tape-drive/p/BC023A)

##### Internal

* [Quantum LTO Drives](https://iq.quantum.com/exLink.asp?10444458OP44N16I37407297&view=1)
  * TC-L82AN-EY
  * TC-L82AN-BR
* [HPE StoreEver LTO-8 Ultrium 30750 Internal Tape Drive](https://buy.hpe.com/us/en/storage/tape-storage/tape-drives-ultrium/storeever-ultrium-tape-drives/hpe-storeever-lto-ultrium-tape-drives/hpe-storeever-lto-8-ultrium-30750-internal-tape-drive/p/BC022A)

# Streaming Player

[Roku Ultra](https://www.roku.com/products/roku-ultra)

# TV

[TCL Class 6-Series 4K QLED Dolby Vision HDR Roku Smart TV](https://www.tcl.com/us/en/products/home-theater/6-series/tcl-55-class-6-series-4k-qled-hdr-roku-smart-tv-55r625)

# UPS

I've heard good things about Eaton, but their lineup on their product site is pretty much impossible to filter, so I really have no idea where to start with them.

## Sine Wave

* CyberPower
  * [PFC Sinewave](https://www.cyberpowersystems.com/products/ups/pfc-sinewave/)
  * [New SmartApp Sinewave](https://www.cyberpowersystems.com/products/ups/new-smart-app-sinewave/)
* APC
  * [Back UPS PRO BR SineWave](https://www.apc.com/shop/us/en/categories/power/uninterruptible-power-supply-ups-/computer-and-peripheral/back-ups-pro/N-1itz49c) (search that page for "SineWave" as APC doesn't breakout sine wave UPS units)
* [Tripp-Lite](https://www.tripplite.com/products/ups-battery-backup~11) (search that page for "Sine" as Tripp-Lite doesn't breakout sine wave units)

### Automatic restart of loads after UPS shutdown

* APC
  * Smart-UPS ([Differences between picks](https://www.apc.com/shop/us/en/tools/compare-products/g2ar2/SMT1500C|SMC1500C/450))
    * [C LCD 120V with SmartConnect](https://www.apc.com/shop/us/en/products/APC-Smart-UPS-C-1500VA-LCD-120V-with-SmartConnect/P-SMC1500C)
    * [LCD 120V with SmartConnect](https://www.apc.com/shop/us/en/products/APC-Smart-UPS-1500VA-LCD-120V-with-SmartConnect/P-SMT1500C)

# USB

## Type C

[The Best USB-C Cables and Adapters](https://thewirecutter.com/reviews/best-usb-c-cables/)

### Charge + Listen adapters

* [Belkin RockStar™ 3.5mm Audio + USB-C™ Charge Adapter](https://www.belkin.com/us/p/P-F7U080/)
* [Moshi USB-C Digital Audio Adapter with Charging](https://www.moshi.com/en/product/usb-c-to-digital-audio-adapter-with-charging-adapter-ipad-pro/silver)