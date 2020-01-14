Note: I haven't used everything on this list. Some of these products are simply what I consider to be the best or best value for money in their category.

# Cables

## Brands

* Monoprice
* Cables2Go
* StarTech.com

# Cases/Chassis

## Rackmount

[RSV-L4312 – 4U Rackmount with 5 Cooling Fans, 12 Internal Bays](https://www.rosewill.com/product/rsv-l4312-4u-rackmount-with-5-cooling-fans-12-internal-bays/)

## Desktop

### Tower

#### Full

##### No Tempered Glass

[Phanteks Enthoo Pro](http://www.phanteks.com/Enthoo-Pro.html)

##### Tempered Glass

[Phanteks Enthoo Pro Tempered Glass](http://www.phanteks.com/Enthoo-Pro-TemperedGlass.html)

# Computers

## Specifications

### New

1. CPU: ≥ 4C/8T for mainstream use, ≥ 6C/12T for gaming
2. RAM: Max supported RAM (by motherboard) ≥ 16 GB
3. LAN: ≥ 1000BASE-T Ethernet
4. Bluetooth: ≥ 5.0
5. Wi-Fi: ≥ 2x2 802.11ac
6. USB: ≥ USB 3.1 Gen 1
7. Storage: NVMe SSD at the least
8. GPU/video out: HDMI ≥ 1.4 or DisplayPort ≥ 1.2
9. Display: ≥ 1080p for < 17 in; ≥ 2160p for ≥ 17.3 in

### Used

1. CPU: ≥ 2C/4T
   * Must be either covered by speculative execution security patches (e.g. Intel Core 2nd Gen and above) or unaffected by speculative execution vulnerabilities 
2. RAM: Max supported RAM (by CPU) ≥ 8 GB
3. USB: ≥ USB 2.0
4. Storage: Available port for SATA SSD
5. GPU/video out: ≥ HDMI
6. Display: ≥ 768p
7. LAN: ≥ 1000BASE-T Ethernet

## Enterprise product lines

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

# Docks

## USB 3.1 Gen 1+

[StarTech HDD Docking Stations](https://www.startech.com/HDD/Docking/?filter_IOINTERFACE=USB+3.1+Gen+2)

# NAS

## Raspberry Pi

[Penta SATA HAT](https://wiki.radxa.com/Penta_SATA_HAT)

# Networking

## Wired

### MoCA adapters

* [Actiontec Bonded MoCA 2.0 Network Adapter](https://www.actiontec.com/products/home-networking/ecb6200/)
* [Hitron HT-EM2](http://www.hitron-americas.com/product/ht-em2/)

## Wireless 

### Access Points

#### High Performance

If you don't absolutely need an AP right now, wait for Ubiquity UniFi Wi-Fi 6 APs before buying. Also, bear in mind you'll need UniFi Controller for all of the following. If you want to run Controller on standalone hardware, I recommend Debian 10 on a [used PC](https://github.com/jdrch/Hardware#what-are-the-minimum-specs-you-recommend-for-any-used-pc) or Raspbian on a Raspberry Pi 4. 

In order of increasing performance and client density:

* [Ubiquiti UniFi AP HD](https://www.ubnt.com/downloads/datasheets/unifi/UniFi_UAP-AC-HD_DS.pdf)
* [Ubiquiti UniFi AP SHD](https://dl.ubnt.com/datasheets/unifi/UniFi_UAP-AC-SHD_DS.pdf)
* [Ubiquiti UniFi AP XG](https://dl.ubnt.com/datasheets/unifi/UniFi_XG_AP_DS.pdf)

#### Value

If you absolutely need to save money or better Windows support than what UniFi Controller offers:

[EAP245 V3](https://www.tp-link.com/us/business-networking/ceiling-mount-access-point/eap245/v3/) + [Omada Software Controller](https://www.tp-link.com/us/business-networking/ceiling-mount-access-point/eap-controller/) + [Omada app](https://play.google.com/store/apps/details?id=com.tplink.omada)

# Storage

## HDDs

Generally speaking, all HDDs that lack a workload rating have the same reliability. The only 2.5 in HDDs with workload ratings are ≥ 15 mm thick, which means they consume (nearly) as much space as a 3.5 in HDD. Also, I have no experience with the former. Ergo, they are omitted here.

Western Digital's UltraStar DC HC550 *should* be recommendable, but it [lacks a spec sheet](https://www.reddit.com/r/hardware/comments/e0bkwe/no_datasheets_and_contradictory_product_brochures/).

### 3.5 in

* [Seagate Exos X Enterprise Hard Drives](https://www.seagate.com/enterprise-storage/exos-drives/exos-x-drives/)
* Toshiba Enterprise Capacity Hard Drive – MG Series
  * [US product page](https://toshiba.semicon-storage.com/us/product/storage-products/enterprise-hdd.html) (Limited US availability, especially for higher end models) 
  * [EMEA product page](https://www.toshiba-storage.com/products/enterprise-capacity-hard-drive-mg-series/) with comprehensive [PDF spec sheet](https://www.toshiba-storage.com/wp-content/uploads/2019/09/TOSH_DS_MG_Series_print.pdf)
* [WD Gold Enterprise Class SATA HDD](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/internal-drives/wd-gold/product-brief-wd-gold-2579-810192.pdf)

#### Accessories

[StarTech.com 3.5in Silicone Hard Drive Protector Sleeve with Connector Cap](https://www.startech.com/HDD/Brackets/35in-Silicone-Laptop-Hard-Drive-Protector-Sleeve-with-Connector-Cap~HDDSLEV35)

##### Brands

* StarTech.com (always check here first)
* IcyDock
* Vantec

## SATA Controller Cards (non-RAID)

### PCI Express 1.0 x1

[StarTech.com 2 Port PCI Express SATA 6 Gbps eSATA Controller Card](https://www.startech.com/Cards-Adapters/HDD-Controllers/SATA-Cards/2-Port-PCI-Express-SATA-6-Gbps-eSATA-Controller-Card~PEXESAT322I)

### PCI Express 3.1 x4

[SYBA 5 port Non-RAID SATA III 6Gbp/s PCI-e x4 Controller Card](https://www.sybausa.com/index.php?route=product/product&path=64_181_85&product_id=1027&filter=38,19&limit=32)

## SSDs

### SATA

Unless you're using the SSD in an extremely write-heavy application (e.g. as an array cache drive) or need > 2 TB of capacity, get the Crucial MX500.

#### Performance & Endurance

* [Samsung SSD 860 EVO 2.5" SATA III](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/ssd-860-evo-2-5--sata-iii-2tb-mz-76e2t0b-am/)
* [Samsung SSD 860 PRO 2.5" SATA III](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/ssd-860-pro-2-5--sata-iii-2tb-mz-76p2t0bw/)

#### Value

[Crucial MX500 3D NAND SATA 2.5" 7mm (with 9.5mm adapter) Internal SSD](https://www.crucial.com/usa/en/ct2000mx500ssd1)

### NVMe

Don't skimp on performance with NVMe. Samsung is the fastest, highest endurance, and best supported on the market.

[Samsung SSD 970 EVO Plus NVMe M.2](https://www.samsung.com/us/computing/memory-storage/solid-state-drives/ssd-970-evo-plus-nvme-m-2-1-tb-mz-v7s1t0b-am/)

## Tape

### LTO-8

#### Drives

##### Internal

[Quantum LTO Drives](https://iq.quantum.com/exLink.asp?10444458OP44N16I37407297&view=1)
* TC-L82AN-EY
* TC-L82AN-BR

# UPS

## Sine Wave

* CyberPower
  * [PFC Sinewave](https://www.cyberpowersystems.com/products/ups/pfc-sinewave/)
  * [New SmartApp Sinewave](https://www.cyberpowersystems.com/products/ups/new-smart-app-sinewave/)
* APC
  * [Back UPS PRO BR SineWave](https://www.apc.com/shop/us/en/categories/power/uninterruptible-power-supply-ups-/computer-and-peripheral/back-ups-pro/N-1itz49c) (search that page for "SineWave" as APC doesn't breakout sine wave UPS units)
* [Tripp-Lite](https://www.tripplite.com/products/ups-battery-backup~11) (search that page for "Sine" as Tripp-Lite doesn't breakout sine wave units)

### Automatic restart of loads after UPS shutdown

[APC Smart-UPS 1500VA LCD 120V with SmartConnect](https://www.apc.com/shop/us/en/products/APC-Smart-UPS-1500VA-LCD-120V-with-SmartConnect/P-SMT1500C)