---
layout: default
title: Field Technicians Troubleshooting
description: Thus, they were granted the treasure map...
---

## Use Case

The company (let's call it _DoxHut_) was performing **PoCs** and running tests directly on what we can call a production environment. The software solution was implemented on a piece of software already established within the customer's facilities. Although it was _code_ injected in an application, it required various pieces of hardware installation and frequent maintenance. <br>
The challenge, however, was the team available to cover eventual incidents. Since we were **dealing with hardware**, on-site analysis was often inevitable. The team was mainly constituted of two levels: <br>
- **SREs**, in charge of controlling the servers' stability and, among other things, running a second level of analysis, usually requested by the Field Technicians, once they run the first instance of analysis and got confirmation on the issue not being related to the hardware installation's status. <br>
- **Field Technicians**, mostly constituted by interns, most of them part-time, and distributed across the country so that in-situ assistance was feasible. <br
As soon as I learned what they did and how they did it, I noticed most of the incidents were time-sensitive, and the two instances of analysis had to occur swiftly and efficiently. To contribute to this cause, I interviewed **SMEs** from both sides, gathered all information on common issues and the steps to achieve their resolution, created a rough draft, validated it with them, and published the following **Help Docs page** for **troubleshooting** the issues they faced on a daily basis.


## Field Technicians Troubleshooting

![image](images-projectdesk-intro.png)

### Goal

This document aims to provide **Field Technicians** with a comprehensive overview of common issues and practical guidelines on how to effectively address them. It covers a wide range of scenarios, including remote troubleshooting and on-site analysis, offering actionable steps for resolution.

> 💡 Contact **SRE's Team Leader** for further questions via Slack.<br>
> 📡 Is there anything missing? Reach out to our **Tech Writer** via Slack.

### On this Page

- [In-Store Monitoring Service](#in-store-monitoring-service)
  - [Connection Issue](#connection-issue)
  - [VPN is Down](#vpn-is-down)
- [NAS](#nas)
  - [NAS is Full](#nas-is-full)
  - [NAS Disconnected](#nas-disconnected)
  - [NAS Disk Broken](#nas-disk-broken)
- [Router](#router)
  - [Router is Broken](#router-is-broken)
  - [K3s Stopped](#k3s-stopped)
  - [LTE/Dongle Issue](#ltedongle-issue)
- [Server](#server)
  - [Internal Disc Full](#internal-disc-full)
  - [Excessive CPU Use Alert](#excessive-cpu-use-alert)
  - [High-Temperature Alarm](#high-temperature-alarm)
  - ["The Box is Disconnected" Message](#the-box-is-disconnected-message)
  - [Server not Recording](#server-not-recording)
  - [NAS is not Mounted](#nas-is-not-mounted)
  - [Wrong Time Settings](#wrong-time-settings)
  - [Excessive RAM Use](#excessive-ram-use)
- [Smart Power Supply](#smart-power-supply)
  - [Power Switch Unreachable (Not Shown/ No Message)](#power-switch-unreachable-not-shown-no-message)
  - [Outlets are Blocked (No Message)](#outlets-are-blocked-no-message)
- [Switch](#switch)
  - [Switch is Off](#switch-is-off)
  - [Server Issue / Server is Off](#server-issue--server-is-off)


## In-Store Monitoring Service
### Connection Issue

![image](images-fieldtechnicians-in-store1.png)

### VPN is Down

![image](images-fieldtechnicians-in-store2.png)

## NAS
### NAS is Full

![image](images-fieldtechnicians-nas1.png)

### NAS Disconnected

![image](images-fieldtechnicians-nas2.png)

### NAS Disk Broken

![image](images-fieldtechnicians-nas3.png)

## Router
### Router is Broken

![image](images-fieldtechnicians-router1.png)

### K3s Stopped 

![image](images-fieldtechnicians-router2.png)

### LTE/Dongle Issue

![image](images-fieldtechnicians-router3.png)

## Server
### Internal Disc Full

![image](images-fieldtechnicians-server1.png)

### Excessive CPU Use Alert

![image](images-fieldtechnicians-server2.png)

### High-Temperature Alarm

![image](images-fieldtechnicians-server3.png)

### "The Box is Disconnected" Message

![image](images-fieldtechnicians-server4.png)

### Server not Recording

![image](images-fieldtechnicians-server5.png)

### NAS is not Mounted

![image](images-fieldtechnicians-server6.png)

### Wrong Time Settings

![image](images-fieldtechnicians-server7.png)

### Excessive RAM Use

![image](images-fieldtechnicians-server8.png)

## Smart Power Supply
### Power Switch Unreachable (Not Shown/ No Message)

![image](images-fieldtechnicians-powersupply1.png)

### Outlets are Blocked (No Message)

![image](images-fieldtechnicians-powersupply2.png)

## Switch
### Switch is Off

![image](images-fieldtechnicians-switch1.png)

### Server Issue / Server is Off

![image](images-fieldtechnicians-switch2.png)


[Back](./)
