# MulitLib-LFS
Linux from Scratch with MulitLib support and S6+S6-RC as init system

This is based on the work of Thomas' Multilib Linux From Scratch (https://www.linuxfromscratch.org/~thomas/multilib-m32), which now uses a different build method based on LFS versions newer than 9.0. That new build method does not work on musl libc based hosts.

The aim of this project is to create a unix-like system using Glibc with support for 32-bit and 64-bit x86 binaries. After completing a build, one may continue building with Gaming Linux From Scratch (https://www.linuxfromscratch.org/glfs).


# Goals:
<ul>
<li> [ ] Create Toolchain to produce a multilib system</li>
<li> [ ] Expand documentation to avoid referencing LFS book</li>
<li> [ ] Support hosts that do not use glibc</li>
<li> [ ] Add doucmentation on updating toolchain from previous build</li>
<li> [ ] Expand support to other architecture like arm </li> 
</ul>

# Supported Architectures

Currently only i686/amd64. Will add more once x86 is complete.

# Quick System Specs
<ul>
<li> Kernel: Linux (main stream) </li>
<li> C Library: Glibc </li>
<li> Init: S6+S6-rc </li>
<li> Compiler: GCC </li>
<li> SSL: LibreSSL or OpenSSL </li>
</ul>

# Host Requirements

Run 'check-version.sh'. Otherwise:
<ul>
<li>Coreutils >= 8.1</li>
<li>Bash      >= 3.2</li>
<li>Binutils  >= 2.13.1</li>
<li>Bison     >= 2.7</li>
<li>Diffutils >= 2.8.1</li>
<li>Findutils >= 4.2.31</li>
<li>Gawk      >= 4.0.1</li>
<li>GCC       >= 5.4</li>
<li>GCC (C++) >= 5.4</li>
<li>Grep      >= 2.5.1a</li>
<li>Gzip      >= 1.3.12</li>
<li>M4        >= 1.4.10</li>
<li>Make      >= 4.0</li>
<li>Patch     >= 2.5.4</li>
<li>Perl      >= 5.8.8</li>
<li>Python    >= 3.4</li>
<li>Sed       >= 4.1.5</li>
<li>Tar       >= 1.22</li>
<li>Texinfo   >= 5.0</li>
<li>Xz        >= 5.0.0</li>
<li>linux kernel >=5.4</li>
<li>awk is GNU</li>
<li>yacc is Bison</li>
<li>sh is bash</li>
</ul>

# Build Method

Using the same build method from LFS-9.0 creates a reusable toolchain that is independant of the host and simplifies the process of creating packages to use with a package manager for the final system.

## Build Toolchain

Entire build will build all packages from source. There are 2 stages, based off LFS-9.0:
<ol>
<li>Build a toolchain that will be used to build the final system</li>
<li>Enter chroot to build final system. </li>
</ol>

## Prebuilt Toolchain

If this project has been built before, the old/previous toolchain (tools) can be upgraded to build a newer LFS build. Alternatively, a prebuilt toolchain can be downloaded from past releases and upgraded to build this version... this is yet to be documented.

# Directory
<ul>
<li>1-Preparation - Build instructions for starting a build</li>
<li>2-Toolchain - Instructions for building the tool chain </li>
<li>3-Final-System - Instructions for building the final system</li>
<li>files - Any additonal files needed</li>
<li>patches - Patches for build </li>
</ul>
