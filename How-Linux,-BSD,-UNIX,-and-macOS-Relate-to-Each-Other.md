![](https://raw.githubusercontent.com/jdrch/Hardware/97c6fa9c202fbc4c46794186b77ec966eb329f94/UNIX%20Comparison.png)

# POSIX

There is a family of computing standards trademarked as [POSIX](https://en.wikipedia.org/wiki/POSIX). The POSIX trademark is [owned by IEEE](http://get.posixcertified.ieee.org/).

An OS that uses the POSIX trademark must:

1. [Be certified to meet all POSIX conformance requirements](http://get.posixcertified.ieee.org/certification_guide.html#Certification)
2. [Have a POSIX Trademark License Agreement](http://get.posixcertified.ieee.org/certification_guide.html#TheFirstStepTheTMLA)

# Certified POSIX-compliant OSes

## UNIX

UNIX's requirements are a [superset of POSIX's](https://unix.stackexchange.com/a/14369/166524). In other words, all UNIX OSes are POSIX-compliant OSes, but not all POSIX-compliant OSes are UNIX OSes. The UNIX trademark is owned by [The Open Group](https://www.opengroup.org/).

A UNIX is [any operating system](https://www.opengroup.org/membership/forums/platform/unix):

1. That passes the applicable UNIX certification test suites 
2. Whose supplier has formally agreed to the terms of the UNIX Certification Program

### macOS

MacOS is a mixed source UNIX OS.

# Non-certified, but "mostly POSIX-compliant" OSes

## Current Generation (Free/DragonFly /Net/Open)BSDs

1. Each use an independently developed kernel
2. Have no aim for binary compatibility among themselves
3. Use the [BSD License](https://en.wikipedia.org/wiki/BSD_licenses)

## Linux Distributions (Distros)

1. Each use the centrally developed Linux kernel
2. *May* modify the kernel for their own purposes, but there is, by virtue of the common kernel:
   1. Binary (*not* necessarily package) compatibility among Linux distros on the same CPU architecture
   2. The features of each kernel are a superset of the features of the mainline Linux kernel of the same release version
3. Each use the [GNU General Public License (GPL)](https://en.wikipedia.org/wiki/GNU_General_Public_License) for the kernel at the very least

# Notes

* The differences between the BSD License and the GPL, while outside the scope of this comparison, are [significant](https://fossbytes.com/open-sources-license-type/)
* Licensing and certification fees for both [POSIX](http://get.posixcertified.ieee.org/docs/posix-fee-schedule-1.3.PDF) and [UNIX](https://www.opengroup.org/openbrand/Brandfees.htm) are expensive relative to open source OS budgets. This appears to be the main reason BSD and Linux are neither certified nor licensed
* POSIX certification appears to involve an [audited self-test](http://get.posixcertified.ieee.org/certification_guide.html#Formal%20Testing), using a standardized testing suite supplied by the IEEE
* UNIX certification appears to involve [approved results self-testing](https://www.opengroup.org/openbrand/docs/faq.html#general21), using [standardized testing suites]9https://www.opengroup.org/openbrand/testing/prodstds.htm) supplied by The Open Group
* There is at least 1 other standard that exists within the Linux ecosystem only: the [Filesystem Hierarchy Standard](https://refspecs.linuxfoundation.org/fhs.shtml)
* The Open Group maintains a [list](https://www.opengroup.org/openbrand/register/) of OSes that have been certified to UNIX standards