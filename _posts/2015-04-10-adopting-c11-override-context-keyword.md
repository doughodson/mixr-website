---
layout: post
title:  "Adopting C++11 'override' Context Keyword"
---
We have embraced the C++11 defined context sensitive keyword **override** throughout the framework. Using **override** throughout the framework serves two important purposes; 1) it adds clarity and serves as a form of documentation to developers - by using it, overridden subclass methods are clearly distinguished from newly defined ones, and 2) it informs the compiler as to developer intent - meaning, it marks the method(s) that are intended to be overrides and not intended to define new ones that possibly inadvertently shadow base methods.

Starting with Visual Studio 2010, **override** is fully supported - the GCC and clang toolchains have supported it for some time. Adopting it allows us to continue to step forward by simultaneously improving code quality and documentation without severely impacting legacy compiler support.

This effort has been completed in the git master branch on GitHub. Although somewhat of a herculean effort, the process of completing this was simplified considerably by leveraging Eclipse's C/C++ Development Tooling (CDT) plugin. The current version of CDT visually indicates overridden class methods in the editor, which aided in properly identifying and marking them.

Note: The use of **override** does not impact the compatibility of this software or affect applications built using it. It simply improves the quality of the underlying code-base.
