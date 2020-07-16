---
layout: page
title: Overview
permalink: /overview.html
---
MIXR is an open source platform designed to support the rapid construction of virtual (human-in-the-loop) and constructive simulation applications. It has been used extensively to build DIS compliant distributed simulation systems.

Serving as a simulation design pattern it provides a structure for constructing simulation applications. The framework aids the design of robust, scalable, virtual, constructive, stand-alone, and distributed simulation applications. It leverages modern object-oriented software design principles while incorporating fundamental real-time system design techniques to meet human interaction requirements.

![image](/assets/pages/overview/structure.png)

By providing abstract representations of system components (that the object-oriented design philosophy promotes), multiple levels of fidelity can be easily intermixed and selected for optimal runtime performance. Abstract representations of systems allow a developer to tune the application to run efficiently so that human-in-the-loop interaction latency deadlines can be met. On the flip side, constructive-only simulation applications that do not need to meet time-critical deadlines can use models with even higher levels of fidelity.

The framework embraces the Model-View-Controller (MVC) software design pattern by partitioning functional components into packages. This concept is taken a step further by providing an abstract network interface so custom protocols can be implemented without affecting system models. Examples include the Distributed Interactive Simulation (DIS) protocol interface.

![image](/assets/pages/overview/packages.png)

The framework and its distribution are organized into a series of packages as shown above. We utilize a number of other third-party open source tools such as Qt, FLTK and Fox for cross-platform GUI applications, and JSBSim as a high-quality flight dynamics model.

