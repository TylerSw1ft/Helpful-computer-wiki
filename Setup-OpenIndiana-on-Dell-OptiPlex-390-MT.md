# PSA: The lack of Resilio Sync and web administration support for OpenIndiana puts this project in a very doubtful state. I'm not sure working around those gaps is worth the effort.

# Documentation

http://docs.openindiana.org/

# Prerequisites

## Storage

### Boot/OS & `/home`

Crucial MX500 [1 TB](https://www.crucial.com/usa/en/ct1000mx500ssd1) or [2 TB](https://www.crucial.com/usa/en/ct2000mx500ssd1) SATA 2.5" 7mm Internal SSD

### Backup

Consumer HDD for `zfs send` backup from boot SSD

### RAM

16 GB ([G.SKILL F3-1600C11D-16GNT](http://www.gskill.com/product/165/186/1532584719/F3-1600C11D-16GNTValueDDR3-1600MHz-CL11-11-11-1.50V16GB-(2x8GB)))

# Synced Folder Access

OpenIndiana does not have a Resilio Sync build, therefore might have to mount shared NFS folders from [Debian 10 machine](https://github.com/jdrch/Hardware/blob/master/Dell%20OptiPlex%20390-1%20SFF.md)