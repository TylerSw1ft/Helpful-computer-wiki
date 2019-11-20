# Scripted Method

1. Save this [script](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Updates) to `/opt/dnscrypt-proxy/dnscrypt-proxy-update.sh`
2. Make the script executable by running `chmod +x /opt/dnscrypt-proxy/dnscrypt-proxy-update.sh`
3. Execute the script by running `sudo ./dnscrypt-proxy-update.sh` in `/opt/dnscrypt-proxy/`

# Automatic Method

1. Complete **Scripted Method** steps above to set up the script and ensure it works on your system
2. Open the crontab editor with `sudo crontab -e`
3. In the crontab editor that pops up, append a descriptive comment describing the entry, e.g. `# Daily dnscrypt-proxy update`
4. Add a crontab entry that performs the update on the desired schedule, e.g. `@daily /opt/dnscrypt-proxy/dnscrypt-proxy-update.sh`. See [crontab syntax](https://github.com/jdrch/Hardware/wiki/Useful-Links#cron) for more scheduling options
5. Hit **Ctrl O** to save your changes
6. Hit **Enter**
7. Hit **Ctrl X** to exit the crontab editor

# Manual Method

1. Start your preferred GUI file manager with `sudo`, e.g. `sudo krusader` on Debian or `sudo pcmanfm` on Raspbian.
2. Download the new version's `linux_Platform-VersionNumber.tar.gz` archive
3. Extract the archive
4. Use the GUI file manager to transfer the extracted files to `/opt`
5. Copy the current dnscrypt-proxy folder into an \*`-old` folder
6. Navigate to `/opt` in the terminal using `cd /opt/dnscrypt-proxy`
7. Stop the `dnscrypt-proxy` service in the terminal using `sudo ./dnscrypt-proxy -service stop`
8. Use the GUI file manager to transfer the new files to to the `dnscrypt-proxy` folder
9. Start the `dnscrypt-proxy` service in the terminal using `sudo ./dnscrypt-proxy -service start`
10. If everything is working, delete the \*`-old` and extracted tar.gz folders

Source:
https://www.reddit.com/r/dnscrypt/comments/9ypenw/how_does_one_update_dnscryptproxy_to_a_new/ea48wkh/