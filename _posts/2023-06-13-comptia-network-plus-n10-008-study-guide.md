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
3. [IPv4 & IPv6](#ip)

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
✧. ┊ ⁭ [Standards](#ೃ⁀-ethernet-standards) ✧ [Copper](#ೃ⁀-copper-cabling) ✧ [Cat Standards](#ೃ⁀-CAT) ✧ [Ethernet Switching](#ೃ⁀-ethernet-switching-devices) ✧ [Network Interfaces](#ೃ⁀-ethernet-switching-network-interfaces) ✧ [Features](#ೃ⁀-ethernet-switching-features) ✧ [Troubleshooting Ethernet](#ೃ⁀-troubleshooting-ethernet) ✧ [Troubleshooting Cables](#ೃ⁀-troubleshooting-cables) ⁭ ⁭┊ .✧

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
- Interface: means which a node connects to media and exchange data w/ other hosts
- Ethernet frame (PDU) format: Preamble, SFD, Destination MAC, source MAC, Ethernet Type, Payload, FCS
- Preamble and Start Frame Delimiter (SFD): clock synchronization and CMSA/CD. 
- Error checking field has checksum called Cyclic Redundancy Check (CRC) or Frame Check Sequence (FCS)
- MAC/EUI: OUI identifies manufacturer as first six hex digits (first 3 bytes)
- Ethernet frame max length 1518 bytes; frame has 18 byte header (6 byte dest/source MAC, 4 byte error check, 2 byte Ether type); max size of payload 1500 bytes (Maximum Transmission Unit MTU); minimum length of frame 64 bytes (CSMA/CD)

- Packet sniffer: captures frames moving over network
- Protocol analyzer: tool for inspecting traffic received by host/passing over network link
- 3 ways to connect sniffer to network point: SPAN (switched port analyzer/mirror port) sensor attached to specific configured port on switch that receives copies of frames, not completely reliable; TAP (passive test access point) box with ports for incoming/outgoing network cable and inductor to physically copy signal from cabling, unlike SPAN gets corrupt frames and unaffected by load; Active TAP powered device performing signal regeneration, point of failure for links
- tcpdump: linux command giving user interface for libpcap library (tcpdump -i eth0) is syntax: eth0 is interface to listen on. Ex: `tcpdump -i eth0 "dst host 192.168.1.1 and (dst port 53 or dst port 80)"` where frames are filtered for dest IP 192.168.1.1 and dest port 53 or 80
- Wireshark: open source graphical packet capture & analysis utility. Top pane shows each frame, middle pane shows fields from frame, bottom pane shows raw data from frame 

<br>
####  ೃ⁀➷ Ethernet Switching Features
- Switches: Unmanaged vs managed, stackable, modular vs fixed, desktop vs rack mount
- Cisco 3 principal modes: User EXEC mode (read only), Privileged EXEC mode/enable mode (can reboot, shut down, backup, restore), Global config mode (can write config updates)
- `show config` to display switch config, `show interface` to list all interfaces and state 
- MAC/CAM address table. If address not found in table, switch acts like hub: frame transmitted out all ports besides source port (called flooding). MAC address table can be queried with `show mac address-table`
- Port security config validates MAC addresses. Can learn static MACs and also have enforcement actions if policy violation
- Port aggregation: Combine 2+ cabled links into single logical channel, aka NIC teaming/bonding. Link Aggregation Control Protocol (LACP) autonegotiate bonded link between end sys and switch ports, detect config errors, and recover faiure of physical link
- Port mirroring: switches only forwards unicast traffic to intended destination interface to prevent sniffing, unlike hubs. Port mirroring helps analyze network traffic by copying all packets sent, to a mirror/destination port. Called Switched Port Analyzer (SPAN) on Cisco switches
- Jumbo frame: supports data payload upto 9k bytes (reduce number of frames needing to be transmitted/amount of processing). To use jumbo frame: all hosts in path must support, be configured, and support same MTU
- Flow control: Lets server instruct switch to pause traffic to avoid overwhelming buffer (which then drops frames) 
- Power over Ethernet (PoE): supply electric power from switch port overcable to connected powered device (PD) like VoIP headset, IP camera, AP. 802.3af is 13W over lilnk, 802.3at (PoE+) 25W, 802.3bt (Ultra PoE) 51W or 73W. PoE switches aka endspan/endpoint power sourcing equpiment (PSE)

<br>
####  ೃ⁀➷ Troubleshooting Ethernet
- Identify problem, Establish theory, Test theory, Establish plan of action, Implement solution/escalate, Verify sys functionality, Document Findings. 
- Identify: identify symptoms, duplicate problem
- Establish theory: Top to bottom, bottom to top, divide and conquer (in regards to the OSI model)

<br>
####  ೃ⁀➷ Troubleshooting Cables
- Symbol: a series of events, physical layer signal transmitted (ex: pulse of higher voltage, transition between peak/trough. Symbols transmitted per second is baud rate measured in hertz 
- Speed: expected performance of properly installed links (to operate at 10, 100 Mbps, 1 Gbps, etc)
- Throughput: average data transfer rate achieved over period of time (excludes encoding schemes, errors, and other losses) adversely affected by link distance, interference, noice, etc
- Distance limitations, attenuation (loss of signal strength in decibels (dB) ratio of signal strength origin:destination, noise (transmitted signals that aren't teh intended signal) expressed as signal to noise ratio (SNR)
- Physical: network tranceiver, patch cable, structured cable, patch cable, etc
- Loopback adapter/plug: RJ-45 packet sent by NIC received by self, used to test network cards and for bad ports
- LED status indicators: solid green (connected but no traffic), flickering green (normal), no light (not working), blinking amber (fault detected), solid amber (blocked by spanning tree algorithm)
- Cable tester: detailed info on phys & elec properties of cable such as crosstalk, cable condition, attenuation, noise, resistance, etc. May have time domain reflectometer (TDR) which measures length of cable run and can locate imperfections in cables 
- Multimeter: check hysical connectivity by testing electrical circuits 
- Wire map tester can identify continuities, shorts, incorrect pin/termination, etc
- Tone generator/probe: traces cables from one end to the other 
- Decibel loss/insertion loss
- Electromagnetic interference (EMI)/alien crosstalk
- Crosstalk usually due to bad wiring, connector, or termination. Measured in dB and higher values represent less noise (opposite of insertion loss). Near End (NEXT) measures crosstalk, usually caused by excessive untwist of pairs or faulty bonding; Attenuation to Crosstalk Ratio Near End (ACRN) is difference between insertion loss and NEXT where ACR is equivalent to signal to noise ratio (SNR); Attenuation to Crosstalk Ratio Far End (ACRF) where far end crsosstalk (FEXT) measured on receive pairs at recipient end (NEXT is at transmitter end) and diff between insertion loss and FEXT gives ACRF; Power sum confirms cable is suitable for application
- Straight through cable: terminated with same T568x, used for uplink (MDI port to MDIX port)
- Crossover cable: one end has T568A and other has B. Used to connect end system host to another host or hub to hub. Nowadays switches have uplink port though so crossover not usually needed due to auto-MDI/MDI-X
- Rollover/Console Cable: connects PC to CLI of switch or router using RJ-45 (DB-9 for legacy)
- Optical Time Domain Reflectometer (OTDR) uses light pulses down cable and times it to find breaks in the cable and break location
- Optical Spectrum Analyzer (OSA) used with wavelength division multiplexing (WDM) to make sure each channel has enough power

└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### IP
✧. ┊ ⁭ [NIC](#ೃ⁀-ipv4) ✧ [Hub](#ೃ⁀-forwarding) ✧ [Switch](#ೃ⁀-subnet) ✧ [Hub](#ೃ⁀-tools-and-troubleshooting) ✧ [Hub](#ೃ⁀-ipv6) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ IPv4
- IP protocols: ICMP/1 for status messaging and connectivity testing, Internet Group Management Protocol (IGMP/2) for multicasting, Generic Routing Encapsulation (GRE/47) for tunneling packets across intermediate network or VPNs, Encapsulating Security Payload (ESP/50) and Authentication Header (AH/51) for encrypted IP (IPSec), Enhanced Interior Gateway Routing Protocol (EIGRP/88) and OSPF (OSPF/89) for routers to exchange information about paths to remote networks 
- Network ID and Host ID. 32 bits long or 4 bytes/octets. Dotted decimal notation.
- Network mask shows diff between net and host ID by concealing host ID and revealing network ID. If 1 in mask, corresponding binary digit in IP is part of network ID. Net ID found by ANDing mask to IP. If two 1s AND together, = 1 while anything else is a 0. Do so by converting dotted decimal notation to binary, AND, then convert back to dotted decimal. 
- Prefix/slash notation
- Longer network portion (255.255.255.0 compared to 255.0.0.0 for example) means more network IDs in network but fewer available host addresses per network while shorter means millions of hosts per network but fewer possible network addresses 
- Network ID and subnet ID use different masks: whole network mask will be regular mask and hosts within the network may use the subnet mask which can be non 255 or 0s such as 255.255.255.240. This means the subnet info mask is only used inside the IP network while external IP networks will address the whole network by the network ID and mask (hosts inside network use longer mask to differentiate)
- 128, 192, 224, 240, 248, 252, 254, 255
- Block size: 2 ^ number of bits allocated to host. For example, /13 has max of 16 bits in first 2 octets, so 2 ^ (16-13) = 8 block size.
- To find possible host ID number: 2^n values where n is the number of bits in host ID (can find by subtracting CIDR from 32). This means a /24 has 8 bits in the host ID, so 256 possible values from (2^8) but first address is network address and last address is reserved as broadcast so 254 possible host. Or, subtract least significant octet from 256 (for example 256-192=64, subtract 2 for network/broadcast addresses so 62 in the case of a subnet mask of 255.255.255.192)
- purpose of subnetting: create layer 3 broadcast domain segment with fewer hosts. each bit added to mask will halve number of available host address (approximately)

<br>
####  ೃ⁀➷ Forwarding
- Layer 2 forwarding called switching; Layer 3 forwarding called routing
- Source and destination address are compared against netmask through IPv4; if masked portions match then destination assumed to be on same IP subnet/network
- Address Resolution Protocol (ARP) resolves IP address to MAC addresses w/ requests and replies
- Unicast: single recipient; Broadcast: multiple hosts by sending to network/subnet's broadcast address (last address in any network). Switches flood broadcasts out of every port besides source port 
- Multicast: any host can send to other hosts that are identified; sent to destination IP address from special range configured for multicast use and swithc must be multicast capable (if not, then treated like broadcast and flooded out of all ports). Intent to receive multicast from host: join multicast group using Internet Group Management Protocol (IGMP) to config group membership and IP address
- Anycast: group of hosts config with same IP address; When packet forwarded a prioritization algorithm selects 'closest' host, for load balancing and failover 

<br>
####  ೃ⁀➷ Subnet
- Class A: 1-126, /8
- Class B: 128-191, /16
- Class C: 192-223, /24
- Class D: 224.0.0.0 to 239.255.255.255 for multicasting
- Class E: 240.0.0.0 to 255.255.255.255 for experimental use and testing
- Private IPs: A 10.0.0.0 to 10.255.255.255, B 172.16.0.0 to 172.31.255.255, C 192.168.0.0 to 192.168.255.255
- Loopback address: 127.0.0.0 to 127.255.255.255, to check TCP/IP correctly installed on local host

<br>
####  ೃ⁀➷ Tools and Troubleshooting
- Windows `netsh` command to configure interfaces. `netsh interface ip set address "Ethernet" dhcp` or `netsh interface ip show config` to report IP config. Legacy command prompt. For scripts use PowerShell cmdlets like `Get-NetAdapter` or `Get-NetIPAddress` 
- Windows `ipconfig`, `/renew [interface] will force DHCP client to renew IP address lease, `ipconfig /release [interface] ` will release IP address from DHCP Server, `/displaydns` displays DNS resolver cache, `/flushdns` clearns DNS resolver cache, and `/registerdns` registers host with DNS server
- ARP used by hosts to see which MAC is associated with which IP, using broadcasts in an ARP table. Can use to disagnose suspected problem w/ local addressing or packet delivery
- `arp -a` will show ARP cache contents, `arp -s [IPAddress] [MACAddress]` adds entry to ARP cache, `arp -d *` will delete all aentries in ARP cache
- Linux: `ip neigh` command shows entries in local ARP cache (old command was `arp`)
- ICMP report errors and sends messages about delivery of packet, error conditions for unicast traffic. Ping: round trip time RTT: measure of latency between host sending probe and receiving reply 
- Good order sequence: ping loopback, ping host, ping gateway, ping remote host, ping host name, establish session. First ping loopback to verify TCP/IP is installed and working. Then ping IP address of local host to verify that was added correctly and network adapter is working, if doesn't work then config error, or faulty network adapter/driver. Next ping IP address of default gateway to verify you can communicate with hosts on local network, then ping other hosts on same subnet to check local config or link problems. Then ping a remote host to verify communication works through the router, if not then check default gateway on local host, then routing infrastructure.


<br>
####  ೃ⁀➷ IPv6
- 2-3 elements: fixed length Main header, optional extension headers, and payload. Can also have traffic class (packet priority), flow label, payload length, next header, and hop limit (like TTL field)
- eight 16 bit numbers (each double byte is 4 hex digits) with colons to separate 
- Canonical notation: if double byte has leading 0s, can be left out. One whole double byte of 0s can be replaced with a double colon place marker
- IPv6 used as URL must be surrounded by brackets 
- First64 bit half is net ID, last 64 bit half is interface/host ID
- Unicast, multicast, anycast. No broadcast
- Global scope: equivalent of public IPv4, first 3 bits (001) indicate. Will start with 2 or 3 in hex 
- Link local: IPv4 private equivalent, range is fe80::/10, starting with leading fe80, next 54 bits set to 0, then last 64 bits the interface ID. E#quivalent to IPv4 APIP. Also has a zone index/scope ID
- Neighbor Discovery Protocol and Router Advertisements (ND) protocol: similar to ARP and ICMP for IPv4. Does address autoconfiguration (enable host to config IPv6 for interfaces automatically and detect if address is already in use on local net by using neighbor solicitation NS and neighbor advertisement NA messages), prefix discovery (host can discover known network prefixes allocated to local segment, next hop determination, router solicitation RS and router advertisement RA messages), local address resolution (allow host to find other nodes/routers on local network called neighbors using NS and NA messages), and redirection (router can inform host of better troutes to destinations)
- Stateless Address Autoconfiguration (SLAAC) like DHCP, host generates link local address and tests it is unique using ND, then listens for router advertisement RA and router will give network prefix or direct to DHCPv6 server
- ICMPv6: updated ICMP with error messaging (Packet Too Big class error, routers are not responsible for packet fragmentation and reassembly), informational messaging (ND, Multicast Listener Discovery MLD)
- Multicast first 8 bits are 11111111 or f. Broadcast addresses not implemented (multicast instead)
- Dual stack: can run both IPv4 and 6
- Tunneling: alternative dual stack, delivers IPv65 packets across IPv4 networks by inserting 6 into 4 packets and routing 
- Generic Routing Encapsulation GRE is tunneling alternative w
- Prefixes: link local unicast fe80::/10, global unicast 2000::/3, multicast ff00::/8, multicast link local ff02::/16, unspecified ::/128, loopcack ::1/128, documentation/examples 2001:db8::/32
- Extended Unique Identifier (EUI) is essentially a MAC address


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
