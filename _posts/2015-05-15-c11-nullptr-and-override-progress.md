---
layout: post
title:  "C++11 'nullptr' and 'override' Progress"
---
After having spent a considerable amount of time manually working and nearly completing this effort, we come to discover clang's automated modernizer tool. Clang is a compiling environment/system, and the modernizer is a supporting tool that can be used to convert, transform or migrate existing C++ code to use newer, modern programming features introduced in C++11. For example, the intelligent replacement of 0's or NULL's with 'nullptr' and the discovery of where the context keyword 'override' can be used are two such transformations. Specifically, the modernizer locates where to apply particular transformations and applies hem as directed.

The progress status for this effort is 100% complete for the framework, and about 70% for the examples. Having discovered this tool, the remaining work should happen quickly. All work is posted in GitHub [repo](https://github.com/doughodson/OpenEaagles).
