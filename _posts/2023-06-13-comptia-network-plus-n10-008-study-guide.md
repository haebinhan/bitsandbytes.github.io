---
title: "CompTIA Network+ N10-008 Study Guide"
layout: post
date: 2023-06-13
feature_image: images/comptianetworkplus.png
tags: [comptia, network+, studyguide, networking]
---

*Disclaimer: This study guide builds off of my own personal knowledge and was used as my study tool for the exam. As such, any other viewers who see this post will have different beginning knowledge so information may be missing or redundant. As with any exam, multiple study sources are recommended!*

<!--more-->

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

## Table of Contents

1. [Internet Connections](#osi-model-network-functions)
2. [Ethernet]

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### OSI Model Network Functions 
✧. ┊ ⁭ [OSI Model](#ೃ⁀-osi) ✧ [Router](#ೃ⁀-soho-router) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ OSI
- Open Systems Interconnection Model by the ISO
- Conceptual model organizing network and hardware functions/components into 7 layers
- All People Seem To Need Data Processing (Application, Presentation, Session, Transport, Network, Data Link, Physical)
- Data encapsulation and decapsulation
- **Physical Layer**: transmission and recept of signals of bits of data. Cabled or wireless. Physical topology, physical interface (cable specifications, pin details, etc) and signaling (transmitting/receiving encoded data). *Devices*: Tranceiver, Repeater (signal amplification), Hub, Media converter, Modem 
- **Data Link Layer**: transferring of data between nodes on same logical segment (using hardware addresses) logical topology. Central nodes can give forwarding functions and deals with *frames* (unit) adding source/destination hardware address as header field. *Devices*: NIC, Brtidge, Switch, AP (wireless access point, bridge between wireless/wired networks)
- **Network Layer**: Moves data around networks/Internet using logical network and host IDs and forwarding between networks with hops/router. Uses routers. ACL at layer 3
- **Transport Layer**: end-to-end/host-to-host layer. Network applications assigned port number and deals with segments that has port num. *Devices*: Multilayer switches (usually as load balancers) and advanced firewalls and IDSs (security appliances)
- **Session Layer**: the exchange of multiple messages between client/server. Layer includes functions that administer session process from beginning to end 
- **Presentation Layer**: Transforms data between network and application types
- **Application Layer**: Top of stack, the protocls give an interface for software programs 

<br>
####  ೃ⁀➷ SOHO Router
- Small Office Home Office
- Layer 1 physical connections: RJ-45 ports connecting to local cabled network (LAN ports), radio antennas (transmit and receive wireless signal), modem (cable or digital subscriber line to connect to ISP network; WAN port)
- Layer 2: ethernet switch (connected to RJ-45 jack), Wireless AP (wirless network, AP internally wired to switch port)
- Layer 3 functions: forwarding decisions, IP addresses private range, DHCP server
- Hexadecimal: From decimal to hex, divide by 16. Remainder is least significant hex digit and quotient is second hex digit. (0xQuotientRemainder)
- CPE Customer Premises Equipment



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Ethernet
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Ethernet Standards
- 802.3 Ethernet standards by IEEE
- 3 part convention xBASE-y (bit rate in Mbps/Gbps), sibnal mode (baseband/broadband), and designator for media type (T = twisted pair copper cable)
- 100BASE-TX Fast Ethernet standard 100 Mbps over Cat 5 or better
- 1000BASE-T is Gigabit Ethernet, over Cat 5e or better. Only switches (no hubs). Mainstream choice for new installations of access networks 
- CSMA/CD host waits random backoff period before attempting to transmit again if data already on cable



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
###
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>



#### Sources & References
