1. Update the PC's BIOS to the latest version. Dell instructions are [here](https://github.com/jdrch/Hardware/wiki/Useful-Links#bios-updates-using-a-usb-stick)
2. Download the OpenIndiana Live USB
3. Ensure the USB flash drive to be used is properly formatted by creating a new partition table corresponding to the OS you'll write the installation image from on the flash drive. Do this in GParted ([manual](https://gparted.org/display-doc.php?name=help-manual)) . **Write from Linux or BSD only** 
3. Write the OpenIndiana Live USB to disk using: `dd if=OpenIndianaLiveUSBFile of=/dev/USBDiskIdentifier`
4. Enter the PC's BIOS
5. Set boot mode to UEFI
6. Exit PC's BIOS. This should cause the PC to automatically restart. If it doesn't, manually restart it
7. Press the required boot menu hotkey when the OEM logo appears onscreen. This hotkey is F12 for the Dell OptiPlex 390 MT
8. Select the USB entry under the UEFI heading. This entry might also have an alphanumeric code
9. Hit **Enter**
10. When the OpenIndiana boot menu appears, hit **5**. All the options are explained [here](http://docs.openindiana.org/handbook/getting-started/)
11. In the following menu, set `ACPI` and `Verbose` to `On`
12. Hit **1** to return to the previous menu
13. Hit **6** to `ChainLoad disk`*n*, where *n* is a whole number. This should cause the graphical live environment to boot
14. When the live enviroment boots, double-click the **Install OpenIndiana** desktop shortcut
15. When the installation is complete, reboot as suggested, while pressing the PC OEM's BIOS hotkey. This hotkey is F2 for the Dell OptiPlex 390 MT
16. Set the boot mode back to Legacy
17. In the Legacy boot mode list, move the disk to which OpenIndiana is installed to the top
18. Save your changes and exit the BIOS. The new OpenIndiana installation should now boot just fine