# PSA: The lack of Resilio Sync and web administration support for OpenIndiana puts this project in a very doubtful state. I'm not sure working around those gaps is worth the effort.

# Documentation

http://docs.openindiana.org/

# Prerequisites

## Storage

### Boot/OS & `/home`

Crucial MX500 [1 TB](https://www.crucial.com/usa/en/ct1000mx500ssd1) or [2 TB](https://www.crucial.com/usa/en/ct2000mx500ssd1) SATA 2.5" 7mm Internal SSD

### Backup

Consumer HDD for `zfs send` backup from boot SSD
# Synced Folder Access

OpenIndiana does not have a Resilio Sync build, therefore might have to mount shared NFS folders from [Debian 10 machine](https://github.com/jdrch/Hardware/blob/master/Dell%20OptiPlex%20390-1%20SFF.md)