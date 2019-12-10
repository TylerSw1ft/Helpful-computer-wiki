# Core backup principles

* Prepare to permanently lose anything that isn't backed up. I prefer this to "back *everything* up," as some things aren't worth the efort
* Where possible, use hardware you already have. Not only is this less expensive, at least you already know it works
* Put the largest storage devices on backup duty. This ensure you'll always have enough backup space
* New incoming critical data - especially hardcopy - must be backed up ASAP
* [Run compute and backup on separate storage devices](https://github.com/jdrch/Hardware/wiki/Why-You-Should-Separate-Compute-and-Backup-Workloads)
* All PCs must have the following levels of backup (note that for some OSes a single solution covers more than 1 of the below):
  * Critical change OS rollback
  * At least daily filesystem snapshots
  * At least weekly device-level recovery backups
* All devices must have one of the following:
  * Folders that real-time sync among all the other devices
  * R/W network access to the real-time sync folders of another device
* All backups must be automated

# Details

I run all 4 major OS paradigms (officially the excuse for this is "just in case 2 of them get compromised," but the real reason is I love computers 🤷‍♂️) and want to back all of them up at multiple levels (device, irreplaceable user data, operating system.)

This requires multiple solutions, and I was getting confused keeping all of them in my head. Excel to the rescue! Here's my current blueprint and progress status (I'm continuously updating this as I tweak my plans, notation, and actually get solutions implemented):

![](https://raw.githubusercontent.com/jdrch/Hardware/master/BackupTable.png)

I also have target dates to keep myself on track. The object here is ultimately turn the entire top table green.

The point of this is to help myself (and others who might want to use the same method) to see:

* Which systems have which level(s) of backup coverage
* Which systems still need which level(s) of backup coverage
* Which solution should be implemented next

&#x200B;

***FAQ:***

**There's no mention of any hardware?**

To keep the spreadsheet manageable, there isn't. However, I'm building a list of all my gear [here](https://github.com/jdrch/Hardware).

**This looks expensive**

The most expensive part has been the HDDs. The only paid software products in the list are Office 356 and Resilio Sync, and I have a lifetime free license from helping the latter beta test back in the day. 3 of the listed PCs are castoffs and I have another Craigslist one waiting in the wings, possibly for Bacula or pfSense purposes, whichever duty calls first.

**Why not stick on one data integrity filesystem?**

Because I want to try the 3 major ones for myself.

**Why are there no offsite** ***device*** **backups? (There are offsite user data backups, see the column dedicated to them)**

Any event that can take out both my devices and their backups onsite will also sufficiently damage those devices to warrant total replacement thereof. I don't have identical spare devices in reserve. Ergo, offsite device backups are pointless for me. The other problems are my 2 TB ISP data cap and the fact that device backups would consume more than one HDD, making the whole process manual, prone to error, irregular, and poorly scaling.

**Why are there so many different solutions?**

I prefer to use the easiest, officially supported solution that gives me what I want for each platform. Clearly, which solution that is will differ among platforms.

**Which solution would you use, if you were to pick one?**

My favorite is Veeam. I'd use it for everything in the Device Bare Metal columns, but it doesn't support Raspbian on armhf or FreeBSD :'(