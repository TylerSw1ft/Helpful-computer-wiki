# POSIX

There is a family of computing standards called [POSIX](https://en.wikipedia.org/wiki/POSIX).

# Certified POSIX-compliant OSes

## UNIX

A UNIX is any operating system that has been certified as POSIX-compliant. 

### macOS

MacOS is a UNIX.

# Non-certified, but "mostly POSIX-compliant" OSes

All the OSes in this category are basically open source UNIX implementations. The main differences are implementation method and license.

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

The differences between the BSD License and the GPL, while outside the scope of this comparison, are [significant](https://fossbytes.com/open-sources-license-type/).