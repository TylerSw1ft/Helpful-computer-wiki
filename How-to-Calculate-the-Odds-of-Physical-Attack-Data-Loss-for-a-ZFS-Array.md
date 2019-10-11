Note: this method should be generalizable to other array and filesystem types. The general method is:

1. Calculate the number of data loss drive destruction combinations for a given number of destroyed drives
2. Calculate the number of non-data loss drive destruction combinations for a given number of destroyed drives
3. Sum the above
4. Divide 1) by 3)

# Problem Statement

Consider a ZFS array with a given redundancy level, *x*. Assume a physical attacker with no knowledge of the array's configuration destroys *x* + 1 (the minimum number of destroyed drives necessary to result in data loss) drives. What is the probability that said destruction actually results in data loss?

# Independence of Problem from Drive Specs and Reliability

Because the drives are being deliberately and randomly destroyed, this calculation is completely independent of drive specs and reliability data. For example, a drive's AFR has no effect on whether it is destroyed when tossed into a shredder. 

For a thorough discussion on array reliability based on drive specs and reliability, see [*High Availability and Disaster Recovery, Concepts, Design, Implementation*](https://www.springer.com/us/book/9783540244608) by Klaus Schmidt.

# Background

It is possible for a ZFS array to lose more than *x* + 1 drives without suffering data loss. Consider, for example, an array containing 2 x 4 HDD RAIDZ2 vdevs. The redundancy is given by the "2", meaning that each vdev can lose 2 HDDs without suffering data loss. If either vdev loses 3 or more HDDs, though, the array suffers data loss. Ergo, *x* + 1, in this case is 3. 

However, what if both vdevs lose 2 HDDs each, for a total of 4 HDDs? Because neither vdev has exceeded its redundancy, neither would suffer data loss.

# Solution Method

Clearly, the aforesaid is a probability problem. What might not be immediately obvious, though, is that it's also a combinations problem. For a quick primer on this, The **Combinations** heading [here](https://www.mathsisfun.com/combinatorics/combinations-permutations.html). 

The key equation to keep in mind here is the one that gives the number of unique *combinations* (read: order doesn't matter, no repetition) in which *r* items can be chosen from a larger set of *n* items:

Eq. 1: *n*!/(*r*!(*n*-*r*)!)

