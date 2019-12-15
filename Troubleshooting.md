# `Ásbrú Connection Manager`

## Asbru gets stuck on "Status: PASSWORD:Sent (not shown)" during SSH to OpenIndiana Hipster machine](https://github.com/asbru-cm/asbru-cm/issues/311)

[Solution](https://github.com/asbru-cm/asbru-cm/issues/311#issuecomment-565765693)

# Bash

## How to recover a broken terminal

* Copy `/etc/skel/.bashrc` to `~` folder

OR

* If using `bash-it`, delete the existing `.bashrc` file in `~` and rename the `.bashrc.bak` file to `.bashrc`

# `dd`

## Resolving the `Operation not permitted` error message

1. In a terminal, enter `mount` to list all mounted filesystems
2. Unmount all file systems on the physical device `dd` is to be run on
3. If the above don't work, create an appropriate (based on target OS) partition table for the USB stick in GParted

# Debian 10.x

## Cannot login via lock screen after monitor disconnect/reconnect while screen is locked

The only way around this is to [reboot the machine](https://www.reddit.com/r/debian/comments/e1mmr2/kde_on_debian_102_dual_hdmi_vga_monitors_can_no/f8rjou5/).

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

# GhostBSD

## MATE clock is very wrong, no obvious way to force NTP update

Run `sudo service ntpdate restart` in the terminal. The [command might hang](https://issues.ghostbsd.org/issues/125); if that happens, wait for the MATE clock to update (might be able to force this by locking the display) and then close the terminal window.

# Illumos

## OpenIndiana

### Bash-it shows up just fine in MATE terminal but not over SSH unless you `su` into root

* [Add this](https://www.reddit.com/r/illumos/comments/e531pq/openindiana_hipster_201910_bashit_shows_up_just/f9lpmnj/) under the 1st block of comments in `~/.profile`:

```
# if running bash
if [ -n "$BASH_VERSION" ]; then
    # include .bashrc if it exists
    if [ -f "$HOME/.bashrc" ]; then
    . "$HOME/.bashrc"
    fi
fi
```
* Log out and log in again. `bash-it` should show up correctly

# Microsoft Windows 10

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

## Windows Update

### Fails with error [0xC1900101](https://support.microsoft.com/en-us/help/10587/windows-10-get-help-with-upgrade-installation-errors)

* Click **Start**
* Search for "features"
* Click on **Turn Windows features on or off**
* In the ensuing list, uncheck **Windows Subsystem for Linux**
* Reboot
* [Clean boot Windows](https://support.microsoft.com/en-us/help/929135/how-to-perform-a-clean-boot-in-windows)
* Go to Windows Update and re(download + install) the update

# MobaXterm

## Updating between Preview Edition versions

* Run the installer 3 times to complete the installation
* Do not delete the associated .dat file that comes with the installer until after the installation is complete

# `ntp`

## `dnscrypt-proxy`, etc. failing due to wrong time

* https://www.reddit.com/r/raspberry_pi/comments/ae00gz/psa_if_you_run_pihole_or_dnscryptproxy_on_a_pi/?utm_medium=android_app&utm_source=share
* https://github.com/DNSCrypt/dnscrypt-proxy/issues/1081

# Pi-hole

## Excessive DNS queries from clients

On problematic clients, check for:

* [TCP port exhaustion](https://www.reddit.com/r/pihole/comments/c2r6vc/anyone_else_seen_client_behavior_like_this_3m_dns/erm5ter/)
* [Rogue services](https://www.reddit.com/r/pihole/comments/e2x046/excessive_requests_to_wwwmsftncsicom_from_a/f9hc83v/)