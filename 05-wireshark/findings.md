# Wireshark Findings

## 1. ICMP Traffic

The ping command generated ICMP traffic between the Kali Linux system and 8.8.8.8.

The ICMP filter was used to isolate the relevant packets.

## 2. DNS Traffic

The `dig example.com` command generated DNS traffic.

The DNS packets showed communication related to resolving the domain name.

## 3. TCP Traffic

The TCP filter was used to identify TCP packets in the captured traffic.

TCP packets contain information such as source port, destination port, sequence information, and acknowledgment information.

## 4. Packet Inspection

Wireshark allowed individual packets to be expanded and inspected at different protocol layers.

This helped identify:

- Source IP
- Destination IP
- Protocol
- Packet length
- Protocol-specific information

## 5. Main Findings

- Network traffic can be captured and inspected using Wireshark.
- Display filters make it easier to isolate specific protocols.
- ICMP traffic can be observed during ping operations.
- DNS traffic can be observed during domain resolution.
- TCP traffic can be analyzed at the packet level.

## Security Relevance

Packet analysis can help security professionals identify unusual network activity, investigate incidents, troubleshoot connectivity problems, and understand how systems communicate.

## Conclusion

The lab provided practical experience with packet capture and protocol analysis using Wireshark.