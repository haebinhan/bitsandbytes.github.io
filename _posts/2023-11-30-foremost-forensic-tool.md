---
title: "Foremost Forensic Tool"
layout: post
date: 2023-11-30
feature_image: images/
tags: [basics, forensics]
---

This is my writeup from a lab to image and create a hash of a disk, verify the integrity of the disk, and use Foremost to recover deleted files. 

*Foremost* is a file carving utility console program used to recover files (called data carving) through headers, footers, and internal data structures. It is currently open to the public at http://foremost.sourceforge.net/

*md5sum* is a Linux command that verifies a Message Digest 5 hash (128-bit).

*sha1sum* is a Linux command that verifies a Secure Hash Algorithm hash (160-bit).


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
### Hashing
✧. ┊ ⁭ [Hashing](#ೃ⁀-routing-concepts) ✧ [Dynamic Protocols](#ೃ⁀-dynamic-routing-protocols) ✧ [Troubleshooting](#ೃ⁀-installation--troubleshooting) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ Hashing

*Hashing* is transforming plaintext into hashed text through a hashing algorithm, which can then be used to ensure integrity (data was not modified). 

MD5 is a very insecure hashing algorithm. MD5 creates 128-bit outputs, but there can be collisions (where two + inputs result in the same hash). 



