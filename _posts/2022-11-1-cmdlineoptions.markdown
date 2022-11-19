---
layout: post
title:  "simple command line options"
date:   2022-11-1 09:16:38 -0800
---

Mohammad wanted to borrow the CmdLineOptions library that we use at microchip so that started me down this path of starting a github page.


This command line parser lets you scatter options throughout your code base, and the top level main() function doesn't need to know anything about them.

Just like how googletest doesn't need to know about all the GTEST() macros to run those tests, this command line parser doesn't need to know about all the command line options exposed in your code.

here's the repo:
[CmdLineOptions](https://github.com/byronwatt/CmdLineOptions)

And I got to write some command line tests with 'bats' which was very fun, and see how that integrates with the github coverage workflow.

