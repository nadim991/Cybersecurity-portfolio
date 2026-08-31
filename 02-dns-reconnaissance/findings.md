# DNS Reconnaissance Findings

## Target

appibrium.com

## A Records

The domain resolved to the following IPv4 addresses:

- 104.21.12.105
- 172.67.194.18

## AAAA Records

The domain resolved to the following IPv6 addresses:

- 2606:4700:3031::ac43:c212
- 2606:4700:3037::6815:c69

## Name Servers

The domain uses the following name servers:

- blakely.ns.cloudflare.com
- eugene.ns.cloudflare.com

## Mail Servers

The domain uses Zoho Mail servers:

- mx.zoho.com
- mx2.zoho.com
- mx3.zoho.com

## TXT Records

The following TXT records were identified:

- v=spf1 include:zohomail.com include:spf.resend.com ~all
- Zoho verification record
- Google site verification record

## DMARC

A DMARC record was identified:

- v=DMARC1
- p=reject
- adkim=s
- aspf=s
- rua=mailto:dmarc@appibrium.com

## DNSSEC

DNSRecon reported that DNSSEC is configured for the domain.

## Subdomains

The following subdomains were identified during enumeration:

- www.appibrium.com
- careers.appibrium.com

## Class C Network Ranges

The following ranges were identified by DNSenum:

- 104.21.12.0/24
- 172.67.194.0/24

## Zone Transfer

Zone transfer attempts against the identified name servers failed.

- blakely.ns.cloudflare.com: FORMERR
- eugene.ns.cloudflare.com: FORMERR

## Fierce Results

Fierce identified:

- careers.appibrium.com
- 104.21.12.105