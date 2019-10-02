# POSIX

There is a family of computing standards trademarked as [POSIX](http://get.posixcertified.ieee.org/certification_guide.html). 

An OS that uses the POSIX trademark must:

1. [Be certified to meet all POSIX conformance requirements](meets all the conformance requirements)
2. [Have a POSIX Trademark License Agreement](http://get.posixcertified.ieee.org/certification_guide.html#TheFirstStepTheTMLA)

# Certified POSIX-compliant OSes

## UNIX

UNIX's requirements are a [superset of POSIX's](https://unix.stackexchange.com/a/14369/166524). In other words, all UNIX OSes are POSIX-compliant, but not all POSIX-compliant OSes are UNIX OSes.

A UNIX is [any operating system](https://www.opengroup.org/membership/forums/platform/unix):

1. That passes the applicable certification test suites 
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
* Both POSIX-certification and UNIX licensing are expensive relative to open source OS budgets, ergo BSD and Linux are neither certified nor licensed