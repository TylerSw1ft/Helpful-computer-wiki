# POSIX

There is a family of standards called [POSIX](https://en.wikipedia.org/wiki/POSIX). It isn't necessary to know what POSIX is to understand the above relationships, just that it exists.

# Certified POSIX-compliant OSes

## UNIX

A UNIX is any operating system that has been certified as POSIX-compliant. macOS is a UNIX.

# Non-certified, but "mostly POSIX-compliant" OSes

All the OSes in this category are basically open source UNIX implementations. The main differences are implementation method and license.

## BSD

1. Each BSD uses an independently developed kernel
2. There is no (guaranteed) binary compatibility among BSDs
3. Uses the [BSD License](https://en.wikipedia.org/wiki/BSD_licenses)

## Linux Distributions (Distros)

1. Each distro uses the centrally developed Linux kernel
2. While each distro *may* modify the kernel for its own purposes, there is:
  a. Binary compatibility among Linux distros on the same CPU architecture
  b. Feature parity among all kernels based on the same release
3. Uses the [GNU General Public License (GPL)](https://en.wikipedia.org/wiki/GNU_General_Public_License)

# Notes

The differences between the BSD License and the GPL, while outside the scope of this comparison, are [significant](https://fossbytes.com/open-sources-license-type/).