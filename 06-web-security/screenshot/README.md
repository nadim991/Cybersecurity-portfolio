# Web Security Assessment

## Overview

This project documents a web security assessment performed against a Metasploitable2 virtual machine in a controlled local lab environment.

## Target

IP Address: 192.168.196.129

## Objectives

The assessment focused on:

- Web server enumeration
- Technology identification
- Directory enumeration
- HTTP method analysis
- WebDAV configuration testing
- File upload testing

## Tools Used

- Nmap
- cURL
- WhatWeb
- Gobuster
- DAVTest

## Key Findings

- Apache 2.2.8 detected
- PHP 5.2.4 detected
- WebDAV enabled
- Multiple HTTP methods enabled on /dav/
- WebDAV allowed file uploads
- PHP file execution was reported by DAVTest

## Evidence

Screenshots are stored in the screenshots directory.

## Environment

Testing was performed against a deliberately vulnerable Metasploitable2 virtual machine in a local VMware lab.