---
layout: single
title: Todo
permalink: /todo/
---

# work in progress

## MPU calculator & display

Currently publishing MPU calculator code.

still need to:

Clean up the mpu calculator code.

document:
- programming .text segment to be read-only/execute,
- everything else read/write/no-execute.
- two stage linking (first to find the size of the .text & .rodata sections, calculate the MPU entries, then relink with new MPU entries.)
- seg-faulting on a stack red-zone.

# future posts

## state machines

Publish the methodology for writing/documenting/testing state machines.

- moore state machines in C
- generating plantuml *from* the source code.
- log state transitions
- test harness

## firmware logging to circular buffers by task

Publish logging to circular buffers, with separate buffers per task or category, and/or severity.

## logging -> sequence diagram with brewer palette.

Publish the register log -> sequence diagram strategy.

## pc/ra logging -> valgrind

Publish the interrupt based pc/ra logging -> valgrind compatible file for kcachegrind.

## load exclusive/store conditional mutex for cortex-M

Publish the load conditional store exclusive speed up of contention free mutexes in freertos.

## bang-bang edge hunting

Publish the bang-bang edge hunting algorithm for adjusting the frequency of one clock to match another.

## calibration in the presence of noise and quantization.

Publish the eye diagram calibration routine which searched for the rising/falling edge of a wave in the presence of noise.

## rational approximations

in digital clock synthesis units we often need to convert one frequency to another with a rational numerator/denominator divider.

The classic continued fractions calculation suffers from very bad successive rounding errors that can produce ludicrously bad results.

Publish the flaws of the continued fractions algorithm and other algorithms like the farey algorithm.


## C functions for coalescing field writes into single register writes.

Publish the strange header files for coalesce field writes into single register writes.

