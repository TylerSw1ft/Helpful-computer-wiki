Note: I haven't used everything on this list. Some of these products are simply what I consider to be the best or best value for money in their category.

# Cases/Chassis

## Rackmount

[Rosewill RSV-4015L – 4U Rackmount with 8 Cooling Fans, 15 Internal Bays](https://www.rosewill.com/product/rsv-4015l-4u-rackmount-with-8-cooling-fans-15-internal-bays/)

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
2. RAM: Max supported RAM ≥ 16 GB
3. LAN: ≥ 1000BASE-T Ethernet
4. Bluetooth: ≥ 5.0
5. Wi-Fi: ≥ 2x2 802.11ac
6. USB: ≥ USB 3.1 Gen 1
7. Storage: NVMe SSD at the least
8. GPU/video out: HDMI ≥ 1.4 or DisplayPort ≥ 1.2
9. Display: ≥ 1080p for < 17 in; ≥ 2160p for ≥ 17.3 in

### Used

1. CPU: ≥ 2C/4T. Must be covered by Intel speculative execution security patches 
2. RAM: Max supported RAM ≥ 8 GB
3. USB: ≥ USB 2.0
4. Storage: Available port for SATA SSD
5. GPU/video out: ≥ HDMI
6. Display: ≥ 768p
7. LAN: ≥ 1000BASE-T Ethernet

# Docks

## USB 3.1 Gen 1+

[StarTech HDD Docking Stations](https://www.startech.com/HDD/Docking/?filter_IOINTERFACE=USB+3.1+Gen+2)

# NAS

## Raspberry Pi

[Penta SATA HAT](https://wiki.radxa.com/Penta_SATA_HAT)

# Networking

## Wireless 

### Access Points

If you don't absolutely need an AP right now, wait for Ubiquity UniFi Wi-Fi 6 APs before buying. Also, bear in mind you'll need UniFi Controller for all of the following. If you want to run Controller on standalone hardware, I recommend Debian 10 on a [used PC](https://github.com/jdrch/Hardware#what-are-the-minimum-specs-you-recommend-for-any-used-pc) or Raspbian on a Raspberry Pi 4. 

In order of increasing performance and client density:

* [Ubiquiti UniFi AP HD](https://www.ubnt.com/downloads/datasheets/unifi/UniFi_UAP-AC-HD_DS.pdf)
* [Ubiquiti UniFi AP SHD](https://dl.ubnt.com/datasheets/unifi/UniFi_UAP-AC-SHD_DS.pdf)
* [Ubiquiti UniFi AP XG](https://dl.ubnt.com/datasheets/unifi/UniFi_XG_AP_DS.pdf)

# Storage

## Tape

### LTO-8

#### Drives

##### Internal

[Quantum LTO Drives](https://iq.quantum.com/exLink.asp?10444458OP44N16I37407297&view=1)
* TC-L82AN-EY
* TC-L82AN-BR

## HDDs

Generally speaking, all HDDs that lack a workload rating have the same reliability. The only 2.5 in HDDs with workload ratings are ≥ 15 mm thick, which means they consume (nearly) as much space as a 3.5 in HDD. Also, I have no experience with the former. Ergo, they are omitted here.

Western Digital's UltraStar DC HC550 *should* be recommendable, but it [lacks a spec sheet](https://www.reddit.com/r/hardware/comments/e0bkwe/no_datasheets_and_contradictory_product_brochures/).

### 3.5 in

* [Seagate Exos X Enterprise Hard Drives](https://www.seagate.com/enterprise-storage/exos-drives/exos-x-drives/)
* Toshiba Enterprise Capacity Hard Drive – MG Series
  * [US product page](https://toshiba.semicon-storage.com/us/product/storage-products/enterprise-hdd.html) (Limited US availability, especially for higher end models) 
  * [EMEA product page](https://www.toshiba-storage.com/products/enterprise-capacity-hard-drive-mg-series/) with comprehensive [PDF spec sheet](https://www.toshiba-storage.com/wp-content/uploads/2019/09/TOSH_DS_MG_Series_print.pdf)
* [WD Gold Enterprise Class SATA HDD](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/product/internal-drives/wd-gold/product-brief-wd-gold-2579-810192.pdf)

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

# UPS

## Sine Wave

* CyberPower
  * [PFC Sinewave](https://www.cyberpowersystems.com/products/ups/pfc-sinewave/)
  * [New SmartApp Sinewave](https://www.cyberpowersystems.com/products/ups/new-smart-app-sinewave/)
* APC
  * [Back UPS PRO BR SineWave](https://www.apc.com/shop/us/en/categories/power/uninterruptible-power-supply-ups-/computer-and-peripheral/back-ups-pro/N-1itz49c) (search that page for "SineWave" as APC doesn't breakout sine wave UPS units)
* [Tripp-Lite](https://www.tripplite.com/products/ups-battery-backup~11) (search that page for "Sine" as Tripp-Lite doesn't breakout sine wave units)