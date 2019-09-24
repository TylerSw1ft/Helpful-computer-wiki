The following uses the Toshiba L200 has an example, but can be adapted to any HDD.

I have a Btrfs RAID1 (data and metadata) filesystem on 2 x 2 TB Toshiba L200s as a backup target for some ~, ext4 LVM located, non-database use folders. 

I was trying to figure out how often I can scrub the L200 array without exceeding the component HDDs' annual workload rating; however the latter is nowhere to be found in the HDD's [datasheet](https://www.toshiba-storage.com/products/toshiba-internal-hard-drives-l200/?pdf) (PDF warning). FWIW, no drive in the 2.5" consumer class has published workload ratings: I checked WD Blue & Black as well as Seagate. 

NOTE: 

* Many of the inputs are estimates/informed guesses. You're free to make your own
* The calculations are conservative, meaning they err on the side of preserving HDD life
* The biggest single component of workload will be the scrub operation, which reads all the data stored on each drive (but NOT the entire drive)
* The all caps function names in the code snippets are Excel functions
* The scrub time will need to be recomputed as the source dataset size grows
* Variable names are CamelCase
* This method can be use for other brands and models, not just Toshiba. It can also be used for drives with known workload ratings
* The base unit of time we'll use is 1 week (7 days), but you can use a different one using the method described in STEP 1 below
* This may sound like overkill, but I like applied math and figured it would be an interesting exercise ;)
* I'm using consumer 2.5" HDDs because that's the largest physical form factor that allows me to fit 2 + the source SSD inside the PC. I'd much rather be using enterprise HDDs with specified workload ratings, but alas
* This method applies to any RAIDed backup targeted by an incremental backup method
* This method does not account for read/write resulting from snapshot pruning; hopefully the conservatism built into the calculations covers that

**STEP 0: Compute source dataset size**

This is approximately 0.5 TB, represented by `SourceDatasetSize`

**STEP 1: Estimate the annual workload rating**

Based on the datasheets I've seen, Toshiba HDDs have 3 annual workload tiers: [Unlimited](https://www.toshiba-storage.com/products/enterprise-performance-hard-drive-al-series/), [550 TB](https://www.toshiba-storage.com/products/enterprise-capacity-hard-drive-mg-series/), [180 TB, 72 TB](https://www.amazon.com/Toshiba-HDWJ110XZSTA-Mobile-5400rpm-Internal/dp/B013JPLM68), and unrated. I assumed unrated is actually a lower number than 72, so I multiplied that number the average fraction of each tier over the next higher one:

`AnnualWorkloadRating=AVERAGE(550/infinity, 180/550, 72/180)*72`

This gives a very disappointing number of 17.45 TB. Remember, this is a very conservative estimate; it's basically the minimum I'd expect an L200 to handle. It may be a valid assumption to just used the lowest workload rating of 72 TB, given that the HDD it applies to [has only half the cache of the L200](https://www.toshiba-storage.com/products/v300/?pdf) (PDF warning), but I'll leave that up to you to decide.

**STEP 2: Compute weekly workload rating**

This is as simple as:

`WeeklyWorkloadRating=AnnualWorkloadRating/NumberOfTimeUnitsPerYear`

which, for weeks, boils down to:

`WeeklyWorkloadRating=AnnualWorkloadRating/52`

This is 0.335 TB for my case.

Note that you can adjust this calculation to a daily value (useful if you want to do multiple snapshots per day by dividing by 365 instead.) Similarly, you can compute monthly values by dividing by 12, etc.

Notice a serious problem here? 0.335 TB is less than `SourceDataSet`. As I said at the outset, this can be mitigated by decreasing the frequency of scrubs (read: scrubbing less often). To this end, let's define a variable, `MinimumWeeksBetweenScrubs`, to represent the smallest number of weeks between scrubs.

**STEP 3: Compute how much differential data in the source dataset needs to be backed up weekly**

This one was really difficult for me to figure out an estimate source for. Since most of my dataset comes from downloaded files, I decided to use my ISP's data usage meter. Based on a 3 month average (provided by ISP meter portal), I calculated my weekly data usage to be 0.056 TB, and therefore assumed `SourceDatasetSize` to change by that much (Clearly, this is an overestimate. You may want to try using DNS, traffic, or existing backup size logs to get a better number.) You can do the same via:

`WeeklySourceDatasetChange=AverageMonthlyDataUsage/WeeksPerMonth`

Which collapses to:

`WeeklySourceDatasetChange=AverageMonthlyDataUsage/4.33`

If you have other (heavy, streaming uses a lot of data so this is a reasonable assumption) users in the house, and only your data is being backed up, you can knock that number down some more by doing:

`WeeklySourceDatasetChange=AverageMonthlyDataUsage/NumberOfUsers/4.33`

**STEP 4: Compute how often you can scrub the backup dataset**

At the very least, we want the backup system to capture all the dataset changes in a week (or other preferred base time unit). So, we can say:

`WeeklySourceDatasetChange=WeeklyWorkloadRating-(SourceDatasetSize/MinimumWeeksBetweenScrubs)`

Solving the above for `MinimumWeeksBetweenScrubs`:

`MinimumWeeksBetweenScrubs=SourceDatasetSize/(WeeklyWorkloadRating-WeeklySourceDatasetChange)`

This is 1.79 weeks on my end, for a weekly source dataset change equal to what I download per week. Note that this latter value does *NOT* imply only 1 snapshot per week. Rather, it describes the maximum amount of changed data per week any amount of snapshots you decide on can cover without exceeding the drive's workload rating. 

The 1.79 weeks value is the smallest time period between scrubs for which dataset changes can be completely backed up without exceeding the HDD's workload rating.

PS: ZFS fans don't worry, I'm planning on building something similar for ZFS on a different machine eventually. I already have on-pool snapshots done on that PC, I just need to use syncoid to replicate them to a mirrored vdev array, probably consisting of the same HDDs(?) I may use Seagate Barracudas instead as their estimated workload in Step 1 might be higher.

Source: https://www.reddit.com/r/DataHoarder/comments/cjhwbo/method_to_determine_how_many_scrubs_hdds_without/