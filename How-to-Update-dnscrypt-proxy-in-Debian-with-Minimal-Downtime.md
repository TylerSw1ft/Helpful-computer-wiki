1. Start your preferred GUI file manager with `sudo`, e.g. `sudo krusader` on Debian or `sudo pcmanfm` on Raspbian.
2. Download the new version's `linux_Platform-VersionNumber.tar.gz` archive
3. Use the GUI file manager to transfer it to `/opt`
4. Copy the current dnscrypt-proxy folder into an \*`-old` folder
5. Navigate to `/opt` in the terminal using `cd /opt/dnscrypt-proxy`
6. Stop the `dnscrypt-proxy` service in the terminal using `sudo ./dnscrypt-proxy -service stop`
7. Use the GUI file manager to transfer the new files to to the `dnscrypt-proxy` folder
8. Start the `dnscrypt-proxy` service in the terminal using `sudo ./dnscrypt-proxy -service start`
9. If everything is working, delete the \*`-old` and extracted tar.gz folders

Source:
https://www.reddit.com/r/dnscrypt/comments/9ypenw/how_does_one_update_dnscryptproxy_to_a_new/ea48wkh/