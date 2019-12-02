1. Update the PC's BIOS to the latest version. Dell instructions are [here](https://github.com/jdrch/Hardware/wiki/Useful-Links#bios-updates-using-a-usb-stick)
2. Download the OpenIndiana Live USB
3. Write the OpenIndiana Live USB to disk (add link to Gparted USB disk formatting instructions) using:
   `dd if=OpenIndianaLiveUSBFile of=/dev/USBDiskIdentifier`
4. Enter the PC's BIOS
5. Set boot mode to UEFI
6. Exit PC's BIOS. This should cause the PC to automatically restart. If it doesn't, manually restart it
7. Press the required boot menu hotkey when the OEM logo appears onscreen. This hotkey is F12 for the Dell OptiPlex 390 MT
8. Select the USB entry under the UEFI heading
9. Hit **Enter**
10. When the OpenIndiana boot menu appears, hit **5**. All the options are explained [here](http://docs.openindiana.org/handbook/getting-started/)
11. In the following menu, set `ACPI` and `Verbose` to `On`
12. Hit *1* to return to the previous menu
13. Hit **6** to `ChainLoad disk`*n*, where *n* is a whole number. This should cause the graphical live environment to boot
14. When the live enviroment boots, double-click **Install OpenIndiana**
15. When the installation is complete, reboot as suggested, while holding down the PC OEM's BIOS hotkey. This hotkey is F2 for the Dell OptiPlex 390 MT
16. Set the boot mode back to Legacy
17. In the Legacy boot mode list, move the disk to which OpenIndiana is installed to the top
18. Exit the BIOS. The new OpenIndiana installation should now booth just fine
