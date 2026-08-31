# DNS Reconnaissance

## Overview

This project demonstrates DNS reconnaissance techniques using Kali Linux.

The assessment focuses on identifying publicly available DNS information for the target domain.

## Target

appibrium.com

## Tools Used

- dig
- nslookup
- DNSRecon
- DNSenum
- Fierce

## DNS Records Investigated

- A
- AAAA
- MX
- NS
- TXT
- SOA

## Enumeration Activities

The following activities were performed:

1. DNS record enumeration
2. Name server identification
3. Mail server identification
4. TXT and email security record identification
5. DNSSEC identification
6. Subdomain enumeration
7. Class C network range identification
8. DNS zone transfer testing

## Key Findings

The reconnaissance identified IPv4 and IPv6 addresses, Cloudflare name servers, Zoho mail servers, TXT records, DMARC configuration, DNSSEC configuration, and subdomains.

Zone transfer attempts against the identified name servers were unsuccessful.

## Evidence

Command outputs and screenshots are stored in this directory.

## Disclaimer

This project was performed for educational and authorized security testing purposes.