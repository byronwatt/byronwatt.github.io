---
layout: single
title:  "extending 32 bit counters to 64 bit counters"
date:   2022-11-16 09:16:38 -0800
author_profile: false
toc: true
toc_label: "  Contents"
toc_icon: "file-alt"
categories:
  - embedded
  - C
---


# work in progress,... need to cleanup MPU calculator.

At the freertos forum I added a post here: 
(freertos-mpu-support-in-arm-cortex-m7)[https://forums.freertos.org/t/freertos-mpu-support-in-arm-cortex-m7/15306/9] and was hoping that people might be able to reuse the work we did for calculating and displaying the MPU table.

# introduction

At microchip, we changed FreeRTOS to update one MPU entry as a red-zone for the bottom of stack every task switch,… this is one memory write,… and that allows us to remove the optional freertos stack overflow checking which checks that the bottom of stack hasn’t been modified, which is faster if you were going to enable stack checking.

we also created a program to configure the MPU in a slightly simpler way than the CMSIS macros, and created a program to display the resulting memory map after the MPU entries are programmed.

here’s a git repo of our code for displaying & calculating memory maps (I still have to sanitize the code for public consumption, and show the freertos patch).

https://github.com/byronwatt/MPUCalc

todo: add readme to MPU calc documenting:

document:
- programming .text segment to be read-only/execute,
- everything else read/write/no-execute.
- two stage linking (first to find the size of the .text & .rodata sections, calculate the MPU entries, then relink with new MPU entries.)
- seg-faulting on a stack red-zone.