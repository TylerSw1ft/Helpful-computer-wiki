NAS as primary storage is something I advise against. If you're gonna do that, build a full-on server with the CPU horsepower for future role expansion. NAS is best at literally just being a dumb(ish, as in CPU, sufficient RAM to manage the filesystem, a NIC at least as fast as your network max, and nothing else), low spec, high storage capacity *backup* node. In other words, its sole job should be to hoard data *of which another copy exists*, and nothing else. Once you use it as primary storage you start running into CPU demands for transcoding and the like and by the time you take care of that you have a server on your hands and you'll *STILL* need to build a backup solution. 

The other issue is combining primary storage and backup on the same HDDs greatly increases the workload of those drives.

So just build the server in the 1st place if that's what you're going for *OR* use an existing high spec PC as your primary data storage and have the NAS back that up. You don't have to build a NAS to get network file sharing capabilities; even a Windows 10 Home PC will serve and transcode files just fine with the right specs.

Source:
https://www.reddit.com/r/DataHoarder/comments/bval61/nas_drive_prices_google_sheet/epnhsgu/