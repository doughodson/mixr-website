---
layout: post
title:  "Adopting C++11 'nullptr'"
---
We have started the process of adopting C++11's **nullptr** throughout the framework. The introduction of this literal (of type **std::nullptr_t**) finally once and for all unambiguously defines a pointer as pointing at nothing. Previously, developers indicated this meaning by setting pointers to either the macro NULL (macros are bad!) or simply the integer value 0 (as done throughout openeaagles). Like **override** leveraging this literal improves code documentation and also helps prevent some interesting side efforts from occurring.

Starting with Visual Studio 2010, **nullptr** is fully supported - the GCC and clang toolchains have supported it for some time. As with override adopting it allows us to continue to step forward by simultaneously improving code quality and documentation without severely impacting legacy compiler support.

This effort is underway within the git repo on GitHub and will take some time - locating all the instances where **nullptr** should be used requires careful examination of each class - which in many ways provides the motivation and clear rationale to adopt it in the first place.

Note: The use of **nullptr** does not impact the compatibility of this software or affect applications built using it. It simply improves the quality of the underlying code-base.
