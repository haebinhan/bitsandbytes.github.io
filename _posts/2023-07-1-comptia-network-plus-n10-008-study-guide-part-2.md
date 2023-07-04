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

1. [Routers](#routers)
2. [Network](#network-topologies)
3. [Transport Layer](#transport-layer-protocols)
4. 


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>


┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Routers
✧. ┊ ⁭ [Concepts](#ೃ⁀-routing-concepts) ✧ [Dynamic Protocols](#ೃ⁀-dynamic-routing-protocols) ✧ [Troubleshooting](#ೃ⁀-installation--troubleshooting) ⁭ ⁭┊ .✧

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


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>



┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Topologies
✧. ┊ ⁭ [3 Tier](#ೃ⁀-tiered-architecture) ✧ [STP](#ೃ⁀-spanning-tree-protocol) ✧ [VLANs](#ೃ⁀-virtual-lans) ✧ [Trunking](#ೃ⁀-trunks) ✧ [Port Tagging](#ೃ⁀-port-tagging) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Tiered Architecture
- Cisco three-tiered hierarchy: access, distibution, core
-  Access/edge layer for end user devices to connect to network connected to switches with star topology
- Distribution/aggregation layer: for fault tolerant interconnections between access blocks and core, or other distribution blocks. Access switch with mesh links to each router/layer 3 switch in its layer block. Traffic policies like routing boundaries, filtering, and QoS. Layer 3 switch uses Application Specific Integrated Circuit ASIC
- Core layer for highly available network backbone and redundant traffic paths. Routers or layer 3 switches

<br>
####  ೃ⁀➷ Spanning Tree Protocol
- STP 
- Bridges and switches organized in hierarchy. Switch with lowest ID (MAC and priority value) selected as root. Switches determine shortest path to root bridge. Bridge Protocol Data Unit BPDU multicast frames.


<br>
####  ೃ⁀➷ Virtual LANs
- VLANs can reduce broadcast traffic 
- Can represent separate zone

<br>
####  ೃ⁀➷ Trunks
- Trunk is the interconnection between switches
- Each switch would have a port config as trunk port

<br>
####  ೃ⁀➷ Port Tagging
- No tag needed if frame addressed to port in same VLAN on same switch
- Needs 802.1Q relevant tag if frame transported over trunk link to identify VLAN
- Switch strips tag before forwarding if receives tagged frame on access port


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>



┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Transport Layer Protocols
✧. ┊ ⁭ [Sockets](#ೃ⁀-sockets) ✧ [Ports](#ೃ⁀-tcp--udp-ports) ✧ [Port Scanning](#ೃ⁀-port-scanning-tools) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Sockets 
- Layer 4 protocols hvae to do w/ delivery of multiplexed application data 
- 0 - 1,023 assigned by IANA to well known server applications, others in 1,024 - 49,151
- Port number w/ source IP address makes a socket, which is bound to software process. One process operate on socket at a time 
- Connection formed when client socket requst service from server socket and uniquely identified by combo of server port, IP address, and client port, IP address. 
- Server socketes can support mult connections from client sockets


<br>
####  ೃ⁀➷ TCP & UDP Ports

| Port | Protocol| Applctn/Servc | Description                           |
| ---------------------------------------------------------------------- |
| 20   | TCP     | ftp-data      | File Transfer Protocol for data       |
| 21   | TCP     | ftp           | File Transfer Protocol for Control    |
| 22   | TCP     | ssh/sftp      | Secure Shell or FTP over SSH          |
| 23   | TCP     | telnet        | Telnet                                |
| 25   | TCP     | smtp          | Simple Mail Transfer Protocol         |
| 53   | TCP/UDP | dns           | Domain Name System                    |
| 67   | UDP     | bootps        | BOOTP/DHCP Server                     |
| 68   | UDP     | bootpc        | BOOTP/DHCP Client                     |
| 69   | UDP     | tftp          | Trivial File Transfer Protocol        |
| 80   | TCP     | http          | Hyper Text Transfer Protocol          |
| 110  | TCP     | pop           | Post Office Protocol                  |
| 123  | UDP     | ntp/sntp      | Network Time Protocol/ Siple NTP      |
| 143  | TCP     | imap          | Internet Message Access Protocol      |
| 161  | UDP     | snmp          | Simple Network Management Protocol    |
| 162  | UDP     | snmp-trap     | SNMP Trap                             |
| 389  | TCP/UDP | ldap          | Lightweight Directory Access Protocol |
| 443  | TCP     | https         | HTTP Secure w/ SSL or TLS             |
| 445  | TCP     | smb           | Server Message Block over TCP/IP      |
| 514  | UDP     | syslog        | Syslog                                |
| 546  | UDP     | dhcpv6-client | DHCPv6 Client                         |
| 547  | TCP     | dhcpv6-server | DHCPv6 Server                         |
| 587  | TCP     | smtps         | SMTP Secure                           |
| 636  | TCP     | ldaps         | LDAP Secure                           |
| 993  | TCP     | imaps         | IMAP Secure                           |
| 995  | TCP     | pop3s         | POP3 Secure                           |
| 1433 | TCP     | sql-server    | MS SQL Server                         |
| 1521 | TCP     | sqlnet        | Oracle SQL *Net                       |
| 3306 | TCP     | mysql         | MySQL/MariaDB                         |
| 3389 | TCP     | rdp           | Remote Desktop Protocol               |
| 5004 | UDP     | rtp           | Real Time Protocol                    | 
| 5005 | UDP     | rtcp          | Real Time Control Protocol            |
| 5060 | TCP/UDP | sip           | Session Initiation Protocol           |
| 5061 | TCP/UDP | sips          | SIP Secure                            |         


<br>
####  ೃ⁀➷ Port Scanning Tools
- IP scanners: will output "host is up" type of messages. Examples: Nmap, AngryIP, PRTG
- Nmap Security Scanner: used for IP scanning (audition and pen testing) open source using CLI or Zenmap GUI
- Give Nmap IP subnet/address to scan, will ping and send TCP ACK packet to 80 and 443 to see if host is present
- netstat command: lets you check tate of ports on local host. Find service misconfigurations, id suspicious remote connections, etc. Outputs active TCP connections 
- Protocol analyzer: works w/ packet capture/sniffer tool to analyze live capture to analyze frames as read, or open saved .pcap captuer file. parses each frame in traffic stream to see header fields and payload contents (packet analysis). Examples: tcpdump for CLI, Wireshark for GUI
- Fingerprinting scan: compare specific responses to known info about hardware platforms, OS, and application/service versions 



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>




┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Services
✧. ┊ ⁭ [NIC](#ೃ⁀-dns) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ DNS
- A record resolves host name to IPv4
- AAAA reesolves host name to IPv6
- CNAME canonical name configures alias for existing A or AAAA 
- MX mail exchange record identifies email server for domain
- SRV service record contains service name and port for application hosted 
- TXT record stores free for mtext needed to support other network services (common SPF and Domain Keys Identified Mil DKIM)
- MX and SRV tpyically have priority/preference values
- Forward lookup zone: contains resource records (aboves) (returns IP address from record/host name)
- Reverse DNS query: returns host name associated with given IP. Stored in reverse lookup zone as PTR record 

<br>
####  ೃ⁀➷ More DNS
- Primary server: zone records held are editable 
- Secondary server: read only copy of zone (zone transfer from primary name server)
- Authoritative name server: holds complete records for a domain (both primary and secondary are authoritative)
- Servers w/o zone (prim or second) are cache-only servers 
- DNS Caching: done by both server and clients, will update record slowly when resource record changed. Hvae to manage carefully to avoid downtime 
- Troubleshoot DNS name res with `nslookup` on windows 
- Domain Information Groper (dig) command queries DNS servers. W/o settings queries DNS root zone. For linux





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
