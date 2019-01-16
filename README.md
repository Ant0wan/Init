# Init [![42](https://i.imgur.com/9NXfcit.jpg)](i.imgur.com/9NXfcit.jpg)

## System and Network Administration

This repository contains the scripts and answers to the <a href="https://cdn.intra.42.fr/pdf/pdf/886/fillit.en.pdf" target="_blank">init [a 42 project]</a>. Init is an introduction subject to system and network administration allowing 42's students to discover system and network basic commandsas well as many of the services used on a server machines.

This repository is split in 3 different parts: network, scripts, system.

---

## Network

The part “Network” has been done on school’s Macs running with Darwin Kernel Version 16.7.0.

---

## Scripts

This part can either be ran on a the Debian virtual machine or Macs (for vitual machine, please refers to Virtual Machine below section).

It contains:

- a script which displays only the login, UID and Path of each entry of the /etc/passwd file, 

- a script which delete an ACTIVE user on the VM (make sure you logged in ssh before), 

- and a password generator

[![passwordgenerator](https://i.imgur.com/IdsM678.gif)](i.imgur.com/IdsM678.gif)

---

## System

This part has been ran on a the Debian virtual machine (please refers to Virtual Machine below section).

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

- Display:

- Video Memory: 128MB
- Enable 3D Acceleration

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
