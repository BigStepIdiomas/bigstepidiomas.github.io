---
layout: default
title: SRE FAQ
description: The great and powerful Oracle, we meet at last--- said Agent Smith
---

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

<span class="tag" style="background-color: #ffc107;">FAQ</span>
<span class="tag" style="background-color: #6f42c1;">Knowledge Base</span>
<span class="tag" style="background-color: #6c757d;">Help Docs</span>
<span class="tag" style="background-color: #17a2b8;">Troubleshooting</span>
<span class="tag" style="background-color: #90ee90;">Support Docs</span>
<span class="tag" style="background-color: #8470ff;">SRE Guides</span>
<span class="tag" style="background-color: #20c997;">English</span>

## Use Case

The company (let's call it _DoxHut_) was performing **PoCs** and running tests directly on what we can call a production environment. The software solution was implemented on a piece of software running on devices already established within the customer's facilities. Although it was _code_ injected in an application, it required various pieces of hardware installation and frequent maintenance. <br>
The challenge, however, was the team available to cover eventual incidents. Since we were **dealing with hardware**, on-site analysis was often inevitable. The team was mainly constituted of two levels: <br>
- **SREs**, in charge of controlling the servers' stability and, among other things, running a second level of analysis, usually requested by the Field Technicians, once they run the first instance of analysis and got confirmation on the issue not being related to the hardware installation's status. <br>
- **Field Technicians**, mostly constituted by interns, most of them part-time, and distributed across the country so that in-situ assistance was feasible. <br>

As soon as I learned what they did and how they did it, I noticed most of the incidents were time-sensitive, and the two instances of analysis had to occur swiftly and efficiently. To contribute to this cause, I interviewed **SMEs** from both sides, gathered all information on common issues and the steps to achieve their resolution, created a rough draft, validated it with them, and published the following **Help Docs page** for **troubleshooting** the issues they faced on a daily basis.


## SRE FAQ

### Goal

This section is explicitly meant for cleanly organized solutions to common DevOps SREs requests like creating a user on a machine, setting up a new user, etc...
The goal is to both save the SRE's time as well as unblock coders faster.

> 💡 If any solution is outdated, please reach out/start a thread on our Slack channel (#sre-faqs) and ping our technical writer @Jonathan Pinetta requesting an update.
<br>

### On this Page

- [How To](##how-to)
- [Useful Documentation](##useful-external-documentation)
- [Useful Tools](##useful-tools)


## How To
### Set up a new user on a machine:
- To set up a new user with sudo and Docker access, follow the commands below. Replace <user> with your desired username.

```bash
sudo adduser <user>              # Create the new user
sudo usermod -aG sudo <user>     # Add the user to the 'sudo' group for administrative privileges
sudo gpasswd -a <user> docker    # Add the user to the 'docker' group for Docker access
```

- This one-liner achieves the same result:

```bash
sudo adduser <user> && sudo usermod -aG docker <user>
```
<br>
> Please note that the one-liner doesn't give explicit sudo permissions to the user. The user will have to enter their password when using sudo for administrative tasks. If you wish to give the user passwordless sudo access, you should modify the sudoers file accordingly. Keep in mind that granting passwordless sudo access should be done with caution and only for trusted users.
<br>


### Generate an SSH key:
- To generate an <SSH> key for secure communication, you can use the `ssh-keygen` command. It is recommended to use the `Ed25519` key type for improved security.

```bash
ssh-keygen -t ed25519 -C "<name>@doxhut.xyz"
```

- Replace <name> with your desired identifier, email, or any other information you wish to associate with the key. This command will create an `Ed25519` SSH key pair, consisting of a private key (id_ed25519) and a public key (id_ed25519.pub). The public key can be shared with remote servers or services you want to authenticate with. Ensure you keep the private key secure and do not share it with others.


### TLDR command to delete a user:

**Userdel** is a command used to remove a user account or remove a user from a group in Linux systems. Note that all commands must be executed as root.

More information about <userdel> can be found in the [manual page](https://manned.org/userdel).

To remove a user:
- Remove a user:

```bash
userdel [name]
```

- Remove a user along with their home directory and mail spool:

```bash
userdel --remove [name]
```

- Remove a user from a group:

```bash
userdel [name] [group]
```

- Remove a user in another root directory:

```bash
userdel --root [path/to/other/root] [name]
```

> 💡 Remember to replace [name], [group], and [path/to/other/root] with the actual username, group name, and path to the other root directory, respectively. Always exercise caution when using this command as it can result in the irreversible deletion of user data.
<br>

### CVD upload script:
A very big change in the CVD upload script: code has been refactored to support camera coordinates for specific cam ids an example config in the upload script looks as below:

```html
cam-config:
  fps: 25
  base-dimension:
  - 1280
  - 720
   origins:
    7:
    - 0
    - 0
    9:
    - 1280
    - 0
```

### Reinstall k3s, set up Rabbit, and GPU splitting on it:
- Use the following script to reinstall k3s and set up Rabbit and GPU splitting on it. It should be available in all the inference boxes as the command **k3scli.sh**.

- With k3scli.sh -h you can see the different options to run it:

```bash
root@dev-office-inference-0:/home/agot# k3scli.sh -h
    Usage: k3scli.sh args ...

    Description:
    Options:
        -k Uninstall and install k3s
        -r Install rabbit
        -g Setup GPU sharing
        -a Install AWS CLI
```

- To reinstall everything, just run **k3scli.sh -k -g -r** . Such action will reinstall k3s, install GPU splitting and deploy rabbit on it.

### Kill a running process
Old processes running in the background may cause slowdowns. In order to terminate them, you will need to find them first. 

Use the following commands to help you straightforwardly identify the ones that are causing you trouble and then proceed to responsibly kill them.
<br>

**PS** gets Information about running processes.

To list information on running processes:
- List all running processes:     

```bash
ps aux
```

- List all running processes including the full command string:   

```bash
ps auxww
```

- Search for a process that matches a string:

```bash
ps aux | grep string
```

- List all processes of the current user in extra full format:   

```bash
ps --user $(id -u) -F
```

- List all processes of the current user as a tree:

```bash
ps --user $(id -u) f
```

- Get the parent PID of a process:     

```bash
ps -o ppid= -p pid
```

- Sort processes by memory consumption:     

```bash
ps --sort size
```

> 🧷 More information [here](https://manned.org/ps).

<br>
  
**kill** sends a signal to a process, usually related to stopping the process. <br>
Then, once you found the process you want to kill, use the command that suits best your scenario:
<br>

> 💡 All signals except for SIGKILL and SIGSTOP can be intercepted by the process to perform a clean exit. 
<br>

- Terminate a program using the default SIGTERM (terminate) signal:

```bash
kill process_id
```
- List available signal names (to be used without the SIG prefix):

```bash
kill -l
```

- Terminate a background job:

```bash
kill %job_id
```

- Terminate a program using SIGHUP (hang up) signal. Many daemons will reload instead of terminating:

```bash
kill -1|HUP process_id
```

- Terminate a program using the SIGINT (interrupt) signal. This is typically initiated by the user pressing CTRL + C:

```bash
kill -2|INT process_id
```

- Signal the operating system to immediately terminate a program (which gets no chance to capture the signal):

```bash
kill -9|KILL process_id
```

- Signal the operating system to pause a program until a SIGCONT (“continue”) signal is received:

```bash
kill -17|STOP process_id
```

- Send a SIGUSR1 signal to all processes with the given GID (group ID): 

```bash
kill -SIGUSR1 -group_id
```

> 🧷 More information [here](kill - manned.org). 

<br>

> ⚠️ All these commands are very sensitive and can lead to a lot of issue. So, please, be aware that killing a process might affect someone else’s works.

<br>


### How to create S3 buckets
Follow the guidelines included in this [repo](https://git.agot.ai/users/sign_in).

### How to install
#### Adding User for Automations

This command creates a new user with the username "awx" and sets the user's shell to /bin/bash. The user will be added to the "sudo" group, granting administrative privileges.

- Create a new user for automations.

```bash
useradd -c "User for automations" -G "sudo" -s /bin/bash -m awx
```

- Set up SSH for the new user.

```bash
mkdir -p /home/awx/.ssh && chmod 0700 /home/awx/.ssh && touch /home/awx/.ssh/authorized_keys && chown -R awx. /home/awx/.ssh && chmod 0600 /home/awx/.ssh/authorized_keys
```

- Edit the sudoers file.

```bash
sudo visudo
```

- Add the following configurations to the sudoers file.

```bash
Defaults    env_reset
Defaults    mail_badpass
Defaults    secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"
root    ALL=(ALL:ALL) ALL
%admin  ALL=(ALL) ALL
%sudo   ALL=(ALL:ALL) NOPASSWD: ALL
See sudoers(5) for more information on "#include" directives:
includedir /etc/sudoers.d
```

- Add the SSH public key to the authorized_keys file for the new user.

```bash
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIMOmhXTjtS4Tehalzfyn6KwPU0CwYpCSRuv2+P/bZrrc user for automation
```

- You can copy and paste each step into your Markdown file or text editor. The code snippets are formatted as code blocks for better visibility and clarity.

## Useful External Documentation
### kubclt Reference Docs
Access [kubectl official documentation](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands).<br>
All the verbs in the left pane are very close to all the actions we want to run inside a Kubernetes cluster so if you are wondering how to do something inside Kubernetes, you may find the correct command by searching for the closest verb related to that action.


## Useful Tools
### TLDR
A mighty app named TLDR, like TLDR RM, and a list o most used rm commands and its explanation will be there:
[GitHub - tldr-pages/tldr: 📚 Collaborative cheatsheets for console commands](https://github.com/tldr-pages/tldr)

[Back](./)
