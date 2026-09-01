# Nmap Network Scanning

## Overview

This project demonstrates network reconnaissance and service enumeration using Nmap against a deliberately vulnerable Metasploitable virtual machine.

## Objective

The objectives were:

- Identify whether the target host is active
- Discover open TCP ports
- Identify running services
- Detect service versions
- Identify the operating system
- Document potential attack surfaces

## Target

IP Address:

192.168.196.129

Environment:

Metasploitable VM
VMware

## Tools

- Nmap
- Kali Linux
- Metasploitable

## Scans Performed

### Host Discovery

```bash
nmap -sn 192.168.196.129