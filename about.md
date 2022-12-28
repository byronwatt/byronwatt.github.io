---
layout: single
title: About
permalink: /about/
---

I'm a firmware developer working at Microchip.

We've developed firmware for MIPS 34K, Cortex-M7, Cortex-A9 and Cortex-A53 and Risc-V cpus.

Our team creates new telecom chips and I work with the firmware during simulation, emulation, in-house testing, and even after the chip is running in customer equipment.

My role in the team is mostly focused on the system layer, communications, watchdog, exceptions, logging & stats.

weird stuff:

code generation from register definitions similar to [ip-xact](https://en.wikipedia.org/wiki/IP-XACT)

Scripts to convert a moore state machine in C code to a plantuml state diagram. (should publish that).

Scripts to extract register logs and import them into plantuml sequence diagrams.

Scripts to convert performance logs into a valgrind compatible file for kcachegrind.

Weird header files to coalesce field writes into single register writes.

Using the load conditional store exclusive to implement mutexes in freertos. (should publish that).
