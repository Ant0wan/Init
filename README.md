# Init [![42](https://i.imgur.com/9NXfcit.jpg)](i.imgur.com/9NXfcit.jpg)

## System and Network Administration

This repository contains the scripts and answers to the <a href="https://cdn.intra.42.fr/pdf/pdf/886/fillit.en.pdf" target="_blank">init [a 42 project]</a>. Init is an introduction to system and network administration allowing 42's students to discover system and network basic commandsas well as many of the services used on server machines.

This repository is made of 3 parts: network, scripts, system.


## Network

The part “Network” has been done on school’s Macs running with Darwin Kernel Version 16.7.0.

- 01 gets the list of the network interfaces
- 02 identifies and display the Ethernet interface characteristics, broadcast address and subnetwork IPs
- 03 identifies the MAC address of the Wi-Fi card 
- 04 identifies the default gateway in the routing table
- 05 identifies the IP address of the DNS responding to an url
- 06 complete path of the file that contains the IP address of the DNS server used by OS
- 07 makes a query on an external DNS server 
- 08 provider of a given .org
- 09 finds the external IP of a given www(dot)
- 10 identifies the network devices between the network interface and a given domain
- 11 name and IP address of the modem
- 12 finds the IP that was assigned to the system by the dhcp server
- 13 name of the host usgin reverse DNS
- 14 path of file containing the local DNS entries
- 15 adds a reroute to /etc/hosts

## Scripts

This part can either be ran on a the Debian virtual machine or Macs (for vitual machine, please refers to Virtual Machine below section).

It contains:

- a script which displays only the login, UID and Path of each entry of the /etc/passwd file, 
- a script which delete an ACTIVE user on the VM (make sure you logged in ssh before), 
- and a password generator

Password generator output sample

```SHELL=
> ./03 -S 18
0t)@IEnlhQmH_0o#V'

> ./03 -b 10
1100001011

> ./03 -o 28 A-Bw-z0-4-+/
Ay1-y4w+-10343wB+/224y+2-yzA

```

Password generator usage demo

[![passwordgenerator](https://i.imgur.com/IdsM678.gif)](i.imgur.com/IdsM678.gif)


## System

This part has been ran on a the Debian virtual machine (please refers to Virtual Machine below section).

- 01 finds path of the file containing the installed OS (Debian)
- 02 temporarily renames the system 
- 03 permanently renames the system
- 04 uptime
- 05 determines the state of the SSH service
- 06 restarts the SSH service
- 07 finds the PID of the SSHD service
- 08 RSA keys of systems that are authorized to connect via SSH
- 09 "who" is connected to the system
- 10 lists the partition tables of drives
- 11 displays the available space left and used on the system in an humanly understandable way
- 12 displays exact size of each folder of /var in a humanly understandable way followed by the path of it  
- 13 displays, in real time, currently running processes 
- 14 runs the ‘tail -f /var/log/syslog‘ command in background
- 15 kills the backgrounded above-mentionned process
- 16 services that runs specific tasks following a regular schedul
- 17 connects VM using SSH
- 18 kills ssh service
- 19 lists all services which are started at boot time
- 20 lists all existing users
- 21 lists all real users
- 22 adds a new local user
- 23 steps to follow for connecting freshly added user
- 24 lists all installed packages

---

## Virtual Machine [![VB](https://i.imgur.com/ZtM4EYJ.png)](i.imgur.com/ZtM4EYJ.png)

The following config has been used: <a href="https://www.virtualbox.org/wiki/Downloads" target="_blank">VirtualBox 6.0.2</a> + <a href="http://ftp.nl.debian.org/debian/dists/stretch/main/installer-amd64/current/images/netboot/" target="_blank">Debian netboot mini.iso</a> 2018-11-10.

### Virtual machine config:

- Name: debian_ontmp
- Type: Linux
- Version: Debian (64-bits)
- RAM: 2048MB
- Disks: VirtualBox Disk Image, dynamically allocated, 8GB, path: /tmp/[login]/

[![VirtualBoxMachine](https://i.imgur.com/TbLbIvc.png)](i.imgur.com/TbLbIvc.png)

### Settings:

- Processors: 4CPUs
- Display: Video Memory: 128MB, Enable 3D Acceleration
- Network:
- Adapter 1: NAT
- Adapter 2: Bridged Adapter en0: Ethernet

This enables SSH connection required by the "system" part.

### Installing Virtual Machine

- Boot has been made on mini.iso.
- Configure the network

[![Process1](https://i.imgur.com/ylJVIEF.png)](i.imgur.com/ylJVIEF.png)

- Set username

[![Process2](https://i.imgur.com/zajQ4n4.png)](i.imgur.com/zajQ4n4.png)

- Set root passwords: root
- Set users password: root

[![Process3](https://i.imgur.com/fYCCeNJ.png)](i.imgur.com/fYCCeNJ.png)

- Choose a mirror for doznloading Debian archive

[![Process4](https://i.imgur.com/g6IZAuI.png)](i.imgur.com/g6IZAuI.png)

- Do not set proxy
- Set username : username
- Select guided disk partitionning

[![Process5](https://i.imgur.com/XkQY4fS.png)](i.imgur.com/XkQY4fS.png)

- Select the disk on which Debian will be installed

[![Process6](https://i.imgur.com/NjIx3Z9.png)](i.imgur.com/NjIx3Z9.png)

- Select All files in one partition
- Then select finish partitionning
- Validate the partitioning as follow,

[![Process7](https://i.imgur.com/uv0UeLu.png)](i.imgur.com/uv0UeLu.png)

- Choose the packages: SSH server, standard system utilities and pick your favorite GUI then press enter key

[![Process8](https://i.imgur.com/0xaF2qY.png)](i.imgur.com/0xaF2qY.png)

- Install the GRUB boot loader : yes and continue
- Turn off the machine closing the windows

[![Process9](https://i.imgur.com/Rt8KPMT.png)](i.imgur.com/Rt8KPMT.png)

- Delete the disk mini.iso from the disks in your VM's settings

[![Process10](https://i.imgur.com/PdC3Ys4.png)](i.imgur.com/PdC3Ys4.png)

The VM is now installed, enjoy !
