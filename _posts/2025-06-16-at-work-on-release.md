---
layout: post
title:  "At Work on Release"
---
We have been spending a significant amount of time on this next release. One of the big shifts is to name classes that serve as interfaces with an "I" prefix. They have defined behavior and usually an implementation. You derived new concrete classes from these. Along with that is the creation of concrete classes marked "final". This is a C++ keyword that prevents further derivation from them. This is considered good practice, interface classes along with concrete ones. In many ways we have adopted Java and Julia-like features and are sidestepping well-known slicing problems.
