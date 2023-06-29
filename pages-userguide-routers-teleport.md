---
layout: default
title: Guides - Sample 01
description: Interns and newcommers wondered if it was already Christmas
---

# Changing Routers Passwords on Teleport

<style>
.tag {
  display: inline-block;
  padding: 4px 8px;
  border-radius: 4px;
  color: #fff;
  font-size: 14px;
  font-weight: bold;
  margin-right: 8px;
  margin-bottom: 10px;
}

/* Add the background colors for each category */
.tag:nth-child(1) { background-color: #007bff; } /* UX Writing */
.tag:nth-child(2) { background-color: #28a745; } /* Technical Specification */
.tag:nth-child(3) { background-color: #dc3545; } /* API Docs */
.tag:nth-child(4) { background-color: #ffc107; } /* Technical Documentation */
.tag:nth-child(5) { background-color: #6f42c1; } /* Knowledge Base */
.tag:nth-child(6) { background-color: #fd7e14; } /* Translation */
.tag:nth-child(7) { background-color: #20c997; } /* English */
.tag:nth-child(8) { background-color: #e83e8c; } /* Installation Guides */
.tag:nth-child(9) { background-color: #6c757d; } /* Help Docs */
.tag:nth-child(10) { background-color: #17a2b8; } /* Troubleshooting */
.tag:nth-child(11) { background-color: #87ceeb; } /* Handbooks */
.tag:nth-child(12) { background-color: #90ee90; } /* Support Docs */
.tag:nth-child(13) { background-color: #ff6666; } /* Project Docs */
.tag:nth-child(14) { background-color: #ffff99; } /* Portuguese */
.tag:nth-child(15) { background-color: #d291bc; } /* Release Notes */
.tag:nth-child(16) { background-color: #ffb347; } /* German */
.tag:nth-child(17) { background-color: #98d8d8; } /* SDK */
.tag:nth-child(18) { background-color: #ffb6c1; } /* Product Discovery */
.tag:nth-child(19) { background-color: #d3d3d3; } /* UX Design */
.tag:nth-child(20) { background-color: #afeeee; } /* Spanish */
.tag:nth-child(21) { background-color: #cd853f; } /* Copywriting */
.tag:nth-child(22) { background-color: #ffa07a; } /* Microcopy */
.tag:nth-child(23) { background-color: #f08080; } /* Educational Material */
.tag:nth-child(24) { background-color: #da70d6; } /* Localization */
.tag:nth-child(25) { background-color: #8470ff; } /* User Guides */
</style>

<span class="tag" style="background-color: #ffc107;">Technical Documentation</span>
<span class="tag" style="background-color: #6f42c1;">Knowledge Base</span>
<span class="tag" style="background-color: #6c757d;">Help Docs</span>
<span class="tag" style="background-color: #17a2b8;">Troubleshooting</span>
<span class="tag" style="background-color: #87ceeb;">Handbooks</span>
<span class="tag" style="background-color: #90ee90;">Support Docs</span>
<span class="tag" style="background-color: #8470ff;">User Guides</span>
<span class="tag" style="background-color: #20c997;">English</span>


![intro](images-changingpasswords-intro.png)

## On this Page:

- [Actions Required](#actions-required)
- [Prerequisites](#prerequisites)
- [Creating Passwords for Stores' Routers on LastPass](#creating-passwords-for-stores-routers-on-lastpass)
- [Accessing a Server](#accessing-a-server)
- [Setting SREs SSH RSA Keys](#setting-sres-ssh-rsa-keys)
- [Bonus: Setting Server’s Time](#bonus-setting-servers-time)

## Actions Required

- Create passwords and sections for servers on **LastPass**
- Access servers and change routers passwords
- Add **SREs' SSH RSA keys** to the routers authorized keys
- Set server time

## Prerequisites

- Having a **LastPass user**
- Having a **Teleport User**
- Having **Teleport installed**
- Having necessary **SSH RSA Keys**
- Knowing which servers to make changes to.

## Creating Passwords for Stores' Routers on LastPass

To create a section for each store’s router password on **LastPass**:

1. Access **DoxHut's LastPass Password Manager** panel.<br>

2. Create a **New Item** by clicking the plus icon located at the bottom right corner. This action will open a modal where you must fill in a few fields. <br>

    ![createnew](images-changingpasswords-createnew.png)<br>

3. Fill in the **Name** field with the server’s name.<br>

4. Fill in the **Folder** field with the “**Shared-stores**” value.<br>

5. Fill in the **Username** with “**root**.”<br>

6. Create a strong password (use the **LastPass' Generate Secure Password** tool).<br>

7. Copy the password and paste it into the **Site Password** field.<br>

8. Save this configuration by clicking **Save**.<br>

9. Repeat the whole process for each of the servers listed below.<br>

    ![createnew2](images-changingpasswords-createnew2.png)

## Accessing a Server

To access a server:

1. List the existing servers by running: <br>
`tsh ls` <br>

   You will see all servers listed as shown next 
   
   ![servers](images-changingpasswords-serverslist.png)

2. Select a server and access it:<br>
`tsh ssh doxhut@doxhut-2-xavier-0` (example)

3. Then, access the router:<br>
`ssh root@192.168.1.1`

4. Once in the router, change its password by running:<br>
`passwd`

5. You will get a confirmation message and that’s it!<br>

## Setting SREs SSH RSA Keys

To set an **SREs SSH RSA key** in the router:<br>

1. Run:<br>
`cd /root`

2. List all directories:<br>
`ls -hal`

3. Open .ssh<br>
`cd .ssh`

4. Then, edit the authorized keys<br>
`vim authorized_keys`

5. Once on the **Vim editor**, press **“i”** to activate the editor mode.<br>

6. Paste one of the **SSH RSA keys**.<br>

7. Press **“Esc”** to exit edit mode.<br>

8. Press **“o”** to jump into the next line.<br>

9. Press **“i”** to activate the editor mode and paste a second key.<br>

10. Repeat the process for key you must insert in the file.<br>

11. Finally, make sure you are not in the editor mode, and press **“:wq”** to save changes and quit. <br>

## Bonus: Setting Server’s Time

Since you are already on the server, use the chance to set the server’s time by running:

`uci set system.ntp.enable_server='1' ; uci commit system ; /etc/init.d/sysntpd restart`<br>

> 💡 **Note**: You will not get any confirmation message for this last step.

<br><br>
[Back](./)