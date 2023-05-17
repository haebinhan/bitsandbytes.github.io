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
✧. ┊ ⁭ [TCP/IP](#ೃ⁀-transmission-control-protocol/internet-protocol-suite) ✧ [IP](#ೃ⁀-internet-protocol) ✧ [IPv4](#ೃ⁀-ipv4)✧ [Public/Private](#ೃ⁀-public-and-private-addresses)✧ [IPv6](#ೃ⁀-ipv6)✧ [TCP](#ೃ⁀-transmission-control-protocol)✧ [UDP](#ೃ⁀-user-datagram-protocol) ⁭ ⁭┊ .✧

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
- Default gateway should be local router interface in dotted decimal if static

<br>
####  ೃ⁀➷ Public and Private Addresses
- Need public IP to communicate on Internet 
- ISP allocate public addresses to customer networks 
- RFC 1918 defines IPv4 range reserved for private addressing where addresses are confined to private LANs. 10.0.0.0 to 255.255.255 (Class A private), 172.16.0.0 to 172.31.255.255 (Class B private), and 192.168.0.0 to 192.168.255.255 (Class C private)
- Class A 255.0.0.0 /8, Class B 255.255.0.0 /16, Class C 255.255.255.0 /24
- Network Address Translation (NAT) converts between private and public addresses for the router in order to access Internet 
- Domain Name System (DNS) resolves host and domain names to IP addresses 
- Dynamic Host Configuration Protocol (DHCP) opposite of static configuration; can assign IP address, subnet mask, default gateway, DNS server addresses
- Automatic Private IP Addressing (APIPA) 169.254.0.1 to 169.254.255.254 for when IP config done by DHCP server but host cannot contact DHCP server
- APIPA address allows host to communicate with hosts on same network that use APIPA (no valid DHCP lease) APIPA aka Link Local

<br>
####  ೃ⁀➷ IPv6
- Hexadecimal notation where one hex digit represents 4 bits (nibble)
- 8 double byte values separated by colons 
- Any leading zeroes in a double byte can be left out. Any double byte with only zeroes can be replaced with double colon marker. 
- 2 equal parts: First 64 bits are Network ID and second half is interface ID. No need for subnet mask
- Global address (like public address) starts with 2 or 3 in hex
- Link-local address (like private address) start with fe80:: in hex
- StateLess Address Auto Configuration (SLAAC) for hosts to obtain global and link-local address via local router automatically (like DHCP)
- Neighbor Discovery (ND) is IPv6 protocol to implement SLAAC and allow host to discover router. Does interface address querying similar to IPv4's ARP. 
- Dual stack is where hosts/routers can use both IPv4 and IPv6 at same time. Host will attempt IPv6 connection first then IPv4

<br>
####  ೃ⁀➷ Transmission Control Protocol (TCP)
- Connection oriented
- SYN, SYN/ACK, ACK 
- Each packet has sequence number for tracking. 
- Main drawback is multiple header fields (size)
- HTTPS and SSH use TCP since cannot tolerate missing info

<br>
####  ೃ⁀➷ User Datagram Protocol (UDP)
- Faster and less reliable 
- Connectionless; no sequencing, no acknowledgements, no guarantee of delivery
- Voice, video
- Used by DHCP and TFTP



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘




<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Ports
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Common Port Numbers
- Port numbers assigned by Internet Assigned Numbers Authority (IANA)

| Port    | Protocol                                          | Usage                                                                          | TCP/UDP |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 20      | FTP - File Transfer Protocol                      | Download files across network                                                  | TCP     |
| 21      | FTP                                               |                                                                                | TCP     |
| 22      | SSH - Secure Shell                                | Secure connection to CLI of server                                             | TCP     |
| 23      | Telnet                                            | Unsecure connection to CLI                                                     | TCP     |
| 25      | SMTP - Simple Mail Transfer Protocol              | Transfer email across network                                                  | TCP     |
| 53      | DNS - Domain Name System                          | ID of hosts by name and IP addressing                                          | TCP/UDP |
| 67      | DHCP - Dynamic Host Configuration Protocol server | Provision IP address config to clients automatically                           | UDP     |
| 68      | DHCP client                                       | Request dynamic IP address config from server                                  | UDP     |
| 80      | HTTP - HyperText Transfer Protocol                | Provision unsecure websites and web services                                   | TCP     |
| 110     | POP - Post Office Protocol                        | Retrieve email message from server mailbox                                     | TCP     |
| 137-139 | NetBIOS over TCP/IP                               | Support network features of legacy Windows                                     | UDP/TCP |
| 143     | IMAP - Internet Mail Access Protocol              | Read, manage mail on server mailbox                                            | TCP     |
| 11      | SNMP - Simple Network Management Protocol         | Query status info from network devices                                         | UDP     |
| 162     | SNMP trap operation                               | Report status info to management server                                        | UDP     |
| 389     | LDAP - Lightweight Directory Access Protocol      | Query info abt network users and resources                                     | TCP     |
| 443     | HTTPS - HTTP Secure                               | Provision secure websites and servers                                          | TCP     |
| 445     | SMB - Server Message Block                        | Implement Windows compatible file and printer sharing service on local network | TCP     |
| 3389    | RDP - Remote Desktop Protocol                     | Secure connection to graphical desktop of computer                             | TCP     |
| 5900    |


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘




<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Configuration
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ DHCP
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
