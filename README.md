# Init [![42](https://i.imgur.com/9NXfcit.jpg)](i.imgur.com/9NXfcit.jpg)

## System and Network Administration

This repository contains the scripts and answers to the <a href="https://cdn.intra.42.fr/pdf/pdf/886/fillit.en.pdf" target="_blank">init [a 42 project]</a>. Init is an introduction subject to system and network administration allowing 42's students to discover system and network basic commandsas well as many of the services used on a server machines.

This repository is split in 3 different parts: network, scripts, system.

## Network

The part “Network” has been done on school’s Macs running with Darwin Kernel Version 16.7.0.


## Scripts

This part can either be ran on a the Debian virtual machine or Macs (for vitual machine, please refers to Virtual Machine below section).


## System

This part has been ran on a the Debian virtual machine (please refers to Virtual Machine below section).


## Virtual Machine

The following config has been used: <a href="https://www.virtualbox.org/wiki/Downloads" target="_blank">VirtualBox 6.0.2</a> + <a href="http://ftp.nl.debian.org/debian/dists/stretch/main/installer-amd64/current/images/netboot/" target="_blank">Debian netboot mini.iso</a> 2018-11-10.

Virtual machine config:

- Name: debian_ontmp
- Type: Linux
- Version: Debian (64-bits)
- RAM: 2048MB
- Disks: VirtualBox Disk Image, dynamically allocated, 8GB, path: /tmp/[login]/

Settings:

- Processors: 4CPUs

Display:

- Video Memory: 128MB
- Enable 3D Acceleration

Network:

- Adapter 1: NAT
- Adapter 2: Bridged Adapter en0: Ethernet

This enables SSH connection required by the "system" part.

Boot has been made on mini.iso.
