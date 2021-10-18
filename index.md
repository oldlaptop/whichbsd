---
layout: default
---

# Which BSD Should I Use?
##### Last updated: {{ 'now' | date: "%Y-%m-%d" }}

This question comes up on an almost daily basis on BSD-related IRC channels,
forums, and mailing lists.
Asking the users of each BSD will yield different opinionated answers, so here
are some basic facts about each one to let you decide which one to use.
Of course, the best way to make the decision for yourself is to just try each
one and see which you prefer.

## A Quick BSD History

[Berkeley Software
Distribution](https://en.wikipedia.org/wiki/Berkeley_Software_Distribution)
(BSD) was a variant of Unix developed in the 1970s.
After the 4.3BSD release in 1986, remaining proprietary AT&T code was removed
or replaced in a release called Net/1 under a newly created BSD license.
Net/2 led to a port to the Intel 80386 released as 386BSD in 1992, which
quickly diverged into the FreeBSD and NetBSD projects.
[AT&T's lawsuit](https://en.wikipedia.org/wiki/UNIX_System_Laboratories,_Inc._v._Berkeley_Software_Design,_Inc.)
against the University of California prompted the final 4.4BSD-Lite2 release in
1995 which was retroactively integrated into these already-established 386BSD
forks to put to rest any licensing issues.

## Major BSD Operating Systems

Unlike various distributions of GNU/Linux which wrap combinations of similar
software around a single Linux kernel, each modern BSD operating system is its
own separate project with its own kernel, libraries, and userland software.
While each of the projects do share code from time to time, they have diverged
from each other decades ago and now differ widely in internal architecture and
development.

The 4 major BSD-based operating systems in alphabetical order:

### [DragonFlyBSD](https://www.dragonflybsd.org/)

DragonFlyBSD was forked from FreeBSD in 2003 to improve system performance.

TODO

### [FreeBSD](https://www.freebsd.org/)

FreeBSD started as a descendant of 386BSD in 1993.

TODO

### [NetBSD](https://www.netbsd.org/)

One of the oldest BSD derivatives still under active development (having similar roots in 386BSD and 4.3BSD NET/2 to FreeBSD), NetBSD is best known for its focus on portability.
(This set it apart from FreeBSD in the early days: FreeBSD was primarily interested in support for i386 machines, while NetBSD aimed to support as many different machines as possible.)
Today, it's the only BSD derivative with any level of support for some unusual or historic machines, such as
[VAXen](https://wiki.netbsd.org/ports/vax/),
[Motorola 68000-based Macintoshes](https://wiki.netbsd.org/ports/mac68k),
and the
[Sega Dreamcast](https://wiki.netbsd.org/ports/dreamcast/).
Other features that set it apart from the others include support for acting as a
[Xen control domain](https://wiki.netbsd.org/ports/xen/)
and a well-oiled framework for
((cross-)compiling the system from source)[https://www.netbsd.org/docs/guide/en/chap-build.html]
easily.
NetBSD also maintains the (pkgsrc)[https://pkgsrc.org/] package system, which is similar to the other BSD derivatives' "ports trees", but supports many UNIX-like systems other than NetBSD, such as the other major BSDs, Linux, illumos, and macOS.

TODO

### [OpenBSD](https://www.openbsd.org/)

OpenBSD was forked from NetBSD in 1995 and quickly focused on security and code
correctness.

- Develops and maintains
[OpenSSH](https://www.openssh.com/),
[OpenBGPD](https://www.openbgpd.org/),
[OpenNTPD](http://www.openntpd.org/),
[OpenSMTPD](http://www.opensmtpd.org/),
and [LibreSSL](http://www.libressl.org/)

- Publishes a new release reliably every six months and supports one previous
release through its
[`syspatch`](https://man.openbsd.org/syspatch)
binary update tool and
[3rd party package](https://www.openbsd.org/faq/faq15.html)
updates through
[`pkg_add`](https://man.openbsd.org/pkg_add)

- All development between releases is done on one central
[`-current`](https://www.openbsd.org/faq/faq5.html#Flavors)
branch, from which regular snapshots are made and released

- Supports
[a number](https://www.openbsd.org/plat.html)
of hardware platforms from common
[amd64](https://www.openbsd.org/amd64.html)-based
servers to the
[Raspberry Pi](https://www.openbsd.org/arm64.html)
to giant
[UltraSPARC servers](https://www.openbsd.org/sparc64.html)

- Has a wide range of hardware device support with drivers for
[802.11 WiFi](https://man.openbsd.org/?query=wireless&apropos=1&sec=0&arch=default&manpath=OpenBSD-current)
to
[10Mbit to 10Gbit ethernet](https://man.openbsd.org/?query=ethernet&apropos=1&sec=0&arch=default&manpath=OpenBSD-current)
to the latest
[GPUs](https://man.openbsd.org/inteldrm)
from Intel, AMD, and Radeon ported from Linux

While OpenBSD has a reputation for being lightweight, secure, and stable, it
does usually perform slower than FreeBSD or NetBSD in network and system
performance benchmarks.

#### About

This site aims to be a neutral resource.
You can submit changes to it by submitting a pull request or sending diffs
[here](https://github.com/jcs/whichbsd).
