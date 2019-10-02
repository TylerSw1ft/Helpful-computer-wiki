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

## BSD

1. Each BSD uses an independently developed kernel
2. There is no aim for binary compatibility among BSDs
3. Uses the [BSD License](https://en.wikipedia.org/wiki/BSD_licenses)

## Linux Distributions (Distros)

1. Each distro uses the centrally developed Linux kernel
2. While each distro *may* modify the kernel for its own purposes, there is, by virtue of the common kernel:
   1. Binary (*not* necessarily package) compatibility among Linux distros on the same CPU architecture
   2. Feature parity among all kernels based on the same release
3. Uses the [GNU General Public License (GPL)](https://en.wikipedia.org/wiki/GNU_General_Public_License)

# Notes

* The differences between the BSD License and the GPL, while outside the scope of this comparison, are [significant](https://fossbytes.com/open-sources-license-type/)
* Licensing and certification for both [POSIX](http://get.posixcertified.ieee.org/docs/posix-fee-schedule-1.3.PDF) and [UNIX](https://www.opengroup.org/openbrand/Brandfees.htm) are expensive relative to open source OS budgets, ergo BSD and Linux are neither certified nor licensed
* POSIX certification appears to involve an [audited self-test](http://get.posixcertified.ieee.org/certification_guide.html#Formal%20Testing), using a standardized testing suite developed by the IEEE