# Dell XPS 8500 Special Edition

## Won't Boot After Windows 10 Update

* Turn off PC
* Disconnect all cables
* Press the power button for 30 seconds
* Open the case
* Disconnect all drives except the boot drive
* Remove all PCIe cards
* Remove and reseat motherboard CMOS battery
* Connect external monitor to onboard HDMI port
* Turn on PC

It should now boot.

## Bluetooth keeps turning off

* Search from the Start menu and run **Find and fix problems with Bluetooth devices**
* Open **Device Manager**
* Expand **Bluetooth**
* Right-click on the wireless NIC
* Click **Properties**
* Click the **Power Management** tab
* Ensure **Allow the computer to turn off this device to save power** is unchecked

# Windows 10

## File Explorer

### Loads thumbnails slowly or not at all, gets stuck on **Working On It**

* Open **Indexing Options** in the **Control Panel**
* Click **Show all locations**
* Click **Modify**
* Uncheck everything
* Check your user folder
* Check all folders in which you keep personal files and media
* Click **OK**
* Reboot the PC