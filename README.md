# Networking and Internet
## topic list
1. ipv4 addressing
2. packet snipping and traffic analysis
3. ipv4 multicast
4. ipv6
5. ipv6 transition
6. cellular network
7. Routing
8. ospf
9. BGP
10. MPLS/MPLS ipv6
11. VPN
12. mpls vpn
13. Qos
14. CDN


## Overview

Computer networking is the practice of connecting multiple computing devices to share resources, data, and communicate effectively. Networks enable devices such as computers, servers, routers, and switches to interact and exchange information. Here's a basic overview of the topic:

**Key Types of Networks**
- LAN (Local Area Network): A network confined to a small area like an office, home, or building.
- WAN (Wide Area Network): A network that spans large geographical areas, such as the internet.
- MAN (Metropolitan Area Network): A network designed for a city or large campus.
- PAN (Personal Area Network): A network for personal devices (e.g., Bluetooth or Wi-Fi for smartphones and laptops).

**Common Networking Devices**
- Router: Directs data packets between networks and manages traffic.
- Switch: Connects devices in a LAN and facilitates data exchange within it.
- Access Point: Enables wireless devices to connect to a network.
- Modem: Converts digital signals to analog for internet access.
- Firewall: Protects a network by filtering incoming and outgoing traffic.

**Networking Protocols**
Protocols are rules that define how data is transmitted over a network. Key examples:

- **TCP/IP:** Foundation of internet communication.

- **HTTP/HTTPS:** Protocols for accessing web pages.

- **FTP (File Transfer Protocol):** Used for transferring files.

- **DNS (Domain Name System):** Translates domain names to IP addresses.

- **SMTP/POP3/IMAP:** Used for sending and receiving emails.

# OSI Model
**The OSI (Open Systems Interconnection) model organizes networking into seven layers:**

**Physical:** Hardware transmission (cables, switches).

**Data Link:** MAC addresses, frames.

**Network:** IP addressing, routing.

**Transport**: Reliable data transfer (TCP/UDP).

**Session:** Manages sessions between applications.

**Presentation:** Data formatting and encryption.

**Application:** Interfaces for end-users (e.g., browsers, email).
## OSI and TCP/IP Models

The OSI (Open Systems Interconnection) and TCP/IP models are frameworks for understanding and designing network protocols and communication.

## OSI and TCP/IP Models

The OSI (Open Systems Interconnection) and TCP/IP models are frameworks for understanding and designing network protocols and communication.

### OSI Model
The OSI model has 7 layers, each with specific responsibilities:

1. **Application Layer**:
   - Provides network services directly to end-users or applications.
   - Protocols: HTTP, FTP, SMTP, POP3, IMAP.
2. **Presentation Layer**:
   - Ensures data is in a readable format for the application layer.
   - Handles encryption, compression, and translation.
   - Examples: SSL/TLS for encryption.
3. **Session Layer**:
   - Manages sessions and controls dialogues between computers.
   - Provides synchronization and checkpointing for data recovery.
   - Example: Session management in RPC (Remote Procedure Calls).
4. **Transport Layer**:
   - Ensures reliable data transfer with error detection and correction.
   - Handles flow control and segmentation of data.
   - Protocols: TCP (reliable, connection-oriented), UDP (faster, connectionless).
5. **Network Layer**:
   - Determines the best physical path for data transfer.
   - Handles logical addressing and routing.
   - Protocols: IP (IPv4, IPv6), ICMP, ARP.
6. **Data Link Layer**:
   - Ensures error-free data transfer between nodes on the same network.
   - Divided into two sublayers:
     - **MAC (Media Access Control)**: Handles access to the physical medium.
     - **LLC (Logical Link Control)**: Manages frame synchronization and error checking.
   - Protocols: Ethernet, Wi-Fi (802.11), PPP.
7. **Physical Layer**:
   - Defines hardware-level specifications for data transmission.
   - Includes cables, switches, NICs, and signal encoding.

### TCP/IP Model
The TCP/IP model simplifies communication by combining layers, focusing on the practical implementation of networking.

1. **Application Layer**:
   - Combines OSI’s Application, Presentation, and Session layers.
   - Provides protocols for data exchange between applications.
   - Protocols: HTTP, FTP, DNS, SMTP, SNMP.
2. **Transport Layer**:
   - Ensures reliable end-to-end communication and data integrity.
   - Manages error checking and retransmission of lost packets.
   - Protocols: TCP (reliable), UDP (faster, lightweight).
3. **Internet Layer**:
   - Handles logical addressing and routing across interconnected networks.
   - Ensures data packets are delivered to the correct destination.
   - Protocols: IP (IPv4, IPv6), ICMP, IGMP.
4. **Network Interface Layer**:
   - Combines OSI’s Data Link and Physical layers.
   - Manages hardware addressing and access to the transmission medium.
   - Protocols: Ethernet, Wi-Fi, ARP.

### Key Differences Between OSI and TCP/IP Models

| Aspect               | OSI Model                           | TCP/IP Model                     |
|----------------------|-------------------------------------|----------------------------------|
| **Structure**        | 7 layers                           | 4 layers                        |
| **Flexibility**      | Conceptual, not protocol-specific  | Protocol-oriented and practical |
| **Usage**            | Theoretical reference framework    | Widely used for real-world networking |
| **Reliability**      | Built-in session and presentation layers | Relies on the application to handle these aspects |

---
## Wireless Networking

**Wi-Fi:** Wireless connectivity within a network.

**Bluetooth:** Short-range wireless communication.

**Cellular Networks (4G/5G):** Mobile internet connectivity.

## Importance of Networking
- Enables resource sharing (files, printers).
- Facilitates communication (email, VoIP).
- Provides centralized data management.
- Supports cloud computing and remote work.




# 1. Network Topologies
Network topology refers to the arrangement of devices in a network. Key types include:

**Physical Topologies**

**Bus Topology:** All devices connect to a single central cable (the bus). Easy to set up but prone to failures if the main cable breaks.

**Star Topology:** Devices connect to a central hub/switch. Easy to troubleshoot but relies heavily on the central hub.

**Ring Topology:** Devices form a closed loop. Each device is connected to two others. Failure in one device can affect the entire network unless a dual-ring topology is used.

**Mesh Topology:** Devices are interconnected. High reliability but complex and expensive.

**Hybrid Topology:** Combines two or more types of topologies, e.g., star-bus or star-ring.

# 2. IP Addressing and Subnetting

## IP addresses uniquely identify devices on a network.

**IPv4 Addressing**

**Format:** Four 8-bit octets (e.g., 192.168.1.1).

# Subnetting: A Complete Guide

## 📌 Introduction
Subnetting is the process of dividing a large network into smaller, more manageable sub-networks (**subnets**). It improves network efficiency, security, and organization.

---

## 📌 IP Address Basics
An **IP address** consists of four octets (e.g., `192.168.1.1`), where each octet is an 8-bit number (0-255).

**Example:**
- **IP Address:** `192.168.1.1`
- **Binary Representation:** `11000000.10101000.00000001.00000001`

---

## 📌 Classes of IP Addresses

| Class | Range | Default Subnet Mask | Default Network Bits | Default Host Bits | No. of Hosts per Network |
|-------|------------|------------------|----------------|----------------|-------------------|
| **A** | `1.0.0.0 – 126.255.255.255` | `255.0.0.0` | 8 | 24 | 16,777,214 |
| **B** | `128.0.0.0 – 191.255.255.255` | `255.255.0.0` | 16 | 16 | 65,534 |
| **C** | `192.0.0.0 – 223.255.255.255` | `255.255.255.0` | 24 | 8 | 254 |
| **D** | `224.0.0.0 – 239.255.255.255` | **Reserved for Multicasting** | - | - | - |
| **E** | `240.0.0.0 – 255.255.255.255` | **Reserved for Experimental Use** | - | - | - |

---

## 📌 Subnet Mask
A **subnet mask** determines which portion of an IP address belongs to the **network** and which part belongs to **hosts**.

**Example:**
- **Subnet Mask:** `255.255.255.0`
- **Binary:** `11111111.11111111.11111111.00000000`

### Common Subnet Masks:

| Subnet Mask | CIDR Notation | No. of Subnets | Hosts per Subnet |
|-------------|--------------|---------------|------------------|
| `255.0.0.0` | `/8` | 1 | 16,777,214 |
| `255.255.0.0` | `/16` | 256 | 65,534 |
| `255.255.255.0` | `/24` | 65,536 | 254 |
| `255.255.255.128` | `/25` | 131,072 | 126 |
| `255.255.255.192` | `/26` | 262,144 | 62 |

---

## 📌 CIDR (Classless Inter-Domain Routing)
CIDR notation represents subnet masks using a **slash (/)** followed by the number of bits in the network portion.

**Examples:**
- `192.168.1.0/24` → `255.255.255.0` (256 addresses, 254 usable)
- `192.168.1.0/26` → `255.255.255.192` (64 addresses, 62 usable)

---

## 📌 Subnetting Calculation

### **Formula to calculate subnets & hosts:**
1. **Number of Subnets:** `2^n` (where `n` = borrowed bits)
2. **Number of Hosts per Subnet:** `2^h - 2` (where `h` = host bits, subtracting 2 for network & broadcast)

#### Example:
- **Given:** `192.168.1.0/26`
- **Subnet Mask:** `255.255.255.192`
- **Network Bits:** `26`
- **Host Bits:** `6`
- **Number of Subnets:** `2^2 = 4`
- **Hosts per Subnet:** `2^6 - 2 = 62`

| Subnet | First Usable IP | Last Usable IP | Broadcast |
|--------|---------------|--------------|-----------|
| `192.168.1.0/26` | `192.168.1.1` | `192.168.1.62` | `192.168.1.63` |
| `192.168.1.64/26` | `192.168.1.65` | `192.168.1.126` | `192.168.1.127` |
| `192.168.1.128/26` | `192.168.1.129` | `192.168.1.190` | `192.168.1.191` |
| `192.168.1.192/26` | `192.168.1.193` | `192.168.1.254` | `192.168.1.255` |

---

## 📌 VLSM (Variable Length Subnet Masking)
VLSM allows **different-sized subnets** in the same network, optimizing IP usage.

### Example:
- `/28` for small networks (**14 hosts**)
- `/26` for medium networks (**62 hosts**)
- `/24` for large networks (**254 hosts**)

---

## 📌 Subnetting Example

**Requirement:** Divide `192.168.10.0/24` into four subnets.

1. **Subnet Mask:** `/26` (255.255.255.192)
2. **Each subnet has:** `62` usable hosts
3. **New subnet ranges:**

| Subnet | First Usable IP | Last Usable IP | Broadcast |
|--------|---------------|--------------|-----------|
| `192.168.10.0/26` | `192.168.10.1` | `192.168.10.62` | `192.168.10.63` |
| `192.168.10.64/26` | `192.168.10.65` | `192.168.10.126` | `192.168.10.127` |
| `192.168.10.128/26` | `192.168.10.129` | `192.168.10.190` | `192.168.10.191` |
| `192.168.10.192/26` | `192.168.10.193` | `192.168.10.254` | `192.168.10.255` |

---

## 📌 Important Terms
- **Network Address:** First address in a subnet (e.g., `192.168.1.0`)
- **Broadcast Address:** Last address in a subnet (e.g., `192.168.1.255`)
- **Usable IPs:** All addresses between the network and broadcast
- **Public IP:** Used on the internet (e.g., `8.8.8.8`)
- **Private IP:** Used inside LAN (e.g., `192.168.1.x`)

---

## 📌 Why Subnet?
✅ **Efficient IP Allocation**  
✅ **Reduces Network Congestion**  
✅ **Improves Security**  
✅ **Enhances Routing Efficiency**  

---

### 🚀 Need subnetting practice problems or tools? Let me know! 😊

# 3. Routing
Routing determines how data packets travel from source to destination.

**Static Routing:** Manually configured routes.

**Dynamic Routing:** Uses algorithms and protocols like OSPF (Open Shortest Path First), BGP (Border Gateway Protocol), and RIP (Routing Information Protocol) to determine paths dynamically.

## Key Concepts:

**Default Gateway:** The router that forwards traffic to external networks.

**Routing Table:** Maintains information about network paths.

# 4. Network Security

Common Threats
DDoS (Distributed Denial of Service): Overwhelms a network with excessive traffic.
Man-in-the-Middle (MITM): Intercepts communication between two parties.
Phishing: Tricks users into revealing sensitive information.
Ransomware: Encrypts files and demands payment.
Security Measures
Firewalls: Blocks unauthorized traffic.
VPNs (Virtual Private Networks): Encrypts data between the user and the server.
Antivirus and IDS/IPS: Detects and prevents malware and intrusions.
Authentication Mechanisms: Use multi-factor authentication (MFA) and strong passwords.

# 5. Wireless Technologies

**Wi-Fi Standards (IEEE 802.11)**
802.11b: Speeds up to 11 Mbps.
802.11g: Speeds up to 54 Mbps.
802.11n: Speeds up to 600 Mbps.
802.11ac: Gigabit speeds on dual-band (2.4 GHz and 5 GHz).
802.11ax (Wi-Fi 6): Higher capacity and efficiency in dense environments.

## Frequency Bands
2.4 GHz: Longer range but slower speed.
5 GHz: Faster speed but shorter range.
Encryption Protocols
WEP (Weak security, outdated).
WPA/WPA2: Stronger security.
WPA3: Latest and most secure.


# 6. Protocols in Detail
TCP (Transmission Control Protocol)
Connection-oriented.
Ensures reliable data delivery.
Uses a 3-way handshake for connection setup.
UDP (User Datagram Protocol)
Connectionless.
Faster but less reliable (e.g., used in gaming, VoIP).
DNS (Domain Name System)
Resolves domain names (e.g., www.google.com) to IP addresses (e.g., 142.250.190.78).
Hierarchical structure with root, TLD (Top-Level Domain), and authoritative servers.
DHCP (Dynamic Host Configuration Protocol)
Automatically assigns IP addresses to devices.

# 7. Advanced Networking Concepts
NAT (Network Address Translation)
Converts private IP addresses to a public IP for internet access.
Types:
Static NAT: One-to-one mapping.
Dynamic NAT: Pool of public IPs assigned dynamically.
PAT (Port Address Translation): Many devices share one public IP.
VLAN (Virtual LAN)
Segments a physical network into multiple logical networks for security and efficiency.
SDN (Software-Defined Networking)
Centralized network control via software.
Separates the control plane from the data plane.
Cloud Networking
Provides network services like storage, servers, and applications over the internet (e.g., AWS, Azure).

# 8. Network Troubleshooting Tools

Ping: Tests connectivity between devices.
Traceroute: Tracks the path data takes to a destination.
NSLookup: Troubleshoots DNS-related issues.
Wireshark: Captures and analyzes network traffic.
Netstat: Displays network connections and stats.


# Advanced Networking Protocols

This document provides an in-depth overview of advanced networking protocols, their functions, and use cases. These protocols improve performance, reliability, and security in modern networks.

---

## Table of Contents

1. [MPLS (Multiprotocol Label Switching)](#mpls-multiprotocol-label-switching)
2. [BGP (Border Gateway Protocol)](#bgp-border-gateway-protocol)
3. [OSPF (Open Shortest Path First)](#ospf-open-shortest-path-first)
4. [EIGRP (Enhanced Interior Gateway Routing Protocol)](#eigrp-enhanced-interior-gateway-routing-protocol)
5. [IPv6 Advanced Protocols](#ipv6-advanced-protocols)
6. [VXLAN (Virtual Extensible LAN)](#vxlan-virtual-extensible-lan)
7. [LISP (Locator/ID Separation Protocol)](#lisp-locatorid-separation-protocol)
8. [SRv6 (Segment Routing over IPv6)](#srv6-segment-routing-over-ipv6)
9. [NetFlow and sFlow](#netflow-and-sflow)
10. [QUIC (Quick UDP Internet Connections)](#quic-quick-udp-internet-connections)
11. [RSVP (Resource Reservation Protocol)](#rsvp-resource-reservation-protocol)
12. [GRE (Generic Routing Encapsulation)](#gre-generic-routing-encapsulation)
13. [SNMP (Simple Network Management Protocol)](#snmp-simple-network-management-protocol)
14. [iSCSI (Internet Small Computer Systems Interface)](#iscsi-internet-small-computer-systems-interface)
15. [Zero Trust Networking Protocols](#zero-trust-networking-protocols)

---

## MPLS (Multiprotocol Label Switching)

MPLS directs data using short path labels instead of long network addresses.

- **Benefits**:
  - Reduces latency.
  - Improves traffic engineering.
  - Enhances scalability for service providers.
- **Use Cases**: WAN optimization, VPNs, and QoS (Quality of Service).

---

## BGP (Border Gateway Protocol)

BGP is a path-vector protocol used to route data between autonomous systems (AS) on the internet.

- **Key Features**:
  - Determines the best path based on policies and attributes.
  - Handles routing between ISPs or large networks.
- **Types**:
  - **eBGP (External BGP)**: Between different autonomous systems.
  - **iBGP (Internal BGP)**: Within the same autonomous system.

---

## OSPF (Open Shortest Path First)

OSPF is a link-state routing protocol for a single autonomous system.

- **How it Works**: Uses Dijkstra’s algorithm to calculate the shortest path.
- **Benefits**:
  - Quick convergence after changes.
  - Supports VLSM (Variable Length Subnet Masking).

---

## EIGRP (Enhanced Interior Gateway Routing Protocol)

A hybrid protocol developed by Cisco, combining distance-vector and link-state features.

- **Key Features**:
  - Rapid convergence through the Diffusing Update Algorithm (DUAL).
  - Supports unequal-cost load balancing.
- **Limitation**: Mostly vendor-specific to Cisco.

---

## IPv6 Advanced Protocols

IPv6 introduces advanced features beyond expanded addressing:

- **ICMPv6**: For error messages and neighbor discovery.
- **SLAAC (Stateless Address Autoconfiguration)**: Allows devices to configure IPv6 addresses automatically.
- **NDP (Neighbor Discovery Protocol)**: Replaces ARP in IPv6 networks.

---

## VXLAN (Virtual Extensible LAN)

VXLAN extends Layer 2 networks over Layer 3 for modern data centers.

- **Benefits**:
  - Scales beyond traditional VLAN limits.
  - Ideal for cloud environments.
- **How it Works**: Encapsulates Layer 2 frames into UDP packets with a VXLAN Network Identifier (VNI).

---

## LISP (Locator/ID Separation Protocol)

Separates device identity (Endpoint ID) from its location (Routing Locator).

- **Purpose**: Simplifies mobility and multi-homing.
- **Use Cases**: IoT, mobile networks, and dynamic environments.

---

## SRv6 (Segment Routing over IPv6)

Encodes routing paths directly in IPv6 headers for simplified traffic engineering.

- **Benefits**:
  - Reduces complexity.
  - Enhances programmability in SDN environments.

---

## NetFlow and sFlow

Traffic monitoring protocols for analytics:

- **NetFlow**:
  - Developed by Cisco.
  - Provides detailed Layer 3 and Layer 4 traffic data.
- **sFlow**:
  - Samples traffic data for lightweight monitoring.
  - Suitable for high-speed networks.

---

## QUIC (Quick UDP Internet Connections)

A transport-layer protocol developed by Google to improve HTTP performance.

- **Features**:
  - Built on UDP for low latency.
  - Reduces connection establishment time with multiplexing and encryption.
- **Applications**: Video streaming, gaming, and websites.

---

## RSVP (Resource Reservation Protocol)

Used for reserving network resources for real-time traffic like video conferencing.

- **Challenges**:
  - Complex implementation.
  - Scalability issues in large networks.

---

## GRE (Generic Routing Encapsulation)

Encapsulates data packets for transport over incompatible networks.

- **Benefits**:
  - Supports multicast traffic over VPNs.
  - Works with various Layer 3 protocols.
- **Drawback**: No built-in encryption.

---

## SNMP (Simple Network Management Protocol)

Monitors and manages network devices.

- **Components**:
  - **Managed Devices**: Devices being monitored.
  - **Agents**: Software collecting and sending data.
  - **NMS (Network Management System)**: Central monitoring console.
- **Versions**:
  - SNMPv1/v2: Basic functionality.
  - SNMPv3: Adds encryption and security.

---

## iSCSI (Internet Small Computer Systems Interface)

Protocol for connecting storage devices over IP networks.

- **Use Cases**: SAN (Storage Area Networks).
- **Benefits**:
  - Cost-effective compared to Fiber Channel.
  - Leverages existing IP infrastructure.

---

## Zero Trust Networking Protocols

Enforces strict identity verification for every device and user.

- **Key Protocols**:
  - **ZTNA (Zero Trust Network Access)**: Implements least privilege access.
  - **TLS/SSL**: Encrypts data in transit.
  - **OAuth/OpenID**: Manages secure authentication.

---

## NAT (Network Address Translation)

NAT is a method used to map private IP addresses to a public IP address and vice versa, enabling devices in a private network to communicate with external networks.

- **How it Works**:
  - Translates private IP addresses to a public IP address for outgoing traffic.
  - Maps incoming responses back to the originating private IP address.

- **Types of NAT**:
  1. **Static NAT**:
     - Maps one private IP to one public IP.
     - Useful for hosting services.
  2. **Dynamic NAT**:
     - Maps a group of private IPs to a pool of public IPs.
     - Allocates public IPs dynamically as needed.
  3. **PAT (Port Address Translation)**:
     - Maps multiple private IPs to a single public IP using unique port numbers.
     - Most commonly used.

- **Benefits**:
  - Conserves public IP addresses.
  - Enhances security by masking internal network structure.

- **Limitations**:
  - Can complicate peer-to-peer applications.
  - May introduce slight latency.

- **Use Cases**:
  - Home and enterprise networks.
  - Cloud services and VPNs.


