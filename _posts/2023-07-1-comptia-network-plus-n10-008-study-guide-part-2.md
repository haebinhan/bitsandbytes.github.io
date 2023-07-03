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
- Border Gateway Protocol (BGP): path vector EGP, over TCP port 179. For routing domains in mesh internetwork, Iternet's routing protocol between ISPs. An exterior gateway protocol for routers to communicate in separate autonomous systems. Works with classless network prefixes (Network Layer Reachability Information NLRI) and path selection will be based upon hop count, weight, origin, local preference, community, etc. Path vector routing protocol 
- Longest prefix match: longer perfixes preferred for routing if multiple entries to similar networks 
- Administrtive Distance AD value: expresses relative trustworthiness of protocol supplying route. Lower value is more trusted. RIP has AD value of 120 so less trusted 
- Variable Lenth Subnet Masking VLSM: complementary classless addressing technique that allows network engineer to allocate IP address ranges to subnets that match predicted need for subnets/hosts closely

<br>
####  ೃ⁀➷ Installation & Troubleshooting
- Routers link physically remote networks and also subdivide IP networks into subnets 
- Edge routers are at network perimeter. Customer's router is Customer Edge CE, service provider's router is Provider Edge PE
- Internal router: no public interfaces
- Layer 3 capable switch: optimized for routing between VLANs/subinterfaces using static/dynamic routing 
- `route print` on Windows to show routing table
- `traceroute` on Linux using UDP probe messages. Can config to use ICMP echo request instead using traceroute -l
- `tracert` for Windows using ICMP Echo request probes
- Use traceroute/tracert to identify where network path is failing and route/show route comands to check routing tables, if suspecting a problem with router configuration or network topology
- Routing loop: 2 routers use each other as the path to network and they circle around loop until TTL expires. ICMP Time Exceeded errror messages can signify a potential routing loop. TO prevent loops: maximum hop count, holddown timer (updates about declared network unreachable to neighbors discarded during timer for converged info about unreachable network), split horizon (prevent routing update being copied back to source
- Asymmetrical routing: topology where return and forward path are different (common with load balancers or redundant paths). Problematic when return path has higher latency than forward path or if difference between them causes stateful firewall/ NAT devices to drop communications. Can be caused by incorrectly config routes. Use traceroute from both source and destination to compare per hop latency
- Optical link budget/loss budget: amount of loss suffered by components along fiber transmission path using attenuation, connectors, splices. Loss budget should be less than power budget 

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
