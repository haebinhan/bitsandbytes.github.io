---
title: "A+ 1102: Configuring, Managing, & Supporting Windows"
layout: post
date: 2022-04-16
feature_image: images/open_source.jpg
tags: [comptia, a+]
---

Intro

<!--more-->

Some OSINT strategies:
- [**Google Dorking**](#basic-windows)
- [**Windows Command Prompt Commands**](#windows-command-prompt-commands) - *looking at data about the data*
- [**Windows Shortcuts**](#windodws-shortcuts) - *searching an image against online databases*


### Basic Windows
<span style="color:blue">J*OS*</span> - An operating system is the interface between the computer hardware, software applications, and user. 

Windows Settings, or the Settings app, is an interface to change configuration settings (all configuration data is held in the registry). 
Privacy settings include the usage data that Windows can collect and/or share. Permissions can also be enabled and disabled here, such as microphone, location, or camera access for different applications. 
In power management, power-saving modes can be activated. Standby suspends to RAM - power is cut to most devices but the memory keeps power. Hibernate suspends to disk - any open, unsaved file will be saved in memory to the disk, and the computer is turned off. These are the same as sleep, hybrid sleep, and modern standby. Sleep would be when the device goes into standby and switches to hibernate if running on pure battery power. Hybrid sleep would be where the device creates the hibernation file, then goes into standby. Modern standby is slightly different, and is basically a low-power idle mode and keeps network connectivity. 

User Account Control (UAC) is meant to prevent unauthorized use of administrator privileges from taking place. It requires the user to confirm a prompt or enter credentials manually. You may have seen this when downloading software.

File Explorer is Window's file management system. It includes system objects such as the User account (personal data folders for signed-in profile), OneDrive, This PC (personal folders, fixed disks, removable storage drives), Network (computers, shared folders and printers), and Recycle Bin. The system objects can be seen in the left hand pane of File Explorer. The system files are the ones required by the operating system in order to function properly. The root directory has a Windows folder which contains the system root, drivers, logs, and configuration files. The Users folder has NTUSER.DAT, which is registry data for each user and their settings and data. 

The Control Panel is a legacy interface that is still used today. It contains all regular settings from Windows Settings and some more configuration settings. One of the applets in Control Panel is called Administrative Tools, which links to more shortcuts that are more advanced. 

A Microsoft Management Console (MMC) is a container that has snap-ins to modify settings. Some common consoles for admins are Computer Management (compmgmt.msc), Defragment and Optimize Drives (dfrgui.exe), Disk Cleanup (cleanmgr.exe), Event Viewer (eventvwer.msc), Local Security Policy (secpol.msc), Resource Monitor (resmon.exe), Performance Monitoring (perfmon.msc), Registry Editor (regedit.exe), Services Console (services.msc), and Task Scheduler (taskschd.msc). A custom MMC can be made, where the admin can create a personal selection of snap-ins and save it as an .msc file. This can make changing settings faster and easier.

### Windows Command Prompt Commands
dir - list files and subdirectories. Use /o:n to order by name, /o:s to order by size, e for extension, d for date. 
cd .. - change directory to parent directory
xcopy Source Destination - copy contents of more than one directory, and maintain directory structure
robocopy - a robust copy. 
md newDirectory - makes a new directory
rd oldDirectory / rmdir oldDirectory - deletes an empty directory. Add /s switch to delete a directory and its contents. 
diskpart - command line version of Disk Management tool
shutdown /s - close all programs/services and power off computer. Use /t switch to specify a time delay in seconds. Use the /a switch to abort a shutdown.
shutdown /h - save current session to disk and poweroff. Hibernate.
shutdown /l - close all programs and log off. Use /r switch to reboot. 
sfc /scannow - run an immediate scan from the System File Checker utility
winver - tells Windows version information

### Windows Shortcuts
WIN/START + SPACE ---> Toggle active keyboard language
START + R ---> Run dialog
type cmd in Instant Search, then CTRL + SHIFT + ENTER ---> Run as administrator in command prompt

