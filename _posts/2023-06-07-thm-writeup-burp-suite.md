---
title: "TryHackMe Writeup: Burp Suite"
layout: post
date: 2023-06-07
feature_image: images/thmwriteup_burpsuite.png
tags: [thm, burpsuite, webapplications]
---

! This post will be completed and launched on June 9th, 2023. Until then it remains as a draft, due to the nature of github pages.

*Writeup summarizing my learning experience with THM's Burp Suite module alongside further research done to solidify my understanding of the topic.*

<!--more-->

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

## Table of Contents

1. [Burp Suite](#burp-suite)

<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>

┌──❀*̥˚───────────────────────────────────────────────❀*̥˚─┐
### Burp Suite
✧. ┊ ⁭ [tbd](#ೃ⁀-tbd) ✧ [tbd](#ೃ⁀-tbd) ✧ [tbd](#ೃ⁀-tbd) ⁭ ⁭┊ .✧

<br>
####  ೃ⁀➷ What is Burp Suite?
Burp Suite is a web application framework from PortSwigger, based off of Java. It's software that can be used for pentesting the security of web applications and is a common, go-to tool. The most common use is to capture and manipulate traffic that is sent between a webserver and attacker, allowing you to intercept and modify web requests before they're fully sent to their original destination server. The Burp Suite Community edition is free for any non-commercial use, while Burp Suite Professional has more features for a price. The Enterprise edition works on servers and constantly will scan targets for vulnerabilities instead of being manually run. 

Basic tools include the proxy, repeater, intruder, decoder, comparer, and sequencer. The **Burp Proxy** lets you intercept and modify web application requests and responses, while the **Repeater** lets you capture, modify, and resend requests repeatedly. The **Intruder** lets you spray endpoints with requests for brute force attacks and more, while the **Decoder** helps you decode or encode information. The **Comparer** is a comparison tool for data, and the **Sequencer** is used to assess how random tokens or randomly generated data is. 

Burp Suite can be downloaded straight from its [website](https://portswigger.net/burp/releases/professional-community-2023-5-3?requestededition=community&requestedplatform=). 



└───❀*̥˚───────────────────────────────────────────────❀*̥˚┘


<br>
<div align="center">.・。.・゜✭・.・✫・゜・。. </div>
<br>



#### Sources & References
