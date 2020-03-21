# MulitLib-LFS
Linux from Scratch with MulitLib support and S6+S6-RC as init system

This is based on the work from Linux from Scratch (https://www.linuxfromscratch.org) which does not build multilib support (i.e. run i686 binaries on a x86_64 system ). Also based on notes from https://www.linuxquestions.org/questions/linux-from-scratch-13/%5Bguide%5D-howto-multilib-lfs-4175649832

The aim of this project is to create a unix system using Glibc with support for 32-bit and 64-bit x86 binaries. Init system will be S6+S6-rc from skarnet.org

## Goals:
<ul>
<li> [x] Create Toolchain to produce a multilib system</li>
<li> [ ] Expand documentation to avoid referencing LFS book</li>
<li> [ ] Update S6+S6-rc to latest version. Currently stuck on s6-rc-0.4.1.0 due to database change in newer versions</li>
</ul>

## Quick System Specs
<ul>
<li> Kernel: Linux (main stream) </li>
<li> C Library: Glibc </li>
<li> Init: S6+S6-rc </li>
<li> Compiler: GCC </li>
<li> SSL: LibreSSL or OpenSSL </li>
</ul>

## Directory
<ul>
<li>doc - Build instructions for project</li>
<li>files - Any additonal files needed</li>
<li>patches - Patches for build </li>
</ul>
