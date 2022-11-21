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

Scripts to extract register logs and import them into plantuml sequence diagrams,

Scripts to convert performance logs into a valgrind compatible file for kcachegrind.

Weird header files to coalesce field writes into single register writes,

Using the load conditional store exclusive to implement mutexes in freertos. (should publish that).

# Thanks!

Many thanks for so many people posting great things about how the ARM stuff works:

## Adam Green's Crash Catcher/dumper

[cyrilfougeray firmware-logs-with-stack-trace](http://www.cyrilfougeray.com/2020/07/27/firmware-logs-with-stack-trace.html)

[adamgreen CrashCatcher](https://github.com/adamgreen/CrashCatcher)

[adamgreen CrashDebug](https://github.com/adamgreen/CrashDebug)

## The very nice ARM CMSIS library

[arm CMSIS_5](https://github.com/ARM-software/CMSIS_5)

## M7 links

other links about using the armv7-m MPU for stack protection or just nice overviews of exceptions:

[memfault](https://interrupt.memfault.com/blog/memfault)

[memfault arm-cortex-m-exceptions-and-nvic](https://interrupt.memfault.com/blog/arm-cortex-m-exceptions-and-nvic)

[memfault fix-bugs-and-secure-firmware-with-the-mpu](https://interrupt.memfault.com/blog/fix-bugs-and-secure-firmware-with-the-mpu)

[embeddedcomputing using-a-memory-protection-unit-with-an-rtos-part-2](https://www.embeddedcomputing.com/technology/processing/using-a-memory-protection-unit-with-an-rtos-part-2)

[arm usefulness-of-mpu-in-a-non-os-system](https://community.arm.com/support-forums/f/architectures-and-processors-forum/7107/usefulness-of-mpu-in-a-non-os-system)

[feabhas setting-up-the-cortex-m34-armv7-m-memory-protection-unit-mpu](https://blog.feabhas.com/2013/02/setting-up-the-cortex-m34-armv7-m-memory-protection-unit-mpu/)

[sciencedirect main-stack-pointer](https://www.sciencedirect.com/topics/engineering/main-stack-pointer)
