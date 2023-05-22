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

1. [Internet Connections](#internet-connections)
2. [TCP/IP](#tcpip)
3. [Ports](#ports)




<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Internet Connections
✧. ┊ ⁭ [Modems](#ೃ⁀-modems) ✧ [Cellular Radio](#ೃ⁀-cellular-radio-connections) ⁭ ⁭┊ .✧

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
✧. ┊ ⁭ [TCP/IP](#ೃ⁀-transmission-control-protocolinternet-protocol-tcpip-suite) ✧ [IP](#ೃ⁀-internet-protocol) ✧ [IPv4](#ೃ⁀-ipv4)✧ [Public/Private](#ೃ⁀-public-and-private-addresses)✧ [IPv6](#ೃ⁀-ipv6)✧ [TCP](#ೃ⁀-transmission-control-protocol)✧ [UDP](#ೃ⁀-user-datagram-protocol) ⁭ ⁭┊ .✧

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
✧. ┊ ⁭ [Common Ports](#ೃ⁀-common-port-numbers) ⁭ ⁭┊ .✧

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
✧. ┊ ⁭ [DHCP](#ೃ⁀-dhcp) ✧ [DNS](#ೃ⁀-domain-name-system) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ DHCP
- DHCP server can allocate IP address/subnet mask to hosts that request
- Scope is range of addresses in a subnet that DHCP can assign, and excludes any statically assigned addresses
- When DHCP client initialize, broadcasts DHCPDISCOVER packet using UDP (server port 67, client port 68). DHCPOFFER, DHCPREQUEST, DHCPACK
- Reserve particular IP address for certain devices - DHCP server can be configured with MAC address list for those to receive same IP address and issue lease for that. Useful for printers, routers, servers, etc since those are easier if IP address is known. Better than static addressing still

<br>
####  ೃ⁀➷ Domain Name System (DNS)
- Basically a translator: resolves human-readable names to computer-readable IP addresses
- Host names should be unique on local network
- Host name, domain name, and suffix: Fully Qualified Domain Name (FQDN) where format is host.domain.suffix where domain.suffix is domain name 'domain' 
- FQDN is assigned by DNS (global name server database)
- Top Level Domains (TLDs) like .com, .net, .gov, .org, .uk, .ca etc
- Managed by ICANN
- Local cache checked first; if not found then query forwarded to local DNS server over port 53. Authoritative Name Server, .net TLD Name Server, Root Name Server 

##### DNS Resource Records
- Each domain needs 1 DNS server to be authoritative information store abt domain, containing resource records
- Resource records allow name server to resolve name and service queries. Can be done manually or generated dynamically
- Address (A) record resolves host name to IPv4 address
- Address (AAAA) record resovles host name to IPv6
- Mail Exchanger (MX) record identifies email server for domain for other servers to send messages to. Can have preference value (lowest is highest preferred) to provide redundancy if more than one. MX record host name must have associated A/AAAA record

##### DNS Spam Management Records
- TXT record stores free form text needed to support other network services
- Single domain can have many TXT records
- Commonly used to block spoofed mail and spam
- Sender Policy Framework (SPF) uses TXT resource record by DNS from email hosting service org
- SPF record meant to identify hosts allowed to send email from domain and indicate what to do with other mail (reject, flag, accept)
- DomainKeys Identified Mail (DKIM) validates source server for email message using cryptography (replace, or addition to SPF). Org upload public key as TXT record in DNS server
- Domain-Based Message Authentication, Reporting, Conformance (DMARC) framework published as DNS TXT record, can use SPF or DKIM or both. Robust policy mechy to specify how DMARC auth failure is treated (flag, reject, quarantine) etc 



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘



<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Services
✧. ┊ ⁭ [File/Print](#ೃ⁀-file--print-servers) ✧ [Web](#ೃ⁀-web-servers) ✧ [Mail](#ೃ⁀-mail-servers) ✧ [Authentication](#ೃ⁀-directory-and-authentication-servers) ✧ [Remote Access](#ೃ⁀-remote-terminal-access-servers) ✧ [Network Monitoring](#ೃ⁀-network-monitoring-servers) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ File & Print Servers
- Fileshare: server disk configured to allow clients to access over network

##### Server Message Block (SMB)
- Application protocol over port 445 using TCP. File and printer sharing for Windows
- SMB3 is current version

##### Network Basic Input/Output System (NetBIOS)
- Earlier Windows used this instead of TCP/IP
- To keep up with TCP/IP as the standard, reworked to work with TCP/UDP called NetBIOS over TCP/IP (NetBT) using UDP 137 for name service and TCP 139 for session service
- NetBT obsolete and should be disabled for security risk

##### File Transfer Protocol (FTP)
- Upload and download files from network server
- Used to upload files to websites 
- Port 21 through TCP
- TCP port 20 to transfer data in active mode or server assigned port in passive mode 
- FTP is unencrypted on its own; high security risk. (FTP-Secure FTPS or FTP over SSH SFTP instead)

<br>
####  ೃ⁀➷ Web Server
- Server that provides client access through HTTP or HTTPS 

##### HyperText Transfer Protocol (HTTP)
- Clients can request resources from HTTP server through port 80 (TCP) and submit a GET request for resource. 
- Serves HTML web pages 
- POST mechanism where user submits data to server 

##### HTTPS
- S for secure
- When TLS used with HTTP (Transport Layer Security)
- Traffic is encrypted between client and server
- TCP and port 443
- For HTTPS, web server installed with digital certificate from CA to prove server identity (public/private key pair)

<br>
####  ೃ⁀➷ Mail Servers

##### Simple Mail Transfer Protocol (SMTP)
- Specify how email delivered from mail domain to another 
- SMTP servers for domain registered in DNS with MX records 
- Port 25 through TCP to message relay between SMTP servers, usually unsecure transmissions
- Port 587 through TCP by mail clients to submit messages for delivery, should use encryption to protect service 

##### Post Office Protocol (POP)
- Mailbox access protocol
- POP client (Outlook, Thunderbird, etc) establish connection to POP server through TCP on port 110 or secure port 995 TCP. User authenticated and mailbox contents are downloaded on local PC then usually deleted from mailbox server 

##### Internet Message Access Protocol (IMAP)
- Mail retrieval protocol
- Support for permanent connections to server, connecting multiple clients to same mailbox simultaneously
- Port 143 TCP. Unsecure 
- IMAP-Secure (IMAPS) Port 993 over TCP, secure

<br>
####  ೃ⁀➷ Directory and Authentication Servers

##### Lightweight Directory Access Protocol (LDAP)
- Directory is a database; object is a record; attributes are fields
- TCP/IP protocol used to query or update X.500 directory (most directories based on X.500 standard)
- UCP and UDP on port 389

##### Authentication, Authorization, and Accounting (AAA) Server
- Consolidates authentication services across multiple access devices 
- Includes Supplicant (device requesting access), a Network Access Server NAS/Network Access Point NAP (switches, access points, VPN gateways, etc) aka AAA clients or AAA authenticators, and an AAA Server which is the authentication server within the local network 
- Makes it so devices don't have to store authentication credentials 
- Often implemented using Remote Authentication Dial-in User Service (RADIUS)

<br>
####  ೃ⁀➷ Remote Terminal Access Servers
- Allows hosts to accept connections to command shell or graphical desktop across the network
- Terminal emulator is software that replicates teletype (TTY) input/output

##### Secure Shell (SSH)
- Secure remote access for Linux and UNIX 
- Also for network appliances like switches, routers, and firewalls 
- Port 22 through TCP

##### Telnet
- Protocol and terminal emulation software tool
- Transmits shell commands & output between remote host and client 
- Port 23 TCP
- Password and communications are not encrypted: unsecure and vulnerable to packet sniffing and replay

##### Remote Desktop Protocol (RDP)
- Microsoft 
- Gives graphical interface rather than just terminal emulation like Telnet/SSH
- Screen and audio data, mouse and keyboard input 
- Port 3389 TCP

<br>
####  ೃ⁀➷ Network Monitoring Servers

##### Simple Network Management Protocol (SNMP)
- Management system and agents
- Agent (process running on switch, server, router, etc) maintains Management Information Base (MIB) which holds statistics for device activity
- Can do trap operation (inform management system of events like failure)
- Device queries: Port 161 UDP
- Traps: Port 162 UDP

##### Syslog
- Protocol and supporting software for log collection
- De facto standard to log events from distributed systems 
- Routers, switches, Linux servers, UNIX servers, etc
- Port 514 UDP

##### Proxy Servers
- Another option besides NAT
- Translates IP addresses, checks and forwards HTTP requests forward and back. 

##### Unified Threat Management (UTM)
- UTM enforces security policies and controls (centralized threat mangement)
- Firewalls allow or block traffic (network ACL with source/destination IP address and ports)
- Intrusion Detection Systems (IDS) has scripts to identify known malicious patterns and raise alerts and take actions
- Antivirus/antimalware, spam gateways, content filters
- Data leak/loss prevention (DLP) will scan outgoing traffic to find info marked confidential/personal and check if authorized transaction; otherwise block

##### Load Balancers
- Distribute client requests across server nodes 
- Web servers, email servers, web conference servers, streaming servers, etc 


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Troubleshooting
✧. ┊ ⁭ [Cable Issues](#ೃ⁀-cable-and-adapter-issues) ✧ [Network Speed](#ೃ⁀-network-speed) ✧ [VoIP](#ೃ⁀-voice-over-internet-protocol) ✧ [Limited Connectivity](#ೃ⁀-limited-connectivity) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Cable and Adapter Issues
- Ethernet has NIC port on host, RJ45 terminated patch cord for host and wall port, structured cable from wall port to patch panel, etc
- Check patch cords properly terminated and also connected to network ports
- Test transceivers in switch port next with loopback tool
- Port flapping: NIC or switch interface has continuous up and down cycles back and forth for internet connectivity 

<br>
####  ೃ⁀➷ Network Speed
- Mismatched duplex settings for network adapter 
- Gigabit Ethernet should be autonegotiate 
- External interference from power lines, motors, generators, fluorescent lighting 
- Crosstalk: poorly installed cabling or termination interference 
- Network adapter driver - any updates available? 

<br>
####  ೃ⁀➷ Voice over Internet Protocol (VoIP)
- Voice calling over network
- Latency: time taken for signal to reach destination in milliseconds 
- VoIP maximum one way latency 150 ms; Round trip time RTT/ two way latency time taken for host to receive response
- Jitter: variation in delay over time, measured by sampling elapsed time between packet arrival. VoIP buffering to tolerate jitter 30ms 
- Quality of Service (QoS) where switches, access points, routers etc configured to prioritize VoIP data over other data 

<br>
####  ೃ⁀➷ Limited Connectivity
- Can establish physical connection to network but no IP config lease from DHCP server 
- APIPA 169.254.x.y range 
- DHCP server, patch cord configuration, VLAN configuration 


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘



<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Cloud and Virtualization 
✧. ┊ ⁭ [NIC](#ೃ⁀-network) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Virtualization
- Sandbox: Isolated environment
- Containerization/container virtualization: Resource separation at OS level with isolated containers for each user instance to run in, with allocated CPU and memory resources. Docker is an example 

<br>
####  ೃ⁀➷ Hypervisor
- Software that facilitates virtualization 
- VMware Workstation, Oracle Virtual Box etc 
- Type 1 hypervisor: bare metal virtual platform installed directonly on computer and manages access w/o host OS. VMware ESXi Server, Microsoft Hyper-V. Hardware needs to support base sys requirements for hypervisor plus resources for guest OSs
- Type 2 hypervisor: Application installed onto host. VMware Workstation, Oracle Virtual Box, etc. Must support host OS and computer needs resources for OS, hypervisor, and guest OSs

<br>
####  ೃ⁀➷ Cloud Deployment 
- Public/multitenant: Cloud Service Providers (CSPs), subscriptions or pay as go, shared resource, risks 
- Private: Private and owned by organization, greater control over privacy and security. Banking, governmental services
- Community: Several orgs share costs of hosted private or full private cloud. Standardization, security policies usage 
- Hybrid

<br>
####  ೃ⁀➷ Cloud Service Models

- Infrastructure as a Service (IaaS): Provision IT resources quickly. Deploy as needed from service provider datacenter 
- Software as a Service (SaaS): Provisioning software applications. Access software hosted on supplier's server pay as go, provision on demand applications quickly, develop and test apps on cloud before deploying on client computers 
- Platform as a Service (PaaS): Between SaaS and IaaS, multi tier web app/db platform but not configured to run application 


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
