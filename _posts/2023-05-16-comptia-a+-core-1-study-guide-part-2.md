---
title: "CompTIA A+ Core 1 220-1101 Study Guide: Part 2/2"
layout: post
date: 2023-05-16
feature_image: images/comptiacore1part2.png
tags: [comptia, a+, studyguide]
---

*Disclaimer: This study guide builds off of my own personal knowledge and was used as my study tool for the exam. As such, any other viewers who see this post will have different beginning knowledge so information may be missing or redundant. As with any exam, multiple study sources are recommended!*

<!--more-->

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

## Table of Contents

1. [Cables and Connectors](#cables-and-connectors)




<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Internet Connections
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Modems

- Used for connection to WAN interface (like Ethernet uses NICs and switches)
- Connects SOHO wireless router to ISP
- Internet Protocol (IP) to identify each network and forward data between

##### Digital Subscriber Line (DSL) Modem
- Uses higher frequencies in copper telephone lines as communications channel
- Advanced modulation and echo cancelling
- High bandwidth full duplex transmissions 

<br>
####  ೃ⁀➷ Cellular Radio Connections 

##### 3G
- area served is called cell
- Range of up to 5 miles
- Global System for Mobile Communication (GSM) subscribers can use removable Subscriber Identity Module (SIM) card to use unlocked handset w/ chosen network provider
- Code Division Multiple Access (CDMA) no removable SIM card and handset/phone directly managed by provider

##### 4G
- Long-Term Evolution (LTE) is series of converged 4G standards 
- Supported by GSM and CDMA network providers both
- Must have SIM card issued by network provider
- Faster speeds 
- Fixed access wireless broadband solution 

##### 5G
- Many smaller antennas 
- Massive Multiple Input Multiple Output (MIMO)
- Faster speeds 
- Fixed access wireless broadband solution 

<br>
####  ೃ⁀➷ Routers
- Uses IP
- Connect local network to the internet 
- Fowards packets using IP addresses (IP address has id of both network and single host w/in network)

<br>
####  ೃ⁀➷ Firewalls
- Filters allowed and denied hosts to control 
- Configured with rules called network access control list (ACL) where each ACL entry lists a source and/or destination network address and protocol type and allow or block
- Unified Threat Management (UTM)


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘




<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### TCP/IP
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Transmission Control Protocol/Internet Protocol (TCP/IP) Suite
- 4 layers
- Application (DHCP, DNS, FTP, HTTP, HTTPS, SMB, SMTP, IMAP, POP3, SSH, RDP, Telnet, LDAP, SNMP, Syslog
- Transport (TCP, UDP)
- Internet (IP)
- Link/Network Interface (Ethernet, Wi-Fi)
- Link layer puts frames on physical network, WAN interfaces, DSL and cable modems. Communications only take place on local network segment. Data is packaged in unit called frame. MAC address
- Internet layer uses IP for packet addressing and routing within network, router, Address Resolution Protocol (ARP) to resolve MAC addresses to IP addresses
- Transport layer determines how hosts manage multiple connections for different appl layer protocols, 
- Transmission Control Protocol: connection oriented forwarding, can identify/recover lost/out of order packets
- User Datagram Protocol: unreliable, connectionless forwarding, faster, less transmission overhead, time-sensitive usage (speech, video)
- Application layer uses protocols that have high-level function, such as those to configure/manage network hosts, or operate services 
- TCP/IP developed by DoD

<br>
####  ೃ⁀➷ Internet Protocol (IP)
- Network and host addressing, packet forwarding between networks 
- Adds headers to data carried in payload 
- Header fields: Source and destination IP address field 
- IPv4: 32 bits long; 4 octets 

<br>
####  ೃ⁀➷ IPv4
- Network ID and Host ID 
- Network ID is common to all hosts on same IP network
- Subnet mask; CIDR format
- Subnet mask will show what is the Network ID (if binary 1 in prefix)
- Forwarding: When sending packet, IPv4 protocol compares source/destination IP against sender's subnet mask: if masked of source/destination match, destination is assumed on same IP network/subnet. Otherwise, route to another network - packet is then forwarded to router (default gateway)

<br>
####  ೃ⁀➷ Public and Private Addresses
- 


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
