---
layout: post
title:  "Working on Next Release"
---
We are diligently working on the next release of MIXR.  Due to surprising interest (and usage), we plan to "wrap up" current work into a release and plan to "divide" or "partition" MIXR into two packages, 1) the simulation/models/physics of defining and computing entity interactions and 2) the graphical aspects of displaying a virtual world.  The framework has also been organized this way, but explicitly defining these aspects into two clear-cut packages will significantly reduce the 3rd party dependencies current provided to compile and run examples.  Furthermore, this will promote the potential use of container technologies to house the simulation aspects away from graphical concerns.
