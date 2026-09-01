# Wireshark Network Traffic Analysis

## Objective

The objective of this lab was to learn how to capture and analyze network traffic using Wireshark.

## Lab Environment

- Operating System: Kali Linux
- Virtualization: VMware
- Tool: Wireshark
- Target: Local lab environment

## Tasks Performed

1. Started Wireshark.
2. Selected the active network interface.
3. Captured network traffic.
4. Generated ICMP traffic using ping.
5. Generated DNS traffic using dig.
6. Applied Wireshark display filters.
7. Analyzed packet information.

## Traffic Analyzed

### ICMP

I used the following command to generate ICMP traffic:

`ping -c 4 8.8.8.8`

The `icmp` display filter was used to identify ICMP packets.

### DNS

I generated DNS traffic using:

`dig example.com`

The `dns` filter was used to identify DNS packets.

### TCP

The `tcp` filter was used to identify TCP traffic in the capture.

### HTTP

The `http` filter was used to identify HTTP traffic when available.

## Key Learning

This lab helped me understand how Wireshark can be used to:

- Capture network packets
- Identify different protocols
- Analyze source and destination addresses
- Inspect packet details
- Filter specific types of traffic
- Understand network communication

## Evidence

Screenshots of the packet captures and applied filters are included in the `screenshots` directory.

## Conclusion

Wireshark is useful for network monitoring, troubleshooting, traffic analysis, and security investigations.