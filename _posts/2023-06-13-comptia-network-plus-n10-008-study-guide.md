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
2. [Ethernet](#ethernet)

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
- Essentially: application, SSL encryption, link presentation to transport layer, TCP encapsulation, IP encapsulation, Ethernet, electrical signals 
- TCP flags: Header identifies payload, set of bits (TCP flags). Flags control payload (SYN, PSH, RST, FIN, etc)
- Maximum Transmission Unit (MTU): maximum IP packet to transmit but not fragment (which slows things down - lose fragment = lose entire packet)

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
✧. ┊ ⁭ [Standards](#ೃ⁀-ethernet-standards) ✧ [Copper](#ೃ⁀-copper-cabling) ✧ [Fiber Optic](#ೃ⁀-fiber-optic-cabling) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Ethernet Standards
- 802.3 Ethernet standards by IEEE
- 3 part convention xBASE-y (bit rate in Mbps/Gbps), sibnal mode (baseband/broadband), and designator for media type (T = twisted pair copper cable)
- 100BASE-TX Fast Ethernet standard 100 Mbps over Cat 5 or better
- 1000BASE-T is Gigabit Ethernet, over Cat 5e or better. Only switches (no hubs). Mainstream choice for new installations of access networks 
- CSMA/CD host waits random backoff period before attempting to transmit again if data already on cable

<br>
####  ೃ⁀➷ Copper Cabling
- Copper wire twisted pair (popular)
- UTP (unshielded twisted pair)
- STP less susceptible to interference/crosstalk
- S/FTP cable: shielded twisted pair; braided outer screen and foil shielding
- CAT Cable standards: categories of cable standards for twisted pairs
- EIA/TIA 568A & B (TIA568A: GW, G, OW, B, BW, O, BrW, Br; TI568B: OW, O, GW, B, BW, G, BrW, Brd)
- American Wire Gauge (AWG): measurement standard for wire thickness
- Coaxial

##### CAT

| Ethernet Standard        | Cat Class | Bandwidth Capacity | Max Distance  | Frequency | Connector | Cable Type               |
| ---------------------------------------------------------------------------------------------------------------------------- |
| 10BASE-T                 | Cat 3     | 10 Mbps            | 100 m         | 16 MHz    | RJ-45     | UTP                      |
| 100BASE-TX               | Cat 5     | 100 Mbps           | 100m          | 100 MHz   | RJ-45     | UTP                      |
| 1000BASE-T               | Cat 5e    | 1000 Mbps          | 100 m         | 100 MHz   | RJ-45     | UTP or F/UTP             |
| 1000BASE-TX or 10GBASE-T | Cat 6     | 1 Gbps             | 100 m or 55 m | 250 MHz   | RJ-45     | UTP, F/UTP, U/FTP        |
| 10GBASE-T                | Cat 6a    | 10 Gbps            | 100 m         | 500 MHz   | RJ-45     | UTP, F/UTP, U/FTP, S/FTP |
| 10GBASE-T                | Cat 7     | 10 Gbps            | 100 m         | 600 MHz   | GG45/TERA | S/FTP, F/FTP             |
| 40GBASE-T                | Cat 8/8.1 | 40 Gbps            | 30 m          | 2000 MHz  | RJ-45     | U/FTP, F/UTP             |
| 40GBASE-T                | Cat 8.2   | 40 Gbps            | 30 m          | 2000 MHz  | GG45/TERA | F/FTP, S/FTP             |


<br>
####  ೃ⁀➷ Fiber Optic Cabling
- Not easily intercepted/interference; less attenuation
- Higher bandwidth over longer cable 
- SMF Single Mode Fiber: small core, long wavelength, by laser
- MMF Multimode Fiber: larger core, shorter wavelength, less expensive, but doesn't support high signaling speeds or long distances as SMF
- ST Straight Tip: early bayonet style connector with push-and-twist locking mechanism usually for multimode networks
- SC Subscriber Connector: push/pull design for simple insertion/removal. Gigabit Ethernet
- LC Local Connector/Lucent Connector: small form factor, tabbed push/pull. Similar to SC but smaller. Gigabit Ethernet
- MTRJ Mechanical Transfer Registered Jack: Small form factor duplex connector, snap in design, multimode networks
- Small Form Factory Pluggable (SFP): LC connectors and Gigabit Ethernet
- Quad Small Form Factor Pluggable (QSFP) transceiver form factor for 4 x 1 Gbps links
- BiDirectional Wavelength Division Multiplexing (BiDi WDM): BiDi transceivers transmit/receive signal over same strand of fiber. Ethernet 1000BASE-BX and 10GBASE-BX
- Coarse Wavelength Division Multiplexing (CWDM): 4-8 bidirectional channels over single fiber strand.Dense Wavelength Division Multiplexing (DWDM) greater numbers of channels (less spacing between channels and more precise/expensive lasers)
- Physical Contact (PC): fiber tip/connector polished to fit better and reduce return loss (light reflecting back interference)
- UltraPhysical Contact (UPC): higher standard polish
- Angled Physical Contact (APC): even tighter connection, better loss performance

<br>
####  ೃ⁀➷ Ethernet Switching Devices
- Repeater: overcomes signal distance limitation by boosting signal at a point in the cable run; Layer 1 of OSI; connects cable segments of same type
- Media converter: transition one cable to another media type cable; physical layer; Single mode fiber to twisted pair, multimode fiber to twisted pair, single mode to multimode fiber, etc
- Hub: Central intermediate system; phys layer, half duplex, CSMA/CD; needs medium dependent interface (MDI) (end system interface); no config options
- Bridge: data link layer; establish separate phys network segments while keeping nodes on same logical network to reduce number of collisions; isolates segments and forwards only appropriate traffic; MAC address table
- Switches: layer 2; same as bridge but more; each port is separate collision domain

<br>
####  ೃ⁀➷ Ethernet Switching: Network Interfaces


<br>
####  ೃ⁀➷ Ethernet Switching Features

<br>
####  ೃ⁀➷ Troubleshooting Ethernet

<br>
####  ೃ⁀➷ Troubleshooting Cables




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
