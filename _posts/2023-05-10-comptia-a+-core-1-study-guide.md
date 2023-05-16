---
title: "CompTIA A+ Core 1 220-1101 Study Guide"
layout: post
date: 2023-05-10
feature_image: images/comptiacore1.png.png
tags: [comptia, a+, studyguide]
---

*Disclaimer: This study guide builds off of my own personal knowledge and was used as my study tool for the exam. As such, any other viewers who see this post will have different beginning knowledge so information may be missing or redundant. As with any exam, multiple study sources are recommended!*

<!--more-->

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

## Table of Contents

1. [Cables and Connectors](#cables-and-connectors)
2. [Motherboard](#motherboard)
3. [Installing Hardware](#installing-hardware)
4. [Troubleshooting: PC Hardware](#troubleshooting-pc-hardware)
5. [Networks](#networks)
6. [Network Hardware](#network-hardware)
7. [Network Cables](network-cables)
8. [IEEE 802.11 & Access Points](#ieee-802.11--access-points)


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Cables and Connectors
✧. ┊ ⁭ ⁭[USB](#ೃ⁀-universal-serial-bus-usb) ✧ [Video](#ೃ⁀-video-interfaces/cables) ✧ [SATA](#ೃ⁀-hard-drive-to-motherboard-cables) ✧ [Legacy Cables](#ೃ⁀-legacy-cables) ⁭ ⁭┊ .✧

<br>
#### ೃ⁀➷ Universal Serial Bus (USB)
##### USB Connector Types, 2.0
- Type A
- Type B (for large devices such as printers)
- Mini B (typically for older digital cameras)
- Micro B (small devices like phones)

##### USB Connector Types, 3.0 & 3.1
- Type A
- Type B
- Micro B
- Type C

<br>
#### ೃ⁀➷ Video Interfaces/Cables
##### High-Definition Multimedia Interface (HDMI) 
- a video interface; widely used
- supports video, audio, remote control
- Regular full size Type A, mini Type C, micro Type D
- requires 1 video card port for each monitor connected (downside)

##### DisplayPort Interface 
- similar to HDMI
- advantage is support for daisy-chaining multiple monitors to same video source

##### Thunderbolt Interface
- display interface or general peripheral interface (like USB)
- compatible with DisplayPort
- lightning bolt icon
- Thunderbolt v.3 uses same connector as USB-C cable

<br>
#### ೃ⁀➷ Hard Drive to Motherboard Cables
##### Serial Advanced Technology Attachment (SATA) Interface
- standard; connect internal storage drives
- 1 m cables; 7-pin connectors
- singular device per cable
- a 15-pin SATA power connector connects the device to PC power supply as 7-pin data connector does not supply power

##### External SATA (eSATA)
- 2 m
- eSATA is to connect to external eSATA port
- powered port, compatible with USB and SATA

##### Molex Power Connector
- 4 pins, white or clear plastic
- legacy components
- used for storage devices that need more power 

<br>
#### ೃ⁀➷ Legacy Cables
##### Digital Visual Interface (DVI) 
- video interface supporting both analog (CRT screens) and digital outputs 
- DVI-I suports both, DVI-A supports only analog, DVI-D supports only digital

##### Video Graphics Array Interface (VGA)
- video interface
- 15-pin

##### Small Computer System Interface (SCSI) 
- legacy parallel bus (parallel data transmission)
- one host bus can control multiple attached devices
- both internal/external peripherals
- 68 pin & 80 pin
- commonly used to connect hard disk

##### Integrated Drive Electronics Interface (IDE) 
- mass storage interface for PC
- aka Parallel Advanced Technology Attachment (PATA)
- Extended IDE (EIDE) uses 16 bit parallel data transfers

##### Serial Cables (RS-232)
- serial port (aka COM port; communications) is for data to be transmitted over one wire, one bit at a time
- start, stop, parity bits to format/verify data transmission
- connecting external modems, establish dial-up connections
- RS-232 has 25 pin hardware interface, but DB-9 9pin typically used


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Motherboards
✧. ┊ ⁭ [Parts](#ೃ⁀-parts) ✧ [DIMM](#ೃ⁀-dual-inline-memory-module) ✧ [PCIe](#ೃ⁀-peripheral-component-interconnect-express-interface) ✧ [Expansion Cards](#ೃ⁀-expansion-cards) ✧ [Form Factors](#ೃ⁀-motherboard-form-factors) ⁭ ⁭┊ .✧

<br>
##### ೃ⁀➷ Parts
- CPU socket (CPU, thermal paste, heat sink, fan)
- Memory slots (Random-access memory RAM)
- Disk drive connectors
- I/O Ports (USB, audio, video)
- Adapter card slots
- SATA ports
- Power connector is 2 pin x 12 pin block with square pin receptacle

<br>
##### ೃ⁀➷ Dual Inline Memory Module (DIMM)
- system RAM
- DDR3, DDR4, DDR5
- form factor depends on version

<br>
##### ೃ⁀➷ Peripheral Component Interconnect Express Interface (PCIe)
- interface for modern adapter cards/expansion cards (GPUs, RAID, WiFi, SSD, etc)
- point-to-point serial communications (each component can have dedicated link to other component)
- x16 PCIe slot, x8 PCIe slot, x4, x1 (number of lanes)
- can insert smaller into port with greater # of lanes (called up-plugging)

<br>
##### ೃ⁀➷ Expansion Cards
- Video card/graphics adapter has Graphics Processing Unit (GPU) and Graphics memory and video ports (HDMI, DisplayPort, Thunderbolt, etc)
- Graphics card typically uses PCIe x16 interface slot
- Network Interface Card (NIC) with RJ-45 port

<br>
#### ೃ⁀➷ Motherboard Form Factors
- shape, layout
- Advanced Technology Extended (ATX) standard form factor for desktop
- Micro-ATX (mATX) smaller
- Information Technology Extended (Mini-ITX) form factor, most can be mounted in ATX cases too
- nano, pico, mobile ITX form afctors for embedded systems and portable devices
- Small Form Factor (SFF) PC often uses Mini-ITX; popular as home machine/mini server

| Form Factor | Size (in.)  | Notes             |
| --------------------------------------------- |
| ATX         | 12 x 9.6    | 7 expansion slot  |
| Micro-ATX   | 9.6 square  | 4 expansion slot  |
| Mini-ITX    | 6.7 square  |                   |



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Installing Hardware
✧. ┊ ⁭ [PSU](#ೃ⁀-power-supply-units) ✧ [PSU Adapters](#ೃ⁀-power-supply-adapters) ✧ [Fan/Cooling](#ೃ⁀-fan/cooling-systems) ✧ [Storage/RAID](#ೃ⁀-storage-devices--raid) ✧ [RAM](#ೃ⁀-ram) ✧ [CPU](#ೃ⁀-central-processing-unit) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Power Supply Units (PSU)
- delivers direct current (DC) low voltage power to PC components 
- contains rectifier to convert alternating current (AC) into DC, transformers to step down to lower voltage, filters and regulators for consistent output voltage, and fan to dissipate generated heat
- PSU needs to meet combined power requirements of components
- Output capability measured in Wattage Rating (standard PC is 200-300W, enterprise/workstation/servers are typically over 300, gaming may require more)

####  ೃ⁀➷ Power Supply Adapters
- Multiple power connectors supply DC voltage from PSU to motherbvoard/devices at 3.3 VDC, 5 VDC, 12 VDC
- Voltage regulators used to correct supplied voltage to exact voltage required by components 
- Power port on motherboad is P1 Connector
- PSU has Molex/SATA power connectors also, and 4/6/8 pin connectors for CPU, PCIe ports
- Original ATX specification, P1 connector was 20 pin (2x10). Nowadays most are ATX12V version 2 specificatoin, a 24 pin (2x12) P1 form factor
- A modeular PSU has detachable power connector cables to reduce # of cables and improve airflow
- Two PSUs in 1 case; extra can be redundant power supply
- Entry-level Power Supply (EPS) specification for server hardware has 8pin 12V connections with 4 yellow and 4 black wires
- SATA connector has 2 types: red flat cable for data, multi-colored cables for power (5V and 12V, a fifth orange wire adds 3.3V power)
- Molex KK connector connects fan to motherboard, with 5V or 12V. 3 circular pins in order of black, yellow, red
- P1 adapter is primary PSU to motherboard connector. Long, 2 pin wide, 24 pin (20+4) connector with black, yellow, orange, red wires (12V, 5V, and 3.3V)
- Molex connector is white with 4 pins and red, yellow, black wires. Power to peripheral devices inside the system case. 5V and 12V

<br>
####  ೃ⁀➷ Fan/Cooling Systems
- all CPUs require cooling
- Heat sink is block of copper/aluminum with fins; glued to surface of CPU with thermal paste
- Heat sink is passive cooling
- Fan improves airflow to dissipate heat; must be plugged into motherboard fan power port
- Liquid-based Cooling System pumps water around chassis for extra cooling (gaming PCs) and can be quiter than fans

<br>
####  ೃ⁀➷ Storage Devices & RAID

##### Storage Devices
- M.2 SSD is physical form factor; supports both SATA And NVMe interfaces
- HDD form factor: 3.5 inch main, laptop: 2.5 inch

##### Redundant Array of Independent Disks (RAID)
- RAID gives fault intolerance in return for disk capacity
- RAID appears as single storage resource/volume; acts like a drive (parititoning/formating)

| RAID    | Desc                             | Redundant? | Fault tolerant? |
| ------------------------------------------------------------------------- |
| RAID 0  | Striping w/o Parity              |    No      |      No         |
| RAID 1  | Mirroring| 4 expansion slot      |    Yes     |      Yes        |
| RAID 5  | Striping w/ Distributred Parity  |    Yes     |      Yes        | 
| RAID 10 | Stripe of Mirrors                |    Yes     |      Yes        |

RAID 0: Striping without Parity
- Data striping divides data into blocks 
- Blocks are spread in fixed order among disks in the array
- Improves performance (mult disks are available to service requests)
- Requires at least 2 disks 
- Provides NO redundancy (if any physical disk fails, whole logical volume fails) 
- Typically used as non-critical cache store

RAID 1: Mirroring
- Two disks; mirrored drive configuration
- Write operations: data written to both disks simultaneously
- Read operations can use either disk 
- Simplest way to protect single disk against failure. If disk fails, other disk takes over
- More costly as disk space utilization is 50%
- Redundant 

RAID 5: Striping with Distributed Parity
- Striping with distributed parity (error correction information spread across all disks)
- Data and parity are always on different disks 
- When single disk fails, enough info spread across other disks for data to be reconstructed 
- Best performance for read operations (unless disk failed)
- Write operations have reduced performance 
- Minimum 3 drives
- Fault tolerance vs available disk space are inverses (more disks, less fault tolerance and more usable disk space) 

RAID 10: Stripe of Mirrors
- Nested RAID configuration (combines features of two RAID levels) 
- Logical striped volume (RAID 0) with two mirrored arrays (RAID 1)
- Excellent fault tolerance (one disk in each mirror can fail and volume still works) 
- Minimum 4 disks, must be even. Also costly like RAID 1

<br>
####  ೃ⁀➷ RAM

##### Virtual RAM
- Virtual memory/RAM is total amount of addressable memory (system RAM plus swap space)
- Extend memory space using disk storage if not enough system RAM (called pagefile or swap space) 
- OS assigns memory locations to processes using 4kB chunks (pages) 
- Inactive pages moved to swap space to free physical RAM

##### Double Data Rate Synchronous Dynamic Random Access Memory (DDR SDRAM)
- modern system RAM
- two data transfers per motherboard clock cycle
- DDR for desktop form factor is DIMM
- Notches depict generation (DDR3, DDR4, etc) Slots on motherboard must match
- Laptop RAM is smaller form factor Small Outline DIMM (SODIMM)

| RAM   | Data Rate MT/x  | Transfer Rate GB/s | Max Size GB |
| ---------------------------------------------------------- |
| DDR3  | 800 - 2133      | 6.4 - 17.06        | 8           |
| DDR4  | 1600 - 3200     | 12.8 - 25.6        | 32          |
| DDR5  | 4800 - 6400     | 38.4 - 51.2        | 128         | 

- Single-channel memory: only one 64 bit data bus for CPU, memory controller, and RAM
- Dual-channel memory controller: 2 64bit pathways (128 bits of data per transfer), only regular RAM (no dual channel DDR)
- Error correcting code (ECC RAM) RAM is used for workstations/servers that need high reliability
- ECC RAM does hash calculation on data value on each trasnfer; stores as 8 bit checksum 
- Most ECC are Registered DIMMs (RDIMMs) with extra component to reduce electrical load from memory controller
- Motherboard and CPU must support ECC 
- Motherboard supports either UDIMMs or RDIMMs (unbuffered DIMMs are mostly non-ECC)
- If motherboard supports UDIMM and RDIMM both, cannot mix and match

<br>
####  ೃ⁀➷ Central Processing Unit (CPU)
- simultaneous multithreading (SMT) (or HyperThreading for Intel) is where multiple parallel threads are run in a process 
- Multi-sockets: CPU must be identical
- thread is a stream of instructions 
- Intel and AMD use different socket types
- Zero insertion force (ZIF) mechanism for CPU sockets; do not force CPU in
- Land Grid Array (LGA) socket form factor positions pins on CPU socket. Used by Intel
- Pin Grid Array (PGA) form factor positions pins on bottom of processor. Used by AMD. Check that pin 1 is aligned properly
- Virtualization depends on CPU model


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Troubleshooting: PC Hardware
✧. ┊ ⁭ [Troubleshooting Model](#ೃ⁀-comptia's-a-troubleshooting-model) ✧ [BIOS & UEFI](#ೃ⁀-basic-inputoutput-system-&-unified-extensible-firmware-interface) ✧ [POST](#ೃ⁀-power-on-self-test-issues) ✧ [Power](#ೃ⁀-power-issues) ✧ [Drive](#ೃ⁀-drive-issues) ✧ [Performance](#ೃ⁀-performance-issues) ✧ [Display](#ೃ⁀-display-issues) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ CompTIA's A+ Troubleshooting Model
1. Identify the problem
2. Establish a theory of probably cause
3. Test the theory to determine the cause
4. Establish a plan of action to resolve the problem& implement the solution
5. Verify full-system functionality and, if applicable, implement preventive measures
6. Document the findings, actions, and outcomes
(I Eat Tacos Every Valentine's Day)

<br>
####  ೃ⁀➷ Basic Input/Output System (BIOS) & Unified Extensible Firmware Interface (UEFI)
- System firware
- UEFI is newer, provides support for 64 bit CPU operation, full GUI and mouse operation, networking functionality, and higher security at boot
- BIOS uses arrow keys and ESC; UEFI has GUI
- Boot mode/options/sequence: Fixed disk (HDD/SSD), Optical drive, USB, Network/PXE
- Secure boot: UEFI feature to protect against malware. Computer firmware configured w/ cryptographic keys, preventing modified or unauthorized boot loaders 
- Trusted Platform Module (TPM) is specification for hardware-based storage of hashed passwords, cryptographic keys, digital certificates. Establishes root of trust. Each has unique unchangeable Endorsement Key. Ensures key system state data has not been tampered with when booting.
- Hardware Security Module (HSM): secre USB or thumb drive that stores cryptographic material. Good for computers that don't support TPM 

<br>
####  ೃ⁀➷ Power-On Self-Test (POST) Issues
- system performs POST during boot
- DIagnostic program to check hardware and ensure everything required is present and functioning correctly
- Black screen, computer doesn't boot, no beeps: power is running? Likely POST didn't run or display faulty
- Revert changes, check cabling/connections, check for faulty interfaces/devices, check PSU, check faulty CPU or system firmware
- Check manufacturer website for beep codes
- Troubleshooting boot sector issues: Rule out power and cable issues first. Format boot information if corruption suspected using MBR or GPT ("Boot device not found") 
- Blue Screen of Death (BSOD) typically system memory fault, hardware device/driver fault (new peripherals attached!), corruption of operating system files

IBM PC Beep Codes

| Beep Code         | Meaning                                     |
| --------------------------------------------------------------- |
| 1 short           | Normal POST                                 |
| 1 short           | POST error (error code)                     |
| None              | Power supply, motherboard, or speaker       | 
| Continuous long   | System memory modules or memory controller  |
| Repeating short   |  PSU or motherboard                         | 
| 1 long 1 short    | Motherboard                                 |
| 1 long, 2-3 short | Video adapter                               | 
| 3 long            | Keyboard                                    | 


<br>
####  ೃ⁀➷ Power Issues
- No power symptoms: Check if system case front panel LEDs are lit up, or if fans are running (sound) 
- Isolate cause: Check other equipment in area, try wall socket, check PSU cabling and sdwitches, backup power cable, disconnect extra devices (PSU underpowered)
- Cause not found? Likely faulty PSU or motherboard

<br>
####  ೃ⁀➷ Drive Issues
- HDD unusual noise (low-level noise, clicking, loud or grinding noise) mechaical problems
- Constant LED light activity (disk thrashing) may indicate not enough RAM, so HDD is used for paging (virtual memory)
- Self-Monitoring, Analysis, and Reporting Technology (SMART) self diagnostic program for most fixed disks. Alerts OS if failure detected 

<br>
####  ೃ⁀➷ Performance Issues
- difficult to diagnose (wide variety of causes)
- Check for overheating (CPU may reduce performance level to avoid overheat, called throttling)
- Check misconfigurations (verify compatibility w/ motherboard)
- Verify problem (rule out other issues)
- Inaccurate date/time in system firmware setup program can show Real Time Clock (RTC) battery [a coin cell lithium battery] is failing

<br>
####  ೃ⁀➷ Display Issues
- is monitor plugged in and turned on? Not on standby?
- Select appropriate data source/input channel
- Physical cabling issues
- Burned-out bulb
- Dimmness, resolution, flickering (connections, or backlight)
- Burn-in (OLED vulnerable)
- Color display for digital art, etc (Color calibration/workflow) w/ Color Management applet in Control Panel


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Networks
✧. ┊ ⁭ [LAN](#ೃ⁀-local-area-network) ✧ [WLAN](#ೃ⁀-wireless-lan) ✧ [WAN](#ೃ⁀-wide-area-network) ✧ [MAN](#ೃ⁀-metropolitan-area-network) ✧ [SAN](#ೃ⁀-storage-area-network) ✧ [PAN](#ೃ⁀-personal-area-network) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Types of Networks

##### Local Area Network (LAN)
- computer goup connected by cables and 1+ switches at a single location
- nodes are about 1-2km from another 
- could be single floor, whole building, whole campus
- most based on 802.3 Ethernet standards (IEEE), which desginates xBASE-y (x is nominal da ta rate, y is cable type) 
- 100BASE-T : Fast Ethernet over copper twisted pair cabling, at 100 Mbps
- 1000BASE-T : Gigabit Ethernet over copper twisted pair cabling, at 1 Gbps. Mainstream choice for most LANs
- Copper cabling uses electrical signaling; fiber uses pulses of light

<br>
####  ೃ⁀➷ Wireless LAN (WLAN)
- Radios and antennas for data transmission/reception
- IEEE 802.11 standard (Wi-Fi)

<br>
####  ೃ⁀➷ Wide Area Network (WAN)
- spans multiple geographic locations 
- Internet is example of WAN
- Internet Service Provider (ISP) is company that facilitates access to Internet from local networks 

<br>
####  ೃ⁀➷ Metropolitan Area Networks (MAN)
- Specific network type covering an area equivalent to a city
- Can also mean company w/ multiple connected networks within same metro area 
- Larger than LAN smaller than WAN

<br>
####  ೃ⁀➷ Storage Area Network (SAN) 
- Configurable pool of storage devices for use by application servers 
- Isolated from main networks and accessed only by servers 
- SAN client is server running applications or databases 
- Uses Fiber Channel adapters for connections 

<br>
####  ೃ⁀➷ Personal Area Network (PAN) 
- wireless connectivity to connect devices at a small range (few meters)
- Connect PC and mobile devices or wearables 
- Connect PC to peripherals 

<br>
####  ೃ⁀➷ Power over Ethernet (PoE)
- Supply electrical power from switch port over regular data cabling to powered device (PD)
- Voice over IP (VoIP) handset, camera, wirless access point (WAP)
- IEEE 802.3af : powered devices can draw 13W
- 802.3at (PoE+) : powered devices draw 25W
- 802.3bt (PoE++ or 4PPoE) draw up to 51 W Type 3 or 73 W Type 4 power
- PoE-enabled switch is aka Endspan power sourcing equipment (PSE). Any connected devices, if PoE enabled on device, determines device's power consumption and supplies appropriate voltage level.  


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Hardware
✧. ┊ ⁭ [NIC](#ೃ⁀-network-interface-card) ✧ [Hub](#ೃ⁀-hub) ✧ [Switch](#ೃ⁀-switch) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Network Interface Card (NIC)
- Physical connection to cable for ethernet communications 
- Most motherboards are compatible with 1000BASE-T
- Can also support other types like fiber optic 
- Cards with multiple ports of same type can bond to create higher-speed link
- Each NIC has unique hardware MAC (media access control) address. 
- Every frame of Ethernet data identifies source MAC, destination MAC in the header
- MAC consists of 48 binary digits (6 bytes; 12 hexadecimal digits) w/ colon/hyphen separators or none 

<br>
####  ೃ⁀➷ Hub
- legacy network hardware device
- Meant for 10BASE-T and 100BASE-T Ethernet cabling 
- star topology (each node connected to concentrator/hub)
- computers ignore frames that have wrong MAC address
- reduced performance; one computer can send frame at any time (collision)
- half-duplex (can send and receive but not at same time) 

<br>
####  ೃ⁀➷ Switch
- Basically Ethernet bridge inserted between hubs to reduce collisions
- Provisions one port for each device that needs network connectivity
- Switch can decode each frame & identify source/destination MAC and track which source addresses are with each port 
- Forwards to port matching destination MAC MAC address table 
- Each switch is separate collision domain 
- Full duplex connection (send and receive simultaneously)
- Unmanaged and managed switches (managed switches are for larger LANs: admin can connect over management port, configure security settings, etc) 


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘




<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Network Cables
✧. ┊ ⁭ [UTP](#ೃ⁀-unshielded-twisted-pair) ✧ [STP](#ೃ⁀-shielded-twisted-pair) ✧ [Cat](#ೃ⁀-cat-standards) ✧ [Copper](#ೃ⁀-copper-cabling) ✧ [Network Tap](#ೃ⁀-network-tap) ✧ [Plenum](#ೃ⁀-plenum) ✧ [Fiber Optic](#ೃ⁀-fiber-optic-cable) ✧ [Coaxial](#ೃ⁀-coaxial-cable) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Unshielded Twisted Pair (UTP)
- popular network cable, cooper wire 
- 4 copper conductor wire pairs, twisted at different rate than other pairs to reduce interference 
- Electrical signals are balanced (each wire has equal, yet opposite signal to the its pair) 
- Suffers from attenuation (loses strength over long ranges)
- Max distance 100m

<br>
####  ೃ⁀➷ Shielded Twisted Pair (STP)
- Extra protection against interference 
- 10G Ethernet or higher, datacenter networks; more reliable than UTP
- May be needed if run in proximity with flurescent lighting, power lines, generators etc due to high interference 
- Screened cable: 1 thin outer foil shield around all pairs (Screened Twisted pair ScTP or foiled/unshielded twisted pair F/UTP or foiled twisted pair FTP
- Fully shielded cables have braided outer screen and foil shielded pairs; referred to as shielded/foiled twisted pair S/FTP 

<br>
####  ೃ⁀➷ Cat Standards 
- Specifications for twisted pair cable construction method to use with Ethernet 
- Higher Cat means higher data rates 
- Defined in TIA/EIA-568-C Commercial Building Telecommunications Cabling Standards
- Cat 6A recommended for health care facilities

| Cat | Max Transfer Rate  | Max Distance (m) | Ethernet Standard Support |
| ---------------------------------------------------------- |
| 5  | 100 Mbps | 100       | 100Base-TX / Fast Ethernet     |
| 5e | 1 Gbps   | 100       | 1000BASE-T / Gigabit Ethernet  |
| 6  | 1 Gbps   | 100       | 1000BASE-T / Gigabit Ethernet  | 
|    | 10 Gbps  | 55        | 10GBASE-T / 10G Ethernet       |
| 6A | 10 Gbps  | 100       | 10GBASE-T / 10G Ethernet       | 

<br>
####  ೃ⁀➷ Copper Cabling 
- RJ45 connectors aka 8P8C (eight position/eight contact)
- Each conductor in 4 pair Ethernet copper cable is color coded; pairs are assigned colors (orange, green, blue, brown)
- First conductor in a pair has white insulator with stripes of color and second is solid color 
- T568A: pin 1 wired green/white, pin 2 green, pin 3 orange/white, etc 
- TIA/EIA-568 standard has 2 methods: T568A and T568B
- Straight through Ethernet cable is wired w/ same type of termination at both ends (terminate meaning where the color meets pin)
- TP can also use RJ11 connectors; typically 2 pair cables for telephone systems, broadband digital subscriber line (DSL) modems
- 1 & 3, 2 & 6
- 0.5 inch must be untwisted when terminating 

| T568A              |                          | T568B              |
| ------------------ |                          | ------------------ |
| Pin | Color        |                          | Pin | Color        |
| ------------------ |                          | ------------------ |
| 1   | Green/white  |                          | 1   | Orange/white |
| 2   | Green        |                          | 2   | Orange       |
| 3   | Orange/white |                          | 3   | Green/white  |
| 4   | Blue         |                          | 4   | Blue         |
| 5   | Blue/white   |                          | 5   | Blue/white   |
| 6   | Orange       |                          | 6   | Green        |
| 7   | Brown/white  |                          | 7   | Brown/white  |
| 8   | Brown        |                          | 8   | Brown        |


<br>
####  ೃ⁀➷ Network Tap
- Used to intercept signals passing through cable 
- Sends to packet or protocol analyzer 

<br>
####  ೃ⁀➷ Plenum 
- Empty space in building to carry heating, ventilation, AC sstems (false ceilings, raised floors) 
- Can also be used for communications wiring 
- Plenum cable must be self extinguishing and meet strict safety fire standards as plenum space can easily welcome fires
- CMP/MMP rated 

<br>
####  ೃ⁀➷ Fiber Optic Cable
- Light pulses through lasers and LEDs
- Not susceptible to interference / suffer less from attenuation
- Supports higher bandwidth links, longer cable runs 
- 2 categories: Single mode, multimode
- Single-mode Fiber (SMF): Small core and carries long wavelength infrared signal, supports data rates up to 10 Gbps 
- Multi-mode Fiber (MMF): Larger core, shorter wavelength infrared light, less expensive and coherent LEDs. Less expensive. Does not support high signaling speeds or long distances. Suitable for LANs
- Easily damaged. Do not repeatedly plug in and out 

Connector form factors: 
- Straight Tip (ST): bayonet style connector with push-and-twist locking mechanism; older multi mode networks
- Subscriber Connector (SC): push/pull design with simple insertion/removal than fiber channel (FC) connector. Simplex and duplex versions. Single or multi mode.
- Lucent Connector (LC): small form factor, tabbed push/pull design. Similar to SC but smaller. Higher port density 

<br>
####  ೃ⁀➷ Coaxial Cable
- Aka coax cable
- Copper cabling that carries electrical signals
- Uses 2 conductors that share same axis to cancel out interference (instead of twisted pairs)
- Core signal conductor enclosed by plastic insulation and second wire mesh conductor for shielding and as a ground
- Mostly used for CCTVs and as patch cable for Cable Access TV (CATV) and broadband cable modems 

└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘



<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Wireless Networking

<br>
####  ೃ⁀➷ IEEE 802.11 & Access Points

##### 802.11
- Aka Wi=Fi (most wireless LANs/ WLANs based on this standard)
- Transmission and reception antennas tuned to specific frequency
- Infrastructure mode: Each client device connects to network via access point (AP) - in 802.11, referred to as infrastructure Basic Service Set (BSS) and MAC address of AP's radio is Basic Service Set Identifier (BSSID)

##### Access Points
- AP establishes wireless-only network, or works as a bridge to forward communicatiosn between wireless and wired network. Wired network would be distribution system (DS) 
- AP joined to network like a host is through a wall port and Ethernet switch 

##### Frequency Bands
- Wi-Fi devices operate on specific radio frequency within overall frequency band 
- Frequency band split into smaller ranges called channels 
- 2 main standards used by 802.11 standards: 
- 2.4 GHz standard: Longest signal range, does not support high number of individual channels, often congested, increased risk of interference, Wi-Fi 45 m 
- 5 GHz standard: Less effective at penetrating solid surfaces, does not support maximum ranges like 2.4 does, supports more individual channels, less congestion and interference, higher data rates at shorter ranges, Wi-Fi 30 m

##### 802.11 Standards 
- 802.11a standard uses 5GHz frequency band only, supports 54 Mbps
- 802.11b standard uses 2.4GHz frequency band, supports data rate of 11 Mbps
- 802.11g standard is upgrade for 802.11b; same encoding mechanism and 54 Mbps as 802.11a but using 2.4GHz from 802.11b w/ same channel layout. Backwards support for legacy 802.11b clients
- 802.11n standard has improvements to increase bandwidth, works over both 2.4 and 5 GHz. Allows 2 adjacent channels to be combined, called channel bonding. Increases reliability and bandwidth by multiplexing signal streams from 2-3 antennas (multiple input multiple output MIMO) 
- 802.11n is now called Wi-Fi 4
- 802.11ac (Wi-Fi 5) works with 5 GHz. Can have dual band access point 
- 802.11ax (Wi-Fi 6) improves per-stream data rate, works in both 2.4 and 5 GHz bands


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘






