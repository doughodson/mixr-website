---
layout: page
title: Interop
permalink: /interop.html
---
Interoperability is a property referring to the ability of diverse systems and organizations to work together (inter-operate). With respect to software, the term interoperability is used to describe the capability of different programs to exchange data via a common set of exchange formats, to read and write the same file formats, and to use the same protocols.

Currently, MIXR supports the DIS interoperability standard, but in the future, we hope to support more.

Distributed Interactive Simulation (DIS)
========================================

Distributed Interactive Simulation (DIS) is an open standard for conducting real-time platform-level wargaming across multiple host computers and is used worldwide especially by military organizations but also by other agencies such as those involved in space exploration and medicine. It defines a set of Protocol Data Units, or PDUs, for publishing Entity State information, Fire and Detonate events, Logistics information, Emissions and Communications data, and more. The DIS protocol was defined through an open standards development process, with participation by government, industry, and academia.

While DIS is defined by IEEE Standard 1278 which contains all of the information about the structure of the various PDUs, the values for the various DIS enumerations were deemed too dynamic, or fast-changing to include in a slow-changing IEEE Standard. For this reason, these values and enumerations are maintained by [SISO](https://www.sisostds.org) (Simulation Interoperability Standards Organization) in a separate document called Enumeration and Bit Encoded Values for Use with Protocols for Distributed Interactive Simulation Applications. The most recent version can be downloaded here: [SISO-REF-010-2006.zip]({{ site.baseurl }}/assets/pages/interop/siso_ref_010_2006.zip)
   
High Level Architecture (HLA)
=============================

The High Level Architecture (HLA) is a general purpose architecture for distributed computer simulation systems. Using HLA, computer simulations can communicate with other computer simulations regardless of the computing platforms. Rather than a networking protocol (wire standard) like DIS, HLA defines an architecture with a set of API (Application Programmer's Interface) Standards. Simulation applications (known as federates in HLA) communicate by making calls to the HLA APIs. A piece of software known as the RTI (Run-time Infrastructure) implements the HLA API, and is responsible for transporting data from one federate to another. Like DIS, the HLA Standards are owned by IEEE.

![]({{ site.baseurl }}/assets/pages/interop/portico_logo.png "poRTIco")

We are looking at the [poRTIco project](http://porticoproject.org). Portico is a fully supported, open-source, cross-platform HLA RTI implementation.

