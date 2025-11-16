# MulitLib-LFS
Linux from Scratch with MulitLib support and S6+S6-RC as init system

This is based on the work of Thomas' Multilib Linux From Scratch (https://www.linuxfromscratch.org/~thomas/multilib-m32), which now uses a different build method based on LFS versions newer than 9.0. That new build method does not work on musl libc based hosts.

The aim of this project is to create a unix-like system using Glibc with support for 32-bit and 64-bit x86 binaries. After completing a build, one may continue building with Gaming Linux From Scratch (https://www.linuxfromscratch.org/glfs).


## Goals:
<ul>
<li> [ ] Create Toolchain to produce a multilib system</li>
<li> [ ] Expand documentation to avoid referencing LFS book</li>
<li> [ ] Support hosts that do not use glibc</li>
<li> [ ] Add doucmentation on updating toolchain from previous build</li>
<li> [ ] Expand support to other architecture like arm </li> 
</ul>

## Supported Architectures

Currently only i686/amd64.

## Quick System Specs
<ul>
<li> Kernel: Linux (main stream) </li>
<li> C Library: Glibc </li>
<li> Init: S6+S6-rc </li>
<li> Compiler: GCC </li>
<li> SSL: LibreSSL or OpenSSL </li>
</ul>

## Build Method

# Build Toolchain

Entire build will build all packages from source. There are 4 stages:
<ol>
<li>Cross-tools - Create a very basic toolchain with host's own tool chain. This will be used to build the next stage. It also allows the next stage to be independent from the host's compiler, useful for hosts not using glibc. </li>
<li>Tools - Creates the tool chain that will be used in the next stage. Resulting toolchain is sandboxed from host and makes it portable across other systems, regardless of libc implementation. Only enough packages are built to chroot and build the rest under chroot.</li>
<li>Chroot - Once the minimal toolchain is built, enter chroot and build the rest of the toolchain.</li>
<li>Final - Build the final system under chroot with toolchain.</li>
</ol>

# Prebuilt Toolchain

If this project has been built before, the old/previous toolchain (tools) can be upgraded to build a newer LFS build. Alternatively, a prebuilt toolchain can be downloaded from past releases and upgraded to build this version. Cross-tools will not be built or required.

## Directory
<ul>
<li>1-Preparation - Build instructions for starting a build</li>
<li>2-Final-System - Instructions for building the final system</li>
<li>files - Any additonal files needed</li>
<li>patches - Patches for build </li>
</ul>
