# Awesome BSD

A compact starting point for BSD operating systems, documentation, communities, and ecosystem software.

## Start Here

BSD is a family of Unix-like operating systems descended from the Berkeley Software Distribution. Start with official documentation:

* **General server, workstation, jail, bhyve, or ZFS use:** [FreeBSD](https://www.freebsd.org/) and the [FreeBSD Handbook](https://docs.freebsd.org/en/books/handbook/).
* **Security-focused base system, PF, network services, or compact documentation:** [OpenBSD](https://www.openbsd.org/) and the [OpenBSD FAQ](https://www.openbsd.org/faq/).
* **Portability, old or unusual hardware, pkgsrc, or classic Unix feel:** [NetBSD](https://netbsd.org/) and the [NetBSD Guide](https://netbsd.org/docs/guide/en/).
* **HAMMER2, kernel work, or a smaller x86-64 BSD:** [DragonFly BSD](https://www.dragonflybsd.org/) and the [DragonFly BSD Handbook](https://www.dragonflybsd.org/docs/newhandbook/).
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

* [FreeBSD](https://www.freebsd.org/) - general-purpose BSD for servers, workstations, networking, storage, jails, bhyve, and ZFS.
* [OpenBSD](https://www.openbsd.org/) - security-focused BSD with strong manual pages, PF, OpenSSH, and a compact base system.
* [NetBSD](https://netbsd.org/) - portable BSD for many CPU families, older systems, embedded boards, and pkgsrc.
* [DragonFly BSD](https://www.dragonflybsd.org/) - x86-64 BSD with a distinct kernel direction and HAMMER2 filesystem.

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

This README is the source of truth. Prefer official documentation and project pages over community or aggregator links. Describe who a resource is for, label niche or historical entries clearly, keep descriptions factual, and run `git diff --check` before committing.
