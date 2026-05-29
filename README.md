# Awesome BSD [![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)

A compact starting point for BSD operating systems, documentation, communities, and ecosystem software.

## Start Here

BSD is a family of Unix-like operating systems descended from the Berkeley Software Distribution. Start with official documentation:

* **General server, workstation, jail, bhyve, or ZFS use:** [FreeBSD](https://www.freebsd.org/) and the [FreeBSD Handbook](https://docs.freebsd.org/en/books/handbook/).
* **Security-focused base system, PF, network services, or compact documentation:** [OpenBSD](https://www.openbsd.org/) and the [OpenBSD FAQ](https://www.openbsd.org/faq/).
* **Portability, old or unusual hardware, pkgsrc, or classic Unix feel:** [NetBSD](https://netbsd.org/) and the [NetBSD Guide](https://netbsd.org/docs/guide/en/).
* **HAMMER2, kernel work, or a smaller x86-64 BSD:** [DragonFly BSD](https://www.dragonflybsd.org/) and the [DragonFly BSD Handbook](https://www.dragonflybsd.org/docs/newhandbook/).
* **Desktop-oriented FreeBSD:** [GhostBSD](https://www.ghostbsd.org/) or [NomadBSD](https://nomadbsd.org/).
* **Firewall or router appliance:** [OPNsense](https://opnsense.org/), [pfSense](https://www.pfsense.org/), or [BSD Router Project](https://bsdrp.net/).

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
* For Octeon, start with [OpenBSD/octeon](https://www.openbsd.org/octeon.html). [NetBSD/evbmips](https://wiki.netbsd.org/ports/evbmips/) supports some Cavium Octeon designs. FreeBSD MIPS is unsupported as of FreeBSD 14.0.

## Core BSDs

* [FreeBSD](https://www.freebsd.org/) - general-purpose BSD for servers, workstations, networking, storage, jails, bhyve, and ZFS. Links: [download](https://www.freebsd.org/where.html), [handbook](https://docs.freebsd.org/en/books/handbook/), [manual pages](https://man.freebsd.org/), [forums](https://forums.freebsd.org/), [FreshPorts](https://www.freshports.org/).
* [OpenBSD](https://www.openbsd.org/) - security-focused BSD with strong manual pages, PF, OpenSSH, and a compact base system. Links: [download](https://www.openbsd.org/ftp.html), [FAQ](https://www.openbsd.org/faq/), [manual pages](https://man.openbsd.org/), [platforms](https://www.openbsd.org/plat.html), [OpenBSD Journal](https://undeadly.org/).
* [NetBSD](https://netbsd.org/) - portable BSD for many CPU families, older systems, embedded boards, and pkgsrc. Links: [download](https://netbsd.org/releases/), [guide](https://netbsd.org/docs/guide/en/), [ports](https://netbsd.org/ports/), [manual pages](https://man.netbsd.org/), [pkgsrc](https://www.pkgsrc.org/).
* [DragonFly BSD](https://www.dragonflybsd.org/) - x86-64 BSD with a distinct kernel direction and HAMMER2 filesystem. Links: [download](https://www.dragonflybsd.org/download/), [handbook](https://www.dragonflybsd.org/docs/newhandbook/), [HAMMER2](https://www.dragonflybsd.org/hammer/), [Digest](https://www.dragonflydigest.com/).

## Desktop, Appliance, And Specialized Systems

* [GhostBSD](https://www.ghostbsd.org/) - desktop-oriented FreeBSD derivative. Links: [download](https://www.ghostbsd.org/download), [forums](https://forums.ghostbsd.org/).
* [NomadBSD](https://nomadbsd.org/) - FreeBSD-based live USB desktop and rescue system. Links: [download](https://nomadbsd.org/download.html).
* [helloSystem](https://hellosystem.github.io/) - FreeBSD-based desktop system with a Mac-like user experience. Links: [releases](https://github.com/helloSystem/ISO/releases), [docs](https://hellosystem.github.io/docs/).
* [OPNsense](https://opnsense.org/) - FreeBSD-based firewall and routing platform. Links: [download](https://opnsense.org/download/), [forum](https://forum.opnsense.org/).
* [pfSense](https://www.pfsense.org/) - FreeBSD-based firewall and router distribution. Links: [download](https://www.pfsense.org/download/), [forum](https://forum.pfsense.org/).
* [BSD Router Project](https://bsdrp.net/) - FreeBSD-based router distribution using FRRouting and BIRD. Links: [downloads](https://bsdrp.net/downloads?DokuWiki=e8a2af21cc91416f910347e472b73841).
* [HardenedBSD](https://hardenedbsd.org/) - security-enhanced FreeBSD fork. Links: [installers](https://installers.hardenedbsd.org/pub/current/), [wiki](https://github.com/HardenedBSD/hardenedBSD/wiki).
* [MidnightBSD](https://www.midnightbsd.org/) - desktop-oriented BSD derivative. Links: [download](https://www.midnightbsd.org/download/).
* [CheriBSD](https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/cheribsd.html) - research FreeBSD adaptation for CHERI architectures. Links: [downloads](https://cheri-dist.cl.cam.ac.uk/), [source](https://github.com/CTSRD-CHERI/cheribsd).

## Embedded, Historical, And Niche

These are not default newcomer starting points.

* [LiteBSD](https://github.com/sergev/LiteBSD/wiki) - 4.4BSD-derived system for PIC32MZ microcontrollers.
* [RetroBSD](https://retrobsd.org/) - 2.11BSD-derived system for PIC32 microcontrollers.
* [ZRouter](https://zrouter.org/) - FreeBSD-based firmware project for embedded devices.
* [OS108](https://os108.org/) - NetBSD-based desktop-oriented project.
* [SmallWall](https://www.smallwall.org/) - small firewall project descended from the m0n0wall/pfSense ecosystem.
* [t1n1wall](https://t1n1wall.com/) - m0n0wall-derived firewall project.

## Practical BSD Software

* [Bastille](https://bastillebsd.org/) - FreeBSD jail management.
* [CBSD](https://cbsd.io/) - FreeBSD jail, bhyve, and Xen management.
* [iocage](https://github.com/freebsd/iocage) - FreeBSD jail manager.
* [pot](https://pot.pizzamig.dev/) - FreeBSD jail manager for container-style workflows.
* [poudriere](https://github.com/freebsd/poudriere) - FreeBSD package build and test system.
* [pkg](https://github.com/freebsd/pkg) - FreeBSD package manager.
* [vm-bhyve](https://github.com/freebsd/vm-bhyve/) - bhyve VM manager.
* [OpenZFS](https://openzfs.org/) - storage platform used by FreeBSD and other systems.
* [HAMMER2](https://www.dragonflybsd.org/hammer/) - DragonFly BSD copy-on-write filesystem.
* [BSD-Cloud-Image](https://bsd-cloud-image.org/) - unofficial BSD cloud images.
* [linuxulator-steam-utils](https://github.com/shkhln/linuxulator-steam-utils) - Steam client helpers for FreeBSD Linux emulation.

## News, Community, And Learning

* [FreeBSD Foundation](https://freebsdfoundation.org/), [NetBSD Foundation](https://www.netbsd.org/foundation/), [OpenBSD Foundation](https://www.openbsdfoundation.org/) - project support organizations.
* [FreeBSD Status Reports](https://www.freebsd.org/status/), [NetBSD Blog](https://blog.netbsd.org/), [OpenBSD Errata](https://www.openbsd.org/errata.html) - official project updates.
* [BSDNow](https://www.bsdnow.tv/), [2.5 Admins](https://2.5admins.com/), [BSDTalk](https://bsdtalk.blogspot.com/) - podcasts.
* [BSDCan](https://www.bsdcan.org/), [EuroBSDCon](https://www.eurobsdcon.org/), [AsiaBSDCon](https://asiabsdcon.org/) - conferences.
* [TeachBSD](https://teachbsd.org/) - operating systems teaching material using BSD tracing.
* [Klara Systems Articles](https://klarasystems.com/articles/) - practical FreeBSD, OpenZFS, and infrastructure articles.
* [dmesgd](https://dmesgd.nycbug.org/) - searchable user-submitted BSD dmesg database.
* [BSD Cafe](https://bsd.cafe), [BSD Network](https://bsd.network/about), [/r/bsd](https://www.reddit.com/r/bsd) - community spaces.

## Books And History

* [Absolute FreeBSD](https://mwl.io/nonfiction/os#af3e), [Absolute OpenBSD](https://www.michaelwlucas.com/os/ao2e), and the [FreeBSD Mastery](https://www.michaelwlucas.com/os) books.
* [The Design and Implementation of the FreeBSD Operating System](https://www.amazon.com/Design-Implementation-FreeBSD-Operating-System/dp/0321968972/).
* [BSD Family Tree](https://cgit.freebsd.org/src/tree/share/misc/bsd-family-tree), [BSD Distributions Timeline](https://github.com/FabioLolix/BSD-Timeline), [The Unix Tree](https://www.tuhs.org/cgi-bin/utree.pl), and [Unix History](https://www.levenez.com/unix/).

## Maintenance

This README is the source of truth. Prefer official documentation, project pages, foundations, manpages, and active communities. Describe who a resource is for, label niche or historical entries clearly, check changed URLs, keep descriptions factual, and run `git diff --check` before committing.
