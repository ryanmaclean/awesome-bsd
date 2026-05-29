# Awesome BSD

A compact starting point for BSD operating systems, documentation, communities, and ecosystem software.

## Start Here

BSD is a family of Unix-like operating systems descended from the Berkeley Software Distribution. Start with official documentation:

* **General server, workstation, jail, bhyve, or ZFS use:** FreeBSD and the FreeBSD Handbook.
* **Security-focused base system, PF, network services, or compact documentation:** OpenBSD and the OpenBSD FAQ.
* **Portability, old or unusual hardware, pkgsrc, or classic Unix feel:** NetBSD and the NetBSD Guide.
* **HAMMER2, kernel work, or a smaller x86-64 BSD:** DragonFly BSD and the DragonFly BSD Handbook.
* **Desktop-oriented FreeBSD:** GhostBSD or NomadBSD.
* **Firewall or router appliance:** OPNsense, pfSense, or BSD Router Project.

## Platform Map

```text
hardware or goal
|-- amd64 / x86-64 PC, server, or VM
|   |-- general purpose: FreeBSD
|   |-- security-focused base system: OpenBSD
|   |-- portability or older hardware: NetBSD
|   `-- HAMMER2 or DragonFly internals: DragonFly BSD
|-- i386 / 32-bit x86: NetBSD or OpenBSD
|-- arm64 / aarch64: FreeBSD, OpenBSD, or NetBSD
|-- riscv64: FreeBSD, OpenBSD, or NetBSD
|-- Octeon / MIPS64 network appliance: OpenBSD/octeon or NetBSD/evbmips
|-- 32-bit ARM board: NetBSD first, then FreeBSD if the board is listed
`-- STM32, ESP32, Arduino, MiSTer, or retro hardware
    `-- not a mainstream BSD target; check embedded or historical projects
```

Notes:

* FreeBSD 14.x is the last FreeBSD release line with standalone i386 support; FreeBSD 15.0 and later do not provide i386 install images.
* On arm64 boards, check board-specific notes before assuming Wi-Fi, GPU, sleep, or boot support.
* On riscv64, expect a rougher path than amd64.
* For Octeon, start with OpenBSD/octeon. NetBSD/evbmips supports some Cavium Octeon designs. FreeBSD MIPS is unsupported as of FreeBSD 14.0.

## Core BSDs

* FreeBSD - general-purpose BSD for servers, workstations, networking, storage, jails, bhyve, and ZFS.
* OpenBSD - security-focused BSD with strong manual pages, PF, OpenSSH, and a compact base system.
* NetBSD - portable BSD for many CPU families, older systems, embedded boards, and pkgsrc.
* DragonFly BSD - x86-64 BSD with a distinct kernel direction and HAMMER2 filesystem.

## Desktop, Appliance, And Specialized Systems

* GhostBSD - desktop-oriented FreeBSD derivative.
* NomadBSD - FreeBSD-based live USB desktop and rescue system.
* helloSystem - FreeBSD-based desktop system with a Mac-like user experience.
* OPNsense - FreeBSD-based firewall and routing platform.
* pfSense - FreeBSD-based firewall and router distribution.
* BSD Router Project - FreeBSD-based router distribution using FRRouting and BIRD.
* HardenedBSD - security-enhanced FreeBSD fork.
* MidnightBSD - desktop-oriented BSD derivative.
* CheriBSD - research FreeBSD adaptation for CHERI architectures.

## Embedded, Historical, And Niche

These are not default newcomer starting points.

* LiteBSD - 4.4BSD-derived system for PIC32MZ microcontrollers.
* RetroBSD - 2.11BSD-derived system for PIC32 microcontrollers.
* ZRouter - FreeBSD-based firmware project for embedded devices.
* OS108 - NetBSD-based desktop-oriented project.
* SmallWall - small firewall project descended from the m0n0wall/pfSense ecosystem.
* t1n1wall - m0n0wall-derived firewall project.

## Practical BSD Software

* Bastille - FreeBSD jail management.
* CBSD - FreeBSD jail, bhyve, and Xen management.
* iocage - FreeBSD jail manager.
* pot - FreeBSD jail manager for container-style workflows.
* poudriere - FreeBSD package build and test system.
* pkg - FreeBSD package manager.
* vm-bhyve - bhyve VM manager.
* OpenZFS - storage platform used by FreeBSD and other systems.
* HAMMER2 - DragonFly BSD copy-on-write filesystem.
* BSD-Cloud-Image - unofficial BSD cloud images.
* linuxulator-steam-utils - Steam client helpers for FreeBSD Linux emulation.

## Linux-To-BSD Orientation

BSD systems are not Linux distributions with different package names. Each BSD ships a coherent base system, its own manual pages, and project-specific administration tools.

Guides to consult when verifying Linux-to-BSD mappings:

* FreeBSD Quickstart Guide for Linux Users.
* FreeBSD Handbook.
* OpenBSD FAQ, OpenBSD afterboot(8), and OpenBSD manual pages.
* NetBSD Guide and pkgsrc guide.
* DragonFly BSD Handbook and DPorts documentation.

Common translation points:

* Shell: expect base `sh`, `ksh`, or `tcsh`; do not assume Bash-only scripts work.
* Third-party files: FreeBSD and DragonFly commonly use `/usr/local`; NetBSD pkgsrc commonly uses `/usr/pkg`; OpenBSD packages also install under `/usr/local`.
* Packages: FreeBSD and DragonFly use `pkg`; OpenBSD uses `pkg_add`, `pkg_delete`, and `pkg_info`; NetBSD uses pkgsrc tools and often `pkgin` for binary packages.
* Updates: FreeBSD has `freebsd-update` for base-system binary updates; OpenBSD uses `sysupgrade` and `syspatch`; NetBSD and DragonFly have their own release and source/pkgsrc workflows.
* Services: do not assume `systemctl`. FreeBSD uses rc scripts and `service`; OpenBSD uses `rcctl`; NetBSD and DragonFly use rc.d-style systems.
* Networking: do not assume `ip` or `eth0`. Use `ifconfig`, `route`, and driver-based interface names such as `em0`, `re0`, or `vio0`.
* Firewalling: do not assume `iptables` or `nft`. OpenBSD uses PF; FreeBSD commonly uses PF or IPFW; NetBSD has its own firewall history and PF/NPF context.
* Hardware inventory: Linux `lspci`, `lsusb`, and `lsblk` map imperfectly. Expect tools such as `pciconf`, `usbconfig`, `pcictl`, `usbdevs`, `geom`, `gpart`, `camcontrol`, `disklabel`, and `dmesg`, depending on BSD.
* Kernel modules: FreeBSD uses `kldstat`, `kldload`, and `kldunload`; other BSDs differ.
* Tracing: FreeBSD has `truss` as a common `strace` counterpart.
* System settings: prefer `sysctl` over Linux `/proc` and `/sys` assumptions.
* Build tools: BSD `make` is not GNU Make; GNU Make is usually installed as `gmake`.
* Privilege escalation: OpenBSD commonly uses `doas`; do not assume `sudo` is installed.
* Core utilities: flags and output can differ from GNU coreutils. Read the target system's man page before scripting.

## News, Community, And Learning

* FreeBSD Foundation, NetBSD Foundation, OpenBSD Foundation - project support organizations.
* FreeBSD Status Reports, NetBSD Blog, OpenBSD Errata - official project updates.
* BSDCan, EuroBSDCon, AsiaBSDCon - conferences.
* TeachBSD - operating systems teaching material using BSD tracing.
* Klara Systems Articles - practical FreeBSD, OpenZFS, and infrastructure articles.
* dmesgd - searchable user-submitted BSD dmesg database.

## Books And History

* Absolute FreeBSD, Absolute OpenBSD, and the FreeBSD Mastery books.
* The Design and Implementation of the FreeBSD Operating System.
* BSD Family Tree, BSD Distributions Timeline, The Unix Tree, and Unix History.

## Maintenance

This README is the source of truth. Keep outbound links out of this file unless there is a strong reason to add one. Prefer official documentation and project pages when verifying entries, but record names and descriptions here. Describe who a resource is for, label niche or historical entries clearly, keep descriptions factual, and run `git diff --check` before committing.
