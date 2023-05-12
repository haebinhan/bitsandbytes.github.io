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
✧. ┊ ⁭ [PSU](#ೃ⁀-power-supply-units) ✧ [PSU Adapters](#ೃ⁀-power-supply-adapters) ✧ [Fan/Cooling](#ೃ⁀-fan/cooling-systems) ✧ [Storage](#ೃ⁀-storage-devices) ✧ [Fan/Cooling](#ೃ⁀-fan/cooling-systems) ⁭ ⁭┊ .✧

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
####  ೃ⁀➷ Storage Devices
- 



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘



<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
###
✧. ┊ ⁭ [Video](#ೃ⁀-video-interfaces/cables) ✧ [Legacy Cables](#ೃ⁀-legacy-cables) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ 


└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘
