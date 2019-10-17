**Preamble:** This is about general principles that help you build a very efficient, customized solution for yourself, as opposed to cribbing some setup that might not work well for you. If you want to use a parts list written by someone who doesn't know your needs, that's fine. This is about starting with *YOUR* needs and working backwards logically to arrive at a solution that's *tailored specifically* to them. 

Also, this method allows you to build affordable solutions from brand new parts instead of scrounging on Ebay.

It's all about teaching people to fish ... anyway lets get started.

I've seen a lot of posts lately asking about server builds, so I figured I'd chime in. This post will NOT talk about actually building the server, which is actually the same as building a PC (see r/buildapc.) This post WILL help you come up with a parts list, though. 

Also, it's for dumb (read: not necessarily high compute capable) *storage*/*backup* servers, preferably running some kind of resilient file system such as ZFS, Btrfs, or ReFS + SS that doesn't need its own controller card. No consideration will be given to CPU Plex transcoding; get a Plex Pass and use a GPU for that if you're really serious about it. Or set your client devices and network up to receive pass-through (unmodified, nontranscoded) streams.

**IMPORTANT: If you're building a compute server, modify the instructions below by choosing the CPU 1st, then storage needs 2nd, then case that matches both, then motherboard.**

Ready? Let's go!

Overarching principle: **When building a server, start from your needs and work backwards. DO NOT TRY TO START WITH A PARTICULAR PART AND WORK FORWARD, YOU WILL GET LOST AND CONFUSED.**

To search for parts: NewEgg (this isn't an ad; you don't need to buy from them. I just haven't found anywhere else that's as good for spec-based searches as they are)

To build and save a parts list: PCPartPicker

1. How much data do you need to store/backup? If you don't know offhand, it's equal to the sum of entire installed storage on devices that are being backed up at the device level + any additional folder/filesystem backups. 
2. How much usable space do you need? "Usable space" here refers to the maximum amount of data that can be written to the storage. For headroom, I recommend that usable space be at least twice the *initial* amount of data you need to store/backup
3. Which redundancy type (e.g. parity or mirror) do you want? Ensure you understand the meaning of those 2 terms for your preferred filesytem. In a very general sense parity requires at least 3 HDDs with the largest HDD (or 2) being the parity drive(s), while mirroring requires total raw storage (total raw HDD capacity) to be at least twice your desired usable space
4. How many (SAS or SATA) HDDs do you need for 1) to 3)? Note that there may be many combinations of drive sizes that are mathematically correct answers to this question. Personally, because ports and case/chassis space tend to be limiting factors, I advise you buy the largest capacity (enterprise, for workload rating and piece of mind) HDDs you can afford. As far as HDDs go your options are (in no implied order) Seagate, Western Digital (into whom HGST has been absorbed,) and Toshiba. Each HDD OEM's site is simple enough to navigate to find specs. Spreadsheets are your friend here
5. How much physical, Euclidean space do you have for a server?
6. Which chassis/case that fits in 5) can hold the number of HDDs in 4)?
7. What do you want your boot media to be (e.g. M.2 NVMe (strongly suggested), SATA, USB stick, etc.)?
8. Which motherboards with at least onboard gigabit Ethernet support 4), 6), & 7)? If the motherboard you want doesn't have enough SATA or SAS slots, which HBA card works with the motherboard and supports 3) & 4)? Note that some motherboards disable PCIe slot(s) if an NVMe drive is installed. To keep things simple, just select only motherboards that come with the number of slots you need. You can also add criteria such as faster Ethernet or specific USB version ports if you prefer
9. Which CPUs with at least 4C/8T support the motherboard in 8)?
10. How much RAM do you need?
11. Which RAM supports the motherboard in 8) & the CPU in 9)?
12. Do you need a GPU? Which GPU supports the motherboard in 8)?
13. How much power does all the above use (PCPartPicker will automatically calculate this for you)?
14. Which PSU supports the power draw in 13)?
15. Choose your desired filesystem. Yes, you can leave this for next to last because of the general principles in 3)
16. Choose the OS that best supports the filesystem in 15), the boot media in 7), and the GPU in 12) while giving you other features you want. Check the system requirements, but the vast majority of modern OSes support any x86 CPU and motherboard and onboard LAN NIC and HDDs you throw at them so that's a minor worry

If you want a value for money solution, select the lowest cost option with at least a 4 star rating at each step. Also, if you live in the US, do not pay for upgraded shipping. Plan ahead and do other things while your parts arrive (many will arrive in a couple days anyway, especially if you're in a large metro.) 

And that's it. Now, I will caution that PCPartPicker excludes a lot of actual server chassis and motherboards. You can find those motherboards at NewEgg and [Supermicro](https://www.supermicro.com/en/products/motherboards) (best for large SATA/SAS port counts.) You can look at [this post](https://www.reddit.com/r/servers/comments/cgiwbi/what_are_wellknown_server_chassis_oems_which/) for a list of chassis OEMs. 

Put all the parts together and build.

Original comment and thread that inspired this is [here](https://www.reddit.com/r/homelab/comments/cn9lf8/how_to_build_a_server/ewcn7zz/).

Source: https://www.reddit.com/r/DataHoarder/comments/cp86qt/how_to_come_up_with_an_affordable_servernas_parts/