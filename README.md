# Task-5-Battu-Harsha-
This  repository contains of  Capturing and Analyzing Network Traffic using Wire Shark of Battu Harsha Vardhan Reddy batch 15
# Task-5-Battu-Harsha-
This  repository contains of  Capturing and Analyzing Network Traffic using Wire Shark of Battu Harsha Vardhan Reddy batch 15
Network Traffic Analysis with Wireshark Wireshark
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

# Protocols Identified :
# 1. ARP (Address Resolution Protocol) : Protocol that maps IP addresses to physical MAC addresses on local network segments.
arp
<img width="1919" height="849" alt="ICMP" src="https://github.com/user-attachments/assets/fb70034a-8d59-41d0-b56d-befe59a52bac" />
<img width="1918" height="852" alt="ARP" src="https://github.com/user-attachments/assets/4c3acc6f-391f-47cf-a32d-b495817f499a" />

Packets Analyzed: 19 ARP requests/responses
Function: MAC address resolution and network discovery
Environment: VMware virtual network


# 2. SSDP (Simple Service Discovery Protocol) : Network protocol used for advertisement and discovery of network services and device presence without manual configuration.  

<img width="1919" height="886" alt="MDNS" src="https://github.com/user-attachments/assets/003ae898-2aec-4ee4-9ea4-3dcaedc1d501" />
<img width="1919" height="888" alt="SSDP" src="https://github.com/user-attachments/assets/6fbb02cf-f9e2-46bc-96f1-70c2623a8474" />
IETF Datatracker
Packets Analyzed: HTTPU (HTTP over UDP) messages on port 1900  
www.ncsc.gov.ie

Types Observed:

M-SEARCH (Unicast or multicast discovery requests to find available services)

NOTIFY (Multicast announcements used to declare or withdraw device presence)

Purpose: Peer-to-peer device discovery and automatic connectivity (the backbone of Universal Plug and Play / UPnP).


# 3. mDNS (Multicast DNS) : Zero-configuration network protocol used to resolve hostnames to IP addresses within small networks without a local name server.
Packets Analyzed: mDNS queries and responses (UDP port 5353)


<img width="1913" height="881" alt="DHCP" src="https://github.com/user-attachments/assets/19ecbc83-7384-4ed4-9549-409304b99f92" />
<img width="1919" height="889" alt="ICMPV6" src="https://github.com/user-attachments/assets/3cee1a74-0e11-4fdf-b730-c7a786c11bbc" />
<img width="1919" height="886" alt="MDNS" src="https://github.com/user-attachments/assets/6a28729b-9d08-45c5-ad86-bc5c55b4179d" />
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

