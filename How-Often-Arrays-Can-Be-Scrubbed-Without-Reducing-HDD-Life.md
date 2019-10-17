NOTE: 

* Most CoW filesystems either recommend monthly scrubs (ZFS, Btrfs) or perform monthly scrubs automatically (ReFS + Storage Spaces)
* Many of the inputs are estimates/informed guesses
* The calculations are conservative, meaning they err on the side of preserving HDD life
* The biggest single component of workload will be the scrub operation, which reads all the data stored on each drive (but NOT the entire drive)
* The all caps function names in the code snippets are Excel functions
* The scrub time will need to be recomputed as the source dataset size grows
* Variable names are CamelCase
* This method can be used for drives with known workload ratings
* The base unit of time used is 1 week (7 days), but a different one can be used via the method described in STEP 1 below
* This method applies to any redundant backup array targeted by an incremental backup method
* This method does not account for read/write resulting from snapshot pruning; hopefully the conservatism built into the calculations covers that

**STEP 0: Compute source dataset size**

This is `SourceDatasetSize`

**STEP 1: Estimate the annual workload rating**

If the HDD's workload rating is already known, skip to STEP 2.

The Toshiba L200 is used as an example. Based on datasheets, Toshiba HDDs have 3 annual workload tiers: [Unlimited](https://www.toshiba-storage.com/products/enterprise-performance-hard-drive-al-series/), [550 TB](https://www.toshiba-storage.com/products/enterprise-capacity-hard-drive-mg-series/), [180 TB, 72 TB](https://www.amazon.com/Toshiba-HDWJ110XZSTA-Mobile-5400rpm-Internal/dp/B013JPLM68), and unrated. Assuming "unrated" is a lower number than 72, multiply that number by the average fraction of each tier over the next higher one:

`AnnualWorkloadRating=AVERAGE(550/infinity, 180/550, 72/180)*72`

This is a very conservative estimate; it's basically the minimum the HDD can be expected to handle. It may be a valid assumption to use the lowest published workload rating of 72 TB, but that is left to the user to decide.

**STEP 2: Compute weekly workload rating**

This is as simple as:

`WeeklyWorkloadRating=AnnualWorkloadRating/NumberOfTimeUnitsPerYear`

which, for weeks, boils down to:

`WeeklyWorkloadRating=AnnualWorkloadRating/52`

This calculation can be adjusted to a daily value (useful for multiple snapshots per day) by dividing by 365 instead. Similarly, monthly values can be computed by dividing by 12, etc.

The variable `MinimumWeeksBetweenScrubs` is defined to represent the smallest number of weeks between scrubs.

**STEP 3: Compute how much differential data in the source dataset needs to be backed up weekly**

If most of the dataset comes from downloaded files, Use the ISP's data usage meter:

`WeeklySourceDatasetChange=AverageMonthlyDataUsage/WeeksPerMonth`

Which collapses to:

`WeeklySourceDatasetChange=AverageMonthlyDataUsage/4.33`

If there are other (heavy, streaming uses a lot of data so this is a reasonable assumption) users sharing the same connection, and only a single user's data is being backed up, that number can be further reduced by:

`WeeklySourceDatasetChange=AverageMonthlyDataUsage/NumberOfUsers/4.33`

**STEP 4: Compute how often the backup dataset can be scrubbed**

At the very least, the backup system should capture all the dataset changes in a week (or other preferred base time unit). So:

`WeeklySourceDatasetChange=WeeklyWorkloadRating-(SourceDatasetSize/MinimumWeeksBetweenScrubs)`

Solving the above for `MinimumWeeksBetweenScrubs`:

`MinimumWeeksBetweenScrubs=SourceDatasetSize/(WeeklyWorkloadRating-WeeklySourceDatasetChange)`

This latter value does *NOT* imply only 1 snapshot per week. Rather, it describes the maximum amount of changed data per week any number of snapshots decided on can cover without exceeding the drive's workload rating.

Source: https://www.reddit.com/r/DataHoarder/comments/cjhwbo/method_to_determine_how_many_scrubs_hdds_without/