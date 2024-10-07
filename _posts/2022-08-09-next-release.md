---
layout: post
title:  "Working on Next Release"
---
We are diligently working on the next release of MIXR.  Due to current interest, we plan to "wrap up" and package current improvements into a release. Eventually we will "divide" or "partition" MIXR into two packages, 1) the simulation/models/physics of entities and interactions and 2) the graphical aspects of displaying a virtual world.  The framework has always been organized this way, but explicitly breaking these aspects out into packages will 1) make it more obvious, and 2) significantly reduce the 3rd party dependencies current provided to build, compile and run non-graphical applications.  This will also make it easy to put the core simulation aspects into a container for independent execution.
