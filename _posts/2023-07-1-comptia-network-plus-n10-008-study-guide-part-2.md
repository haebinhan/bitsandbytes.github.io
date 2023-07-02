---
title: "CompTIA Network+ N10-008 Study Guide Part 2/3"
layout: post
date: 2023-07-01
feature_image: images/comptianetworkplus2.png
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
### Routers
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Routing Concepts
- Routing table: info abt location of other hosts and IP networks. Each entry has protocol (source), destination, interface, and gateway/next hop
- Four categories: direct network route, remote routes, host routes (to a specific IP), and default route
- Directly connected route: IP/subnet for every active router interface. Automatically added to routing table
- Static route: Added to routing table manually
- Default route: Special static route that shows next hop router if destination can't be matched on routing table 
- Packet Forwarding: search matching dest network IP in routing table with ARP/ND, forward via gateway over interface by using next hop router MAC in new frame, or forward via gateway over DSL interface then encapsulate packet in appropriate frame type. If not matched, forward via default route, or drop (undeliverable)
- Time to Live TTL: IP header field, decreases by 1 with each router hop. Discarded at 0

<br>
####  ೃ⁀➷ Dynamic Routing Protocols
- Uses algorithm and metrics for routing information database
- Distance vector or link state 
- Convergence: routers with dynamic routing algorithms agree on network topology. 
- Network with routers sharing same topology: steady state. Convergence performance measures time taken to reach steady state
- Autonomous System (AS) admin control of single owner only. Interior Gateway Protocol (IGP) identifies routes within AS. Exterior Gateway Protocol (EGP) advertises routes between ASs
- Routing Information Protocol (RIP): distance vector routing protoocl. IGP, UDP over port 520 or 521. Only considers next hop router to select optimal path. Max size is 15 of RIP networks. RIPv1 classful protocol w/ inefficient broadcasts over UDP port 520, RIPv2 with classless addressing and multicast transmissions UDP 520 w/ authentication, and RIPng next generation for IPv6 UDP port 521
- Enhanced Interior Gateway Routing Protocol (EIGRP): distance vector/hybrid IGP, native IP port 88. Cisco made for routing w/in domain or autonomous sys. Advanced distance vector/hybrid routing protocol, distance vector using neighbor routers, uses metric from admin weighted elements, commonly bandwidth (cost based on lowest bandwidth link in path) and delay (cost based on time takes for packet to travel). Native IP protocol
- Open Shortest Path First (OSPF): link state IGP, native IP port 89. Link state algorithm which lets router to store complete network topology and find least cost path. Good for large organizations w/ many redundant paths, w/ better convergence performance than RIP. Supports classless addressing. Hierarchical. OSPF hello messages, Link State Advertisement (LSA) updates for link state database (LSDB), SPF algorithm. Supports plaintext and cryptographic authentication
- Border Gateway Protocol (BGP): path vector EGP, over TCP port 179. For routing domains in mesh internetwork, Iternet's routing protocol between ISPs. An exterior gateway protocol for routers to communicate in separate autonomous systems 

<br>
####  ೃ⁀➷ Installation & Troubleshooting

<br>
####  ೃ⁀➷



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
