# Subdomain Enumeration

## Overview

This project demonstrates passive subdomain enumeration using security reconnaissance tools.

The objective was to identify publicly discoverable subdomains and verify which discovered hosts were accessible over HTTP or HTTPS.

## Target

appibrium.com

## Tools

- Subfinder
- Amass
- httpx-toolkit

## Methodology

1. Enumerated subdomains using Subfinder.
2. Performed passive enumeration using Amass.
3. Tested discovered subdomains using httpx-toolkit.
4. Documented the results.
5. Captured screenshots as evidence.

## Results

Two subdomains were identified:

- studio.appibrium.com
- www.appibrium.com

Both were confirmed as HTTPS endpoints by httpx-toolkit.

Amass did not identify additional subdomains.

## Evidence

Screenshots are stored in the `screenshots` directory.

## Disclaimer

This project was performed for educational and authorized security testing purposes.