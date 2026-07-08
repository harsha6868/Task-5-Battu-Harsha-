# Task-5-Battu-Harsha-
This  repository contains of  Capturing and Analyzing Network Traffic using Wire Shark of Battu Harsha Vardhan Reddy batch 15
Network Traffic Analysis with Wireshark , Wireshark
Network Analysis Platform Tool Protocols Status

# Project Overview :
This project demonstrates network packet capture and analysis using Wireshark to identify protocols and analyse traffic patterns in a controlled environment.

# Objective: Capture live network packets and identify basic protocols and traffic types using Wireshark.

# Tools Used:
Wireshark (Free network protocol analyzer)
VMware Virtual Environment
Firefox Browser (Traffic generation)
Target: testphp.vulnweb.com (Vulnerable web application for testing)

# Executive Summary:
Successfully captured and analyzed network packets, identified multiple protocols including HTTP, DNS, TCP, ICMP, NTP and ARP. The analysis revealed critical security vulnerabilities in unencrypted web traffic and demonstrated effective network monitoring techniques.
# Over view of wire shark
<img width="1918" height="852" alt="over view  of wire shark" src="https://github.com/user-attachments/assets/e1f3a141-0058-4433-852b-e879c872dabe" />

# Protocols Identified :
# 1. ARP (Address Resolution Protocol) : Protocol that maps IP addresses to physical MAC addresses on local network segments.
arp
<img width="1919" height="886" alt="MDNS" src="https://github.com/user-attachments/assets/640f457f-19b9-489d-9feb-aa5118428817" />
<img width="1091" height="376" alt="ARPWiresharkfilter" src="https://github.com/user-attachments/assets/ac67679f-2491-4b15-b909-6a1bb81602a6" />


Packets Analyzed: 19 ARP requests/responses
Function: MAC address resolution and network discovery
Environment: VMware virtual network


# 2. SSDP (Simple Service Discovery Protocol) : Network protocol used for advertisement and discovery of network services and device presence without manual configuration.  
<img width="1919" height="888" alt="SSDP" src="https://github.com/user-attachments/assets/f46a3457-2eaf-4333-ad2c-d746a3081318" />


IETF Datatracker
Packets Analyzed: HTTPU (HTTP over UDP) messages on port 1900  
www.ncsc.gov.ie

Types Observed:

M-SEARCH (Unicast or multicast discovery requests to find available services)

NOTIFY (Multicast announcements used to declare or withdraw device presence)

Purpose: Peer-to-peer device discovery and automatic connectivity (the backbone of Universal Plug and Play / UPnP).


# 3. mDNS (Multicast DNS) : Zero-configuration network protocol used to resolve hostnames to IP addresses within small networks without a local name server.
Packets Analyzed: mDNS queries and responses (UDP port 5353)
<img width="1919" height="886" alt="MDNS" src="https://github.com/user-attachments/assets/c2f6d9b3-d7d3-45d9-8c40-4bcf50b46b8f" />


Types Observed:

Standard Query (Multicast requests sent to find a specific device or service)

Standard Response (Multicast answers containing the device's IP address or service details)

Purpose: Local network hostname resolution and service discovery (powering services like Apple AirPlay, Bonjour, and Chromecast setup).


# 4. ICMPv6 (Internet Control Message Protocol version 6) : Core protocol for IPv6 that provides error reporting, diagnostic functions, and essential network-layer neighbor discovery mechanisms required for IPv6 operation.
Packets Analyzed: ICMPv6 messages (IPv6 Next Header value 58)

<img width="1919" height="889" alt="ICMPV6" src="https://github.com/user-attachments/assets/71613c49-2ac4-491a-9f8b-fb9191ad2a0b" />

Types Observed:

Neighbor Solicitation / Advertisement (Replaces IPv4 ARP for resolving local link-layer addresses)

Router Solicitation / Advertisement (Used for stateless autoconfiguration / SLAAC to automatically assign IP addresses)

Echo Request / Reply (ICMPv6-based ping diagnostics)

Purpose: Essential IPv6 network troubleshooting, automatic address assignment, and neighbor management without relying on a legacy centralized configuration.


# Methodology:
# Step-by-Step Process:
Environment Setup:

Installed Wireshark on VMware virtual machine sudo apt install wireshark
Configured network interface for packet capture
Traffic Generation

Browsed testphp.vulnweb.com
Performed DNS lookups (google.com)
Submitted forms with test data
Packet Capture

Duration: ~6 minutes
Total packets: 2,468
Interface: VMware virtual network adapter
Analysis Techniques

Protocol filtering (http, dns, arp)
Statistical analysis using Wireshark
Packet-level inspection and data extraction

# Application Layer
   ├── HTTP (Web traffic)
   ├── DNS (Name resolution)  
   └── NTP (Time synchronization)

# Transport Layer
   └── TCP (Reliable transport)

# Network Layer
   └── ICMP (Network diagnostics)

# Data Link Layer
   └── ARP (MAC address resolution)
# Skills Demonstrated:
Primary Skills:
> Network Protocol Analysis - Successfully identified and analyzed multiple protocols

> Security Assessment - Detected critical vulnerabilities in network traffic

>Forensic Analysis - Extracted sensitive data from packet captures

