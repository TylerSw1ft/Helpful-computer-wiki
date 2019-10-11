Note: This method should be generalizable to other array and filesystem types. The general method is:

1. Calculate the number of data loss drive destruction combinations for a given number of destroyed drives
2. Calculate the number of non-data loss drive destruction combinations for a given number of destroyed drives
3. Sum the above
4. Divide 1) by 3)

# Problem Statement

Consider a ZFS array with a given redundancy level, *r*. Assume a physical attacker with no knowledge of the array's configuration destroys *r* + 1 (the minimum number of destroyed drives necessary to result in data loss) drives. What is the probability *P* that said destruction actually results in data loss?

# Independence of Problem from Drive Specs and Reliability

Because the drives are being deliberately and randomly destroyed, this calculation is completely independent of drive specs and reliability data. For example, a drive's AFR has no effect on whether it is destroyed when tossed into a shredder. 

For a thorough discussion on array reliability based on drive specs and reliability, see [*High Availability and Disaster Recovery, Concepts, Design, Implementation*](https://www.springer.com/us/book/9783540244608) by Klaus Schmidt.

# Background

ZFS arrays stripe data across vdevs at the top level, with no parity. This means the loss of a single vdev in a ZFS array results in data loss. 

It is possible for a ZFS array to lose more than *r* + 1 drives without suffering data loss. Consider, for example, an array containing 2 x 4 HDD RAIDZ2 vdevs. The redundancy is given by the "2", meaning that each vdev can lose 2 HDDs without suffering data loss. If *either* vdev by itself loses 3 or more HDDs, though, the array suffers data loss. Ergo *r* + 1 in this case is 2 + 1 = 3. 

However, what if both vdevs lose 2 HDDs each, for a total of 4 HDDs? Because neither vdev has exceeded its redundancy, neither would suffer data loss.

# Solution Method

Clearly, the aforesaid is a probability problem. What might not be immediately obvious, though, is that it's also a combinations problem. For a quick primer on this, see the **Combinations** heading [here](https://www.mathsisfun.com/combinatorics/combinations-permutations.html). 

The key equation to keep in mind here is the one that gives the number of unique *combinations* (read: order doesn't matter, no repetition) in which *r* items can be chosen from a larger set of *n* items:

Eq. 1: *n*!/(*r*!(*n* - *r*)!)

The second equation to keep in mind is the one that gives the number of *permutations* in which *r* items can be chosen from a larger set of *n* items:

Eq. 2: *n*!/(*n* - *r*)!

2 array types are considered, those containing *only*: 

* RAIDZ*r*
* mirror

vdevs.

The following variables are defined:

* *F*, the *minimum* number of destroyed drives necessary for data loss
  * *F* = 2 for all ZFS arrays containing mirrors
  * *F* = *r* + 1 for ZFS array containing RAIDZ*r* vdevs only

*N*, the total number of drives the array has before any drive destruction

*V*, the total number of vdevs

*D*, the number of drives per vdev = *N*/*V*

*L*, the total number of combinations of *F* destroyed drives that result in data loss

*I*, the total number of combinations of *F* destroyed drives that do not result in data loss

*C*, *L* + *I*

*P*, *L*/*C*

# RAIDZ*r*, where 0 < *r* < 3

## Calculating *L*

Data loss occurs whenever *F* drives are destroyed per vdev. Combinatorically, this is the same as picking any 3 drives from a vdev. The number of such combinations *per vdev* is therefore:

*D*!/(*F*!(*D* - *F*)!)

However, because this can be done for each vdev *and* only needs to happen to 1 vdev for data loss to occur, the above expression must be multiplied by *V*, such that:

*L* = *V*(*D*!/(*F*!(*D* - *F*)!))

## Calculating *I*

Data loss does *not* occur when less than *F* drives are destroyed per vdev.

Assume 1 drive is picked from the first vdev and the remaining *F* - 1 = *r* drives are picked from the remaining vdevs. From *D*, pick *r* drives:

*D*!/(*r*!(*D* - *r*)!)

Because that combination occurs for every drive in *D*, and for every multiply by *D*:

*D*(*D*!/(*r*!(*D* - *r*)!))

Because the above combination occurs for every permutation of 2 vdevs, multiply by that factor:

(*V*!/(*V* - 2)!)*D*(*D*!/(*r*!(*D* - *r*)!))

### For *V* ≥ 3

For this value of V, 1 drive can fail from each vdev. The number of tuples consisting of 1 drive from each vdev is:

*D*^*F*

This can be done for any 3 vdevs in the array, so multiply by that combination:

(*V*!/(3!(*V* - 3!))*D*^*F*

Putting all of the above together:

*I* = (*V*!/(*V* - 2)!)*D*(*D*!/(*r*!(*D* - *r*)!)) + (*V*!/(3!(*V* - 3!))*D*^*F*
