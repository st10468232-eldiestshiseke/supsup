================================================================================
CONE5111 / CONE5111p / CONE5111w / NWEG5111
COMPUTER NETWORKS 1A - COMPREHENSIVE REVISION GUIDE WITH ANSWERS
================================================================================
Module Code: CONE5111/CONE5111p/CONE5111w/NWEG5111
NQF Level: 5
Qualification: BCA1/DMT1/DNM1/HSU1/HSU1p/BCA1w; DNM1w
Prescribed Text: West, J. (2022). CompTIA Network+: Guide to Networks, 9th Ed.

================================================================================
TABLE OF CONTENTS
================================================================================
1. LU1: NETWORK CONCEPTS & PRINCIPLES ................................. 1
   1.1 P2P vs. Client/Server Networks
   1.2 OSI Model (7 Layers)
   1.3 Network Topologies
   1.4 Troubleshooting Methodology
   1.5 Network Safety Practices

2. LU2: CABLING, DOCUMENTATION & CHANGE MANAGEMENT .................. 10
   2.1 Twisted Pair Cable Categories
   2.2 Fiber-Optic Cable Types
   2.3 Structured Cabling Standards
   2.4 Network Documentation Components
   2.5 Change Management Process
   2.6 Transmission Concepts

3. LU3: NETWORK ADDRESSING & PROTOCOLS ............................... 15
   3.1 MAC vs. IPv4 vs. IPv6 Addresses
   3.2 IPv4 Address Classes & Special Ranges
   3.3 CIDR & Subnetting
   3.4 DHCP Process
   3.5 NAT (Network Address Translation)
   3.6 Common Protocols & Ports
   3.7 DNS (Domain Name System)
   3.8 CLI Troubleshooting Commands

4. LU4: NETWORK ARCHITECTURE & SEGMENTATION .......................... 25
   4.1 Benefits of Network Segmentation
   4.2 VLANs (Virtual LANs)
   4.3 Virtualization & Cloud Models
   4.4 High Availability & Redundancy
   4.5 Subnetting Practice Problems

5. LU5: WANS & WIRELESS TRANSMISSIONS ................................. 30
   5.1 WAN Technologies Comparison
   5.2 Routing Fundamentals
   5.3 802.11 Wireless Standards
   5.4 Wireless Security
   5.5 Wireless Troubleshooting

6. LU6: SECURITY, RISK MANAGEMENT & DISASTER RECOVERY ................. 35
   6.1 CIA Triad
   6.2 Defence-in-Depth
   6.3 Firewalls, IDS, and IPS
   6.4 AAA (Authentication, Authorization, Accounting)
   6.5 Common Threats & Malware
   6.6 Device Hardening
   6.7 Risk Management Steps
   6.8 Network Performance Monitoring
   6.9 Disaster Recovery & Business Continuity
   6.10 Incident Response Lifecycle

7. EXAM PREPARATION TIPS ............................................. 45
   7.1 Task Words in Exam Questions
   7.2 Key Topics to Memorize
   7.3 Exam Strategies
   7.4 Final Checklist

================================================================================
LU1: NETWORK CONCEPTS & PRINCIPLES
================================================================================

---
1.1 Q: Compare P2P and Client/Server Networks
---
A:
+-------------------+------------------+------------------+
| FEATURE            | P2P              | CLIENT/SERVER    |
+-------------------+------------------+------------------+
| Cost              | Low              | High             |
| Scalability       | Poor (<10 users) | Excellent        |
| Security          | Decentralized    | Centralized      |
| Resource Sharing  | Each device shares its own resources | Central server provides resources |
| Management        | No dedicated admin | Requires IT staff |
| Use Case          | Small offices, home networks | Enterprises, universities |
+-------------------+------------------+------------------+

---

---
1.2 Q: Explain the 7 OSI Layers with Examples
---
A:
+-------+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| LAYER | NAME              | FUNCTION                                                                     | EXAMPLES            | DEVICES/PROTOCOLS |
+-------+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| 7     | Application       | User interfaces, network services                                           | HTTP, FTP, DNS, SMTP | Applications      |
| 6     | Presentation      | Data translation, encryption, compression                                   | SSL/TLS, JPEG, MPEG | -                 |
| 5     | Session           | Manages connections between applications                                    | NetBIOS, RPC       | -                 |
| 4     | Transport         | End-to-end communication, error recovery, flow control                   | TCP, UDP           | -                 |
| 3     | Network           | Logical addressing, routing                                                 | IP, ICMP, OSPF     | Routers           |
| 2     | Data Link         | Framing, MAC addressing, error detection                                     | Ethernet, PPP      | Switches, NICs    |
| 1     | Physical          | Raw bit transmission (cables, signals)                                     | Ethernet, Wi-Fi    | Hubs, NICs, Cables|
+-------+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

MNEMONIC: All People Seem To Need Data Processing (Top → Bottom)

---

---
1.3 Q: Describe Common Network Topologies with Pros/Cons
---
A:
+---------------+-------------------------------+-----------------------------------------------+-----------------------------------------------+-------------------+
| TOPOLOGY      | DESCRIPTION                   | PROS                                          | CONS                                          | USE CASE          |
+---------------+-------------------------------+-----------------------------------------------+-----------------------------------------------+-------------------+
| Star          | All devices to central switch | Easy to manage, scalable, no collisions        | Single point of failure (switch)             | Offices, homes    |
| Bus           | All devices on one cable      | Simple, cheap to implement                    | Collisions, difficult to troubleshoot          | Legacy networks   |
| Ring          | Devices in a loop              | No collisions (token passing), redundant     | Single failure breaks the ring                | Fiber networks    |
| Mesh          | Every device to every other   | High redundancy, fault-tolerant               | Expensive, complex to manage                  | Military networks |
| Hybrid        | Combination of topologies     | Flexible, scalable                            | Complex design                                | Enterprise networks|
| Tree          | Star networks to a bus         | Scalable, hierarchical                        | Single point of failure (root)                | Campuses          |
+---------------+-------------------------------+-----------------------------------------------+-----------------------------------------------+-------------------+

---

---
1.4 Q: Explain the 7-Step Troubleshooting Methodology with an Example
---
A:
+-------+-------------------------------+--------------------------------------------------+
| STEP  | DESCRIPTION                   | EXAMPLE (No Internet Access)                     |
+-------+-------------------------------+--------------------------------------------------+
| 1     | Identify the Problem           | User reports: "I can't access the internet."     |
| 2     | Establish a Theory             | Possible causes: Faulty cable, NIC failure, DHCP issue |
| 3     | Test the Theory                | Check link lights, try different cable/port, run ipconfig /all |
| 4     | Plan Action                    | Replace cable, restart NIC, or renew DHCP lease   |
| 5     | Implement Solution             | Replace the faulty Ethernet cable               |
| 6     | Verify Functionality          | Test internet access, run ping 8.8.8.8          |
| 7     | Document Findings              | Log: "User X's cable was damaged; replaced with Cat6." |
+-------+-------------------------------+--------------------------------------------------+

---

---
1.5 Q: List and Explain 5 Network Safety Practices
---
A:
1. ESD Protection: Use anti-static wrist straps when handling components (e.g., RAM, NICs).
2. Power Protection: Use UPS for critical devices and surge protectors to prevent damage.
3. Cable Management: Label all cables and avoid sharp bends (exceeding bend radius).
4. Access Control: Lock server rooms and use keycard access for sensitive areas.
5. Hazard Reporting: Report hazards immediately and follow correct lifting techniques.

---

================================================================================
LU2: CABLING, DOCUMENTATION & CHANGE MANAGEMENT
================================================================================

---
2.1 Q: Compare Twisted Pair Cable Categories (Cat5e, Cat6, Cat6a)
---
A:
+-------------------+----------+----------+----------+
| FEATURE            | Cat5e    | Cat6     | Cat6a    |
+-------------------+----------+----------+----------+
| Max Speed         | 1 Gbps   | 10 Gbps  | 10 Gbps  |
| (at 100m)         | (100m)   | (55m)    | (100m)   |
| Bandwidth         | 100 MHz  | 250 MHz  | 500 MHz  |
| Crosstalk Resist. | Moderate | Better   | Best     |
| Shielding        | UTP      | UTP/STP  | STP      |
| Cost             | Cheapest | Moderate | Expensive|
| Use Case         | Legacy   | Offices  | Data centers |
+-------------------+----------+----------+----------+

---

---
2.2 Q: Explain Fiber-Optic Cable Types (Single-Mode vs. Multi-Mode)
---
A:
+---------------------------+-----------------------------+-----------------------------+
| FEATURE                  | SINGLE-MODE FIBER (SMF)     | MULTI-MODE FIBER (MMF)      |
+---------------------------+-----------------------------+-----------------------------+
| Light Source             | Laser                      | LED                        |
| Core Diameter            | 8-10 microns (thin)         | 50-62.5 microns (thick)    |
| Distance                 | Up to 80km+ (long-haul)    | Up to 550m (short-haul)    |
| Bandwidth                | Very high (100 Gbps+)       | Moderate (10 Gbps)         |
| Cost                     | Expensive                  | Cheaper                    |
| Use Case                 | ISPs, WANs, backbone links | LANs, data centers         |
| Color (Jacket)           | Typically yellow           | Typically orange/aqua      |
+---------------------------+-----------------------------+-----------------------------+

---

---
2.3 Q: What are the 3 Basic Types of Structured Cabling?
---
A:
1. HORIZONTAL CABLING: Runs from workstation outlets to the telecommunications closet (max 90m for copper).
2. BACKBONE CABLING: Connects telecommunications closets, equipment rooms, and entrance facilities (uses fiber or high-grade copper).
3. WORK AREA CABLING: From the wall jack to the end device (e.g., PC, phone).

---

---
2.4 Q: What are the Components of Network Documentation?
---
A:
1. Network Diagrams (Logical: IPs, subnets, VLANs; Physical: cable routes, rack layouts).
2. IP Address Scheme (Subnet allocations, DHCP ranges, reserved IPs).
3. Device Configurations (Backup configs for routers, switches, firewalls).
4. Cabling Layouts (Patch panel ports, cable types, lengths, labels).
5. Policies & Procedures (Password policies, change management workflows).
6. Inventory List (Hardware/software versions, serial numbers, warranties).
7. Change Logs (Record of all changes: who, what, when, why).

---

---
2.5 Q: Explain the 6-Step Change Management Process
---
A:
1. REQUEST: Submit a change request with justification, scope, and impact assessment.
2. REVIEW: Change Advisory Board (CAB) evaluates risk and approves/rejects.
3. PLAN: Define rollback plan, schedule, resources, and communication plan.
4. TEST: Test in a lab/non-production environment first.
5. IMPLEMENT: Execute change during the scheduled maintenance window.
6. DOCUMENT: Record what was done, who performed it, when, and the outcome.

KEY PRINCIPLE: Every change must be auditable and reversible.

---

---
2.6 Q: Explain Key Transmission Concepts
---
A:
+-------------------+-----------------------------------------------------------------------------+--------------------------+-----------------------------+
| CONCEPT           | DEFINITION                                                                     | EXAMPLE                  | MITIGATION                 |
+-------------------+-----------------------------------------------------------------------------+--------------------------+-----------------------------+
| Bandwidth         | Maximum data capacity of a link (e.g., 1 Gbps). Theoretical maximum.       | 1 Gbps Ethernet link     | Upgrade to higher bandwidth|
| Throughput        | Actual data transfer rate achieved in practice. Always <= bandwidth.        | 800 Mbps on 1 Gbps link  | Optimize configuration      |
| Latency           | Delay between sender and receiver (measured in ms).                         | 50ms ping time           | Use faster media (fiber)   |
| Attenuation       | Signal weakening over distance.                                              | Wi-Fi signal drops at 100m | Use repeaters/fiber        |
| Crosstalk         | Interference between adjacent cables.                                       | Cat5e near power lines  | Use STP or fiber          |
| EMI/RFI           | Electromagnetic/Radio Frequency Interference.                              | Fluorescent lights        | Use STP or fiber          |
| Multiplexing      | Combining multiple signals on one medium.                                   | TDM (24 calls on T1)     | Use FDM, TDM, or WDM      |
+-------------------+-----------------------------------------------------------------------------+--------------------------+-----------------------------+

---

---
2.7 Q: What is the Purpose of a Crossover Cable?
---
A:
- DEFINITION: A cable that swaps transmit/receive pairs (e.g., Pin 1 → Pin 3, Pin 2 → Pin 6).
- USE CASE: Connects similar devices directly (e.g., switch-to-switch, PC-to-PC).
- WHY OBSOLETE? Modern Ethernet ports (Gigabit+) support Auto-MDI/MDIX, which automatically detects and configures the connection. Straight-through cables now work for all connections.

---

================================================================================
LU3: NETWORK ADDRESSING & PROTOCOLS
================================================================================

---
3.1 Q: Differentiate Between MAC, IPv4, and IPv6 Addresses
---
A:
+---------------------------+--------------------------------------+---------------------------------------+---------------------------------------+
| FEATURE                   | MAC ADDRESS                          | IPv4 ADDRESS                          | IPv6 ADDRESS                          |
+---------------------------+--------------------------------------+---------------------------------------+---------------------------------------+
| Format                    | 48-bit hex (AA:BB:CC:DD:EE:FF)       | 32-bit dotted-decimal (192.168.1.10)   | 128-bit hex (2001:0db8::1)             |
| Layer                     | Layer 2 (Data Link)                  | Layer 3 (Network)                     | Layer 3 (Network)                     |
| Purpose                   | Identifies NICs on a LAN             | Identifies devices on a network       | Identifies devices on a network       |
| Scope                     | Local (LAN only)                    | Global (routable on internet)        | Global (routable on internet)        |
| Assignment                | Burned into NIC (hardware)           | Configured manually or via DHCP       | Configured manually or via DHCPv6     |
| Example                   | 00:1A:2B:3C:4D:5E                   | 192.168.1.10                          | 2001:0db8:85a3::8a2e:0370:7334      |
| Special Ranges            | -                                    | Private: 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | Unique Local: FC00::/7               |
+---------------------------+--------------------------------------+---------------------------------------+---------------------------------------+

---

---
3.2 Q: Explain IPv4 Address Classes and Special Ranges
---
A:
+-------+-------------------------------+---------------------+--------------------------+-----------------------------+
| CLASS | RANGE                         | DEFAULT SUBNET MASK | USE CASE                | PRIVATE RANGES            |
+-------+-------------------------------+---------------------+--------------------------+-----------------------------+
| A     | 1.0.0.0 – 126.255.255.255     | 255.0.0.0 (/8)       | Large networks          | 10.0.0.0/8                 |
| B     | 128.0.0.0 – 191.255.255.255   | 255.255.0.0 (/16)    | Medium networks         | 172.16.0.0 – 172.31.255.255 |
| C     | 192.0.0.0 – 223.255.255.255   | 255.255.255.0 (/24)  | Small networks          | 192.168.0.0/16             |
| D     | 224.0.0.0 – 239.255.255.255   | N/A                   | Multicast               | -                           |
| E     | 240.0.0.0 – 255.255.255.255   | N/A                   | Experimental            | -                           |
+-------+-------------------------------+---------------------+--------------------------+-----------------------------+

SPECIAL IPv4 ADDRESSES:
- Loopback: 127.0.0.0/8 (e.g., 127.0.0.1 for localhost).
- APIPA: 169.254.0.0/16 (assigned when DHCP fails).
- Broadcast: 255.255.255.255 (limited broadcast).
- Network ID: All host bits 0 (e.g., 192.168.1.0/24).
- Broadcast ID: All host bits 1 (e.g., 192.168.1.255/24).

---

---
3.3 Q: Explain CIDR and Subnetting with Examples
---
A:
CIDR (Classless Inter-Domain Routing):
- Purpose: Eliminates class boundaries (A, B, C) for efficient IP allocation.
- Notation: IP/prefix (e.g., 192.168.1.0/24).
- Prefix Length: Number of network bits (e.g., /24 = 24 network bits, 8 host bits).

SUBNETTING STEPS:
1. Determine the number of subnets and hosts needed.
2. Borrow bits from the host portion to create subnets.
3. Calculate:
   - Subnet Mask: Convert prefix to dotted-decimal (e.g., /26 = 255.255.255.192).
   - Network Address: All host bits 0.
   - Broadcast Address: All host bits 1.
   - Usable Host Range: Network +1 to Broadcast -1.

EXAMPLES:
+------+------------------------+------------------+-------------------+---------------------+
| CIDR | SUBNET MASK           | USABLE HOSTS     | NETWORK EXAMPLE   | BROADCAST EXAMPLE   |
+------+------------------------+------------------+-------------------+---------------------+
| /24  | 255.255.255.0          | 254              | 192.168.1.0       | 192.168.1.255       |
| /25  | 255.255.255.128        | 126              | 192.168.1.0       | 192.168.1.127       |
| /26  | 255.255.255.192        | 62               | 192.168.1.0       | 192.168.1.63        |
| /27  | 255.255.255.224        | 30               | 192.168.1.0       | 192.168.1.31        |
+------+------------------------+------------------+-------------------+---------------------+

VLSM (Variable Length Subnet Masking):
- Allows different subnet sizes in the same network.
- Example: Divide 192.168.1.0/24 into:
  - 192.168.1.0/26 (62 hosts for Sales)
  - 192.168.1.64/26 (62 hosts for HR)
  - 192.168.1.128/27 (30 hosts for Finance)

---

---
3.4 Q: Explain DHCP and Its 4-Step Process
---
A:
DHCP (Dynamic Host Configuration Protocol):
- Automatically assigns IP addresses, subnet masks, gateways, and DNS servers.
- Eliminates manual configuration and IP conflicts.

4-STEP PROCESS (DORA):
1. DISCOVER: Client broadcasts DHCP Discover (source IP: 0.0.0.0, dest: 255.255.255.255).
2. OFFER: Server responds with DHCP Offer (proposed IP, subnet mask, lease time, gateway, DNS).
3. REQUEST: Client broadcasts DHCP Request to accept the offered IP.
4. ACKNOWLEDGE (ACK): Server sends DHCP ACK to confirm the lease.

LEASE TIME:
- IP is temporarily assigned (default: 24 hours).
- Client must renew the lease before it expires (typically at 50% and 87.5% of lease time).

---

---
3.5 Q: Explain NAT (Network Address Translation)
---
A:
PURPOSE OF NAT:
1. Conserves Public IPs: Allows thousands of private IPs to share one public IP.
2. Security: Hides internal IPs from the internet (harder to attack).
3. Enables Internet Access: Devices with private IPs can access the internet.

TYPES OF NAT:
+------------------------+-----------------------------------------------------------------------------+---------------------+
| TYPE                  | DESCRIPTION                                                                 | EXAMPLE             |
+------------------------+-----------------------------------------------------------------------------+---------------------+
| Static NAT            | One-to-one mapping of private to public IPs.                              | Server hosting a website |
| Dynamic NAT           | Pool of public IPs assigned dynamically to private IPs.                    | Small office with 5 public IPs |
| PAT (Port Address Translation) | Many-to-one mapping using port numbers. Most common type.            | Home router with 1 public IP |
| SNAT (Source NAT)      | Changes the source IP in outbound traffic.                                 | Outgoing traffic from a private network |
| DNAT (Destination NAT) | Changes the destination IP in inbound traffic.                           | Port forwarding (e.g., RDP to a server) |
+------------------------+-----------------------------------------------------------------------------+---------------------+

HOW PAT WORKS:
- Multiple devices share one public IP.
- Each connection uses a unique port number (e.g., PublicIP:5000, PublicIP:5001).
- Example: 5 clients in an office can access the internet using 1 public IP via PAT.

---

---
3.6 Q: List and Explain Common Protocols and Ports
---
A:
+--------------------+----------+-----------+-----------------------------------------------------------------------------+---------------------+
| PROTOCOL          | PORT     | LAYER     | PURPOSE                                                                     | EXAMPLE USE         |
+--------------------+----------+-----------+-----------------------------------------------------------------------------+---------------------+
| HTTP              | 80       | Application| Unencrypted web traffic.                                                    | Browsing websites   |
| HTTPS             | 443      | Application| Encrypted web traffic (HTTP + SSL/TLS).                                   | Secure websites    |
| FTP               | 20, 21   | Application| File transfer (port 21: control, port 20: data).                         | Uploading files     |
| SFTP              | 22       | Application| Secure file transfer (FTP over SSH).                                       | Secure file transfers |
| SSH               | 22       | Application| Secure remote shell access.                                                | Managing servers    |
| Telnet            | 23       | Application| UNENCRYPTED remote access. AVOID IN PRODUCTION.                           | Legacy devices      |
| SMTP              | 25       | Application| Sending email.                                                             | Email servers       |
| IMAP              | 143      | Application| Retrieving email (keeps copies on server).                                  | Email clients       |
| POP3              | 110      | Application| Retrieving email (downloads to local device).                              | Email clients       |
| DNS               | 53       | Application| Resolves hostnames to IPs (UDP for queries, TCP for zone transfers).      | Browsing internet   |
| DHCP              | 67, 68   | Application| Dynamic IP assignment (server: 67, client: 68).                           | Auto IP config      |
| SNMP              | 161      | Application| Network device monitoring.                                                | Monitoring devices  |
| RDP               | 3389     | Application| Remote Desktop Protocol (Windows).                                         | Remote access       |
+--------------------+----------+-----------+-----------------------------------------------------------------------------+---------------------+

---

---
3.7 Q: Explain DNS (Domain Name System)
---
A:
PURPOSE OF DNS:
- Translates human-readable hostnames (e.g., www.google.com) to IP addresses (e.g., 142.250.190.46).
- Eliminates the need to memorize IP addresses.

DNS COMPONENTS:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| COMPONENT         | ROLE                                                                        | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| DNS Client        | Queries DNS servers for name resolution.                                    | Your PC or phone    |
| Resolver          | Typically your ISP's DNS server (e.g., 8.8.8.8).                           | Google DNS          |
| Root DNS Server   | Top-level DNS server; refers queries to TLD servers.                      | . (root zone)      |
| TLD Server        | Manages top-level domains (e.g., .com, .za).                                | .com TLD server    |
| Authoritative DNS Server | Holds the actual DNS records for a domain.                          | ns1.example.com    |
+-------------------+-----------------------------------------------------------------------------+---------------------+

DNS RECORD TYPES:
+-----------------+-----------------------------------------------------------------------------+---------------------+
| RECORD TYPE     | PURPOSE                                                                     | EXAMPLE             |
+-----------------+-----------------------------------------------------------------------------+---------------------+
| A               | Maps hostname to IPv4 address.                                             | example.com → 192.0.2.1 |
| AAAA            | Maps hostname to IPv6 address.                                             | example.com → 2001:db8::1 |
| CNAME           | Alias for another hostname.                                                | www.example.com → example.com |
| MX              | Mail server for a domain.                                                   | example.com → mail.example.com |
| NS              | Nameserver for a domain.                                                    | example.com → ns1.example.com |
| TXT             | Text records (e.g., SPF, DKIM for email security).                         | v=spf1 include:_spf.google.com ~all |
| SOA             | Start of Authority (zone information).                                     | Admin contact, refresh intervals |
+-----------------+-----------------------------------------------------------------------------+---------------------+

DNS QUERY TYPES:
1. RECURSIVE QUERY: Client asks DNS server for a full resolution. Server MUST return the final answer (or an error).
   Example: Your PC asks Google DNS (8.8.8.8) for www.google.com.
2. ITERATIVE QUERY: DNS server provides the best referral it has. Client must query the next server in the hierarchy.
   Example: Root DNS refers to .com TLD, which refers to Google's authoritative server.

TTL (TIME TO LIVE):
- Specifies how long (in seconds) a DNS record can be cached.
- Prevents stale records by forcing re-query after TTL expires.
- Example: TTL=3600 (1 hour) means the record must be refreshed after 1 hour.

---

---
3.8 Q: Explain CLI Troubleshooting Commands
---
A:
+---------------------------+-----------------------------------------------------------------------------+---------------------+---------------------------------------+
| COMMAND                   | PURPOSE                                                                     | EXAMPLE             | OUTPUT INTERPRETATION                |
+---------------------------+-----------------------------------------------------------------------------+---------------------+---------------------------------------+
| ping                      | Tests ICMP reachability to a host (Layer 3 test).                     | ping 8.8.8.8       | Success: Replies. Failure: "Request timed out" |
| tracert / traceroute     | Shows each hop to a destination. Identifies where failure occurs.   | tracert google.com | Lists routers/latency per hop. * = timeout |
| ipconfig / ifconfig       | Displays TCP/IP configuration of local adapters.                     | ipconfig /all      | Shows IP, subnet mask, gateway, DNS, MAC |
| nslookup / dig           | Queries DNS for name resolution.                                           | nslookup google.com | Returns IP address for hostname |
| netstat                  | Shows active connections, listening ports, routing table.             | netstat -ano       | Lists all connections and PIDs |
| arp -a                   | Displays ARP cache (IP-to-MAC mappings on local segment).             | arp -a             | Shows devices on the same LAN |
| route print / ip route   | Shows and manages the routing table.                                      | route print        | Lists network destinations and next hops |
| nmap                     | Network scanner; discovers hosts and open ports.                         | nmap -sS 192.168.1.1 | Lists open ports on a host |
| netsh                    | Windows network configuration tool.                                         | netsh interface ip show config | Shows IP config for all interfaces |
+---------------------------+-----------------------------------------------------------------------------+---------------------+---------------------------------------+

---

================================================================================
LU4: NETWORK ARCHITECTURE & SEGMENTATION
================================================================================

---
4.1 Q: Explain the Benefits of Network Segmentation
---
A:
+---------------------------+-----------------------------------------------------------------------------+---------------------+
| BENEFIT                  | EXPLANATION                                                                 | EXAMPLE             |
+---------------------------+-----------------------------------------------------------------------------+---------------------+
| Reduced Broadcast Domains | Limits broadcast traffic to a segment, reducing congestion.              | VLANs separate departments |
| Improved Security        | Isolates sensitive traffic (e.g., finance, HR) from the rest of the network. | Finance VLAN blocked from guest VLAN |
| Better Performance       | Reduces collisions and congestion in large networks.                     | Separate VoIP and data traffic |
| Simplified Management     | Logical grouping by function/department (e.g., Sales, IT).             | VLAN 10 = Sales, VLAN 20 = IT |
| Easier Troubleshooting    | Smaller failure domains (issues are contained to a segment).             | Network issue in VLAN 10 doesn't affect VLAN 20 |
| Regulatory Compliance     | Meets legal/industry requirements for data isolation.                     | PCI-DSS for payment systems |
+---------------------------+-----------------------------------------------------------------------------+---------------------+

---

---
4.2 Q: Explain VLANs (Virtual LANs)
---
A:
WHAT IS A VLAN?
- A logical grouping of devices regardless of physical location.
- Devices in the same VLAN can communicate directly (Layer 2).
- Devices in different VLANs require a router or Layer 3 switch to communicate.

TYPES OF VLANS:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| TYPE              | DESCRIPTION                                                                 | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| Default VLAN      | All ports are in VLAN 1 by default (should be DISABLED for security).   | VLAN 1 (unused)     |
| Data VLAN         | Carries user traffic (e.g., departments).                                  | VLAN 10 (Sales)    |
| Voice VLAN        | Carries VoIP traffic (prioritized for quality).                         | VLAN 100 (VoIP)    |
| Native VLAN       | Untagged traffic on a trunk port (default: VLAN 1).                        | Native VLAN = 99   |
| Management VLAN   | Used for admin access to switches/routers.                                 | VLAN 99 (Admin)    |
+-------------------+-----------------------------------------------------------------------------+---------------------+

VLAN TAGGING (802.1Q):
- TAGGED PORTS (TRUNK PORTS): Carry traffic for multiple VLANs. Add a 4-byte tag to frames (VLAN ID, priority). Used between switches or switch-to-router.
- UNTAGGED PORTS (ACCESS PORTS): Carry traffic for a single VLAN. No tag added (assumes default VLAN if not specified).

INTER-VLAN ROUTING:
- PROBLEM: Devices in different VLANs cannot communicate at Layer 2.
- SOLUTION:
  1. ROUTER-ON-A-STICK: Single router with sub-interfaces for each VLAN.
  2. LAYER 3 SWITCH: Switch with IP routing enabled (faster, more scalable).

---

---
4.3 Q: Explain Virtualization and Cloud Models
---
A:
VIRTUALIZATION:
- Definition: Running multiple virtual machines (VMs) on a single physical host.
- Purpose: Improves resource utilization and flexibility.

HYPERVISOR TYPES:
+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| TYPE              | DESCRIPTION                                                                 | EXAMPLES            | USE CASE          |
+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| Type 1 (Bare-Metal) | Runs directly on hardware (no OS).                                       | Hyper-V, ESXi, KVM | Enterprise data centers |
| Type 2 (Hosted)   | Runs on top of an OS (e.g., Windows, Linux).                               | VirtualBox, VMware Workstation | Development, testing |
+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

CLOUD SERVICE MODELS:
+-------+-----------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| MODEL | FULL NAME                   | DESCRIPTION                                                                 | EXAMPLES            | YOUR RESPONSIBILITY |
+-------+-----------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| IaaS  | Infrastructure as a Service  | VMs, storage, networking (you manage OS and above).                       | AWS EC2, Azure VMs | OS, apps, data, runtime |
| PaaS  | Platform as a Service        | Managed runtime environment (you manage apps and data).                  | AWS Elastic Beanstalk, Heroku | Apps, data |
| SaaS  | Software as a Service        | Full application delivered online (provider manages all).               | Gmail, Office 365, Salesforce | User data/configuration |
+-------+-----------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

CLOUD DEPLOYMENT MODELS:
+-----------------+-----------------------------------------------------------------------------+---------------------+
| MODEL           | DESCRIPTION                                                                 | EXAMPLE             |
+-----------------+-----------------------------------------------------------------------------+---------------------+
| Public Cloud    | Services over the public internet by third-party providers.               | AWS, Azure, Google Cloud |
| Private Cloud   | Cloud infrastructure dedicated to a single organization.               | On-premises OpenStack |
| Hybrid Cloud    | Combines public and private clouds.                                         | AWS + on-premises data center |
| Community Cloud | Shared by multiple organizations with similar needs.                     | Government agencies sharing a cloud |
+-----------------+-----------------------------------------------------------------------------+---------------------+

CLOUD BENEFITS:
1. Scalability: Easily add/remove resources as needed.
2. Elasticity: Automatically scale up/down based on demand.
3. Pay-per-Use: Pay only for what you use (no upfront hardware costs).
4. Geographic Redundancy: Deploy in multiple regions for disaster recovery.
5. High Availability: Built-in redundancy and failover.

---

---
4.4 Q: Explain High Availability and Redundancy
---
A:
+---------------------------+-----------------------------------------------------------------------------+---------------------+
| CONCEPT                  | DESCRIPTION                                                                 | EXAMPLE             |
+---------------------------+-----------------------------------------------------------------------------+---------------------+
| High Availability (HA)   | Systems designed to be operational nearly 100% of the time.               | 99.9% uptime = ~8.76 hours downtime/year |
| Redundancy               | Duplicate components to prevent single points of failure.                 | Dual power supplies, backup links |
| Load Balancing           | Distributes traffic across multiple servers to prevent overload.         | F5 BIG-IP, AWS ELB |
| Failover                 | Automatic switch to a backup system when primary fails.                | Primary server → Backup server |
| RAID                     | Redundant Array of Inexpensive Disks (data redundancy at storage level). | RAID 1 (mirroring), RAID 5 (parity) |
| UPS                      | Uninterruptible Power Supply keeps systems running during outages.      | APC UPS for servers |
| SLA                      | Service Level Agreement defining uptime guarantees.                       | 99.99% uptime SLA |
+---------------------------+-----------------------------------------------------------------------------+---------------------+

---

---
4.5 Q: Subnetting Practice Problems
---
A:
PROBLEM 1: Calculate Usable Hosts
- Given: 192.168.1.0/24
- Subnet Mask: 255.255.255.0
- Usable Hosts: 2^(32-24) - 2 = 256 - 2 = 254
- Network Address: 192.168.1.0
- Broadcast Address: 192.168.1.255
- Usable Range: 192.168.1.1 to 192.168.1.254

PROBLEM 2: Divide into Subnets
- Given: 192.168.10.0/24 (256 addresses)
- Requirement: 4 subnets with ~60 hosts each.
- Solution:
  - Borrow 2 bits from host portion (2^2 = 4 subnets).
  - New prefix: /26 (24 + 2).
  - Subnet Mask: 255.255.255.192
  - Subnets:
    1. 192.168.10.0/26 (Hosts: .1–.62, Broadcast: .63)
    2. 192.168.10.64/26 (Hosts: .65–.126, Broadcast: .127)
    3. 192.168.10.128/26 (Hosts: .129–.190, Broadcast: .191)
    4. 192.168.10.192/26 (Hosts: .193–.254, Broadcast: .255)

PROBLEM 3: VLSM Example
- Given: 10.0.0.0/24
- Requirement:
  - Subnet A: 100 hosts (Sales)
  - Subnet B: 50 hosts (HR)
  - Subnet C: 20 hosts (Finance)
- Solution:
  1. Subnet A (Sales): Needs 100 hosts → 2^7 - 2 = 126 → /25 (255.255.255.128). 10.0.0.0/25 (Hosts: .1–.126, Broadcast: .127).
  2. Subnet B (HR): Needs 50 hosts → 2^6 - 2 = 62 → /26 (255.255.255.192). 10.0.0.128/26 (Hosts: .129–.190, Broadcast: .191).
  3. Subnet C (Finance): Needs 20 hosts → 2^5 - 2 = 30 → /27 (255.255.255.224). 10.0.0.192/27 (Hosts: .193–.222, Broadcast: .223).

---

================================================================================
LU5: WANS & WIRELESS TRANSMISSIONS
================================================================================

---
5.1 Q: Compare WAN Technologies
---
A:
+----------------------+-----------------------------------------------------------------------------+---------------------+----------------+-------------------+-------------------+-------------------+
| TECHNOLOGY          | DESCRIPTION                                                                 | SPEED              | COST          | USE CASE          | PROS              | CONS              |
+----------------------+-----------------------------------------------------------------------------+---------------------+----------------+-------------------+-------------------+-------------------+
| Leased Lines (MPLS) | Dedicated private connection. High reliability.                        | 10 Mbps – 10 Gbps  | Very High      | Enterprises, banks | High reliability, low latency | Expensive         |
| DSL (ADSL/VDSL)      | Uses telephone lines. Asymmetric (faster download).                          | 1–100 Mbps        | Low            | Small offices      | Affordable, widely available | Limited upload speed |
| Cable (DOCSIS)      | Uses coaxial cable. Shared medium.                                          | 10–1000 Mbps      | Moderate       | Residential       | Fast, always-on  | Shared bandwidth  |
| Fiber (FTTH/FTTB)   | Fiber-optic to the home/business. Highest speed/reliability.                | 100 Mbps – 10 Gbps | High           | Businesses, ISPs  | Highest speed, low latency | Limited availability |
| Cellular (4G/5G)   | Mobile broadband. Good for backup or remote sites.                          | 10–1000 Mbps      | Moderate       | Remote sites      | Mobile, flexible | High latency, data caps |
| Satellite          | High latency but covers remote areas.                                       | 1–100 Mbps       | Very High      | Rural areas       | Global coverage  | High latency, expensive |
| SD-WAN             | Software-defined WAN across multiple links (MPLS, internet, 4G).            | Varies           | Moderate       | Multi-site enterprises | Optimizes path selection | Complex to manage |
+----------------------+-----------------------------------------------------------------------------+---------------------+----------------+-------------------+-------------------+-------------------+

---

---
5.2 Q: Explain Routing Fundamentals
---
A:
ROUTER:
- Purpose: Connects different networks (e.g., LAN to WAN).
- Function: Forwards packets based on IP addresses (Layer 3).
- Components:
  - Interfaces: Physical/port connections (e.g., GigabitEthernet0/0).
  - Routing Table: Database of network destinations and next hops.
  - RAM: Stores routing table and ARP cache.
  - NVRAM: Stores startup configuration.
  - Flash: Stores IOS (operating system).

ROUTING TABLE:
- Contains:
  - Network Destination: Target network (e.g., 192.168.1.0/24).
  - Next Hop: Next router or gateway (e.g., 10.0.0.1).
  - Interface: Outgoing interface (e.g., GigabitEthernet0/0).
  - Metric: Cost/distance to the network (e.g., hop count, bandwidth).
  - Route Source: How the route was learned (e.g., static, OSPF, RIP).

TYPES OF ROUTING:
+-------------------+-----------------------------------------------------------------------------+-------------------+-------------------+---------------------+
| TYPE              | DESCRIPTION                                                                 | PROS              | CONS              | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+-------------------+-------------------+---------------------+
| Static Routing    | Manually configured routes.                                                  | Predictable, no overhead | Labour-intensive, no adaptability | ip route 192.168.1.0 255.255.255.0 10.0.0.1 |
| Dynamic Routing   | Routers exchange information automatically.                                | Adapts to topology changes | Overhead, complexity | OSPF, RIP, BGP     |
| Default Route     | Catch-all route for traffic not matching other routes.                      | Simple, reduces table size | Inefficient for large networks | ip route 0.0.0.0 0.0.0.0 203.0.113.1 |
+-------------------+-----------------------------------------------------------------------------+-------------------+-------------------+---------------------+

ROUTING PROTOCOLS:
+--------------+-------------------+------------------+-----------------+-------------------+---------------------+
| PROTOCOL     | TYPE              | METRIC           | CONVERGENCE      | USE CASE          | EXAMPLE             |
+--------------+-------------------+------------------+-----------------+-------------------+---------------------+
| RIP          | Distance-Vector   | Hop count        | Slow (~30 sec)   | Small networks    | router rip          |
| OSPF         | Link-State        | Cost (bandwidth) | Fast (~1 sec)    | Enterprise networks| router ospf 1      |
| EIGRP        | Advanced Distance-Vector | Composite metric | Fast | Cisco networks | router eigrp 100 |
| BGP          | Path-Vector       | Path attributes  | Slow             | Internet routing (ISP-level) | router bgp 65000 |
+--------------+-------------------+------------------+-----------------+-------------------+---------------------+

RIP (ROUTING INFORMATION PROTOCOL):
- Max hops: 15 (16 = unreachable).
- Update interval: 30 seconds.
- Version: RIPv2 (supports VLSM, authentication).

OSPF (OPEN SHORTEST PATH FIRST):
- Uses Dijkstra's algorithm to calculate shortest path.
- Areas: Divides network into areas for scalability.
- Hello packets: Maintains neighbor relationships.

BGP (BORDER GATEWAY PROTOCOL):
- Exterior Gateway Protocol (EGP): Routes between autonomous systems (AS).
- Path attributes: AS_PATH, NEXT_HOP, LOCAL_PREF, MED.
- Used by ISPs to route internet traffic.

---

---
5.3 Q: Explain 802.11 Wireless Standards
---
A:
+--------------------+----------------+---------------+--------------------+-------------------------------------------+------------------+-------------------+
| STANDARD          | NAME          | FREQUENCY      | MAX SPEED         | KEY FEATURES                          | RELEASE YEAR    | USE CASE          |
+--------------------+----------------+---------------+--------------------+-------------------------------------------+------------------+-------------------+
| 802.11a            | Wi-Fi 1        | 5 GHz         | 54 Mbps           | OFDM, less interference                    | 1999             | Legacy (rare)     |
| 802.11b            | Wi-Fi 1        | 2.4 GHz       | 11 Mbps           | Long range, but slow and congested        | 1999             | Legacy (rare)     |
| 802.11g            | Wi-Fi 3        | 2.4 GHz       | 54 Mbps           | Backward compatible with 802.11b         | 2003             | Older devices      |
| 802.11n            | Wi-Fi 4        | 2.4/5 GHz     | 600 Mbps          | MIMO (Multiple Input Multiple Output)    | 2009             | Common in homes/offices |
| 802.11ac          | Wi-Fi 5        | 5 GHz         | ~3.5 Gbps         | MU-MIMO, beamforming, wider channels      | 2013             | High-speed networks |
| 802.11ax          | Wi-Fi 6/6E     | 2.4/5/6 GHz   | ~9.6 Gbps         | OFDMA, better in dense environments       | 2019/2021        | Modern devices, crowded areas |
+--------------------+----------------+---------------+--------------------+-------------------------------------------+------------------+-------------------+

2.4 GHz VS. 5 GHz:
+-------------------+-----------------------------+-----------------------------+
| FEATURE            | 2.4 GHz                     | 5 GHz                      |
+-------------------+-----------------------------+-----------------------------+
| Range              | Longer (better penetration) | Shorter (blocked by walls) |
| Speed              | Slower (max 600 Mbps)       | Faster (max 3.5 Gbps+)     |
| Interference       | More (microwaves, Bluetooth) | Less (fewer devices use 5 GHz) |
| Channels           | 3 non-overlapping (1, 6, 11) | 23+ non-overlapping channels |
| Use Case           | Long-range, legacy devices   | High-speed, modern devices  |
+-------------------+-----------------------------+-----------------------------+

---

---
5.4 Q: Explain Wireless Security
---
A:
+---------------------------+-----------------------------------------------------------------------------+-------------------+-------------------+-----------------------------+
| SECURITY METHOD          | DESCRIPTION                                                                 | ENCRYPTION       | SECURITY LEVEL   | VULNERABILITIES             |
+---------------------------+-----------------------------------------------------------------------------+-------------------+-------------------+-----------------------------+
| Open (No Security)       | No authentication or encryption.                                              | None             | ❌ Very Weak      | Eavesdropping, unauthorized access |
| WEP                      | Wired Equivalent Privacy. OUTDATED.                                           | RC4 (40/104-bit) | ❌ Weak           | Easily cracked (IV collisions) |
| WPA                      | Wi-Fi Protected Access. DEPRECATED.                                          | TKIP (128-bit)   | ⚠️ Moderate       | Vulnerable to brute force |
| WPA2                     | CURRENT STANDARD. Uses AES.                                                 | AES-CCMP (128/256-bit) | ✅ Strong | Secure if strong password used |
| WPA3                     | LATEST STANDARD. Stronger handshake (SAE).                                  | AES-GCMP (128-bit) | ✅✅ Very Strong | Resistant to offline attacks |
| 802.1X                   | Enterprise authentication via RADIUS server.                                | Varies           | ✅✅ Very Strong | Requires RADIUS infrastructure |
+---------------------------+-----------------------------------------------------------------------------+-------------------+-------------------+-----------------------------+

ADDITIONAL WIRELESS SECURITY MEASURES:
+---------------------------+-----------------------------------------------------------------------------+-------------------+
| MEASURE                  | DESCRIPTION                                                                 | EFFECTIVENESS     |
+---------------------------+-----------------------------------------------------------------------------+-------------------+
| SSID Hiding              | Disable SSID broadcast.                                                     | ⚠️ Low (easily discovered) |
| MAC Filtering            | Allow only specific MAC addresses.                                           | ⚠️ Low (MAC spoofing) |
| Strong Passwords         | Use 12+ character passwords with mixed case, numbers, symbols.              | ✅ High          |
| Disable WPS              | WPS is vulnerable to brute force.                                             | ✅ High          |
| Firmware Updates         | Patch router/AP vulnerabilities.                                             | ✅ High          |
| VLAN Segmentation        | Isolate guest Wi-Fi from internal network.                                  | ✅ High          |
| Intrusion Detection      | Monitor for rogue APs or attacks.                                            | ✅✅ Very High   |
+---------------------------+-----------------------------------------------------------------------------+-------------------+

WIRELESS TROUBLESHOOTING:
+---------------------------+-----------------------------+-----------------------------+
| SYMPTOM                  | POSSIBLE CAUSE              | SOLUTION                    |
+---------------------------+-----------------------------+-----------------------------+
| No Connection             | Wrong SSID/password, disabled Wi-Fi | Verify SSID/password, enable Wi-Fi |
| Low Signal                | Too far from AP, obstructions | Move closer, remove obstructions |
| Interference              | Other 2.4 GHz devices        | Switch to 5 GHz, change channel |
| Slow Speeds               | Channel overlap, too many clients | Use 5 GHz, reduce channel width |
| IP Issues                 | DHCP failure, APIPA address | Check DHCP server, renew IP |
| Authentication Failures   | Wrong security mode         | Match security mode on client/AP |
| Intermittent Drops        | Interference, firmware bugs | Update firmware, change channel |
+---------------------------+-----------------------------+-----------------------------+

---

---
5.5 Q: Explain Wireless Troubleshooting
---
A:
See table in 5.4.

---

================================================================================
LU6: SECURITY, RISK MANAGEMENT & DISASTER RECOVERY
================================================================================

---
6.1 Q: Explain the CIA Triad
---
A:
+--------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| PRINCIPLE         | DEFINITION                                                                 | EXAMPLE CONTROLS   | VIOLATION EXAMPLE |
+--------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| Confidentiality   | Ensures only authorized users can access data.                          | Encryption, access controls, firewalls | Data breach, eavesdropping |
| Integrity         | Ensures data is accurate and unaltered.                                   | Hashing, digital signatures, checksums | MitM attack, data tampering |
| Availability      | Ensures systems/data are accessible when needed.                         | Redundancy, UPS, DDoS protection | DoS attack, hardware failure |
+--------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

---

---
6.2 Q: Explain Defence-in-Depth
---
A:
DEFINITION: A layered security approach where multiple controls are used to protect against threats. No single point of failure can compromise the network.

LAYERS OF DEFENCE-IN-DEPTH:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| LAYER             | CONTROLS                                                                     | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| Perimeter         | Firewalls, IDS/IPS, VPNs, DMZs                                               | Cisco ASA Firewall |
| Network           | VLANs, ACLs, segmentation, monitoring                                        | VLAN 10 (HR), VLAN 20 (Finance) |
| Endpoint          | Antivirus, host-based firewalls, MFA, patch management                     | Windows Defender    |
| Application       | Input validation, secure coding, WAFs (Web Application Firewalls)         | Cloudflare WAF      |
| Data              | Encryption (at rest and in transit), backups, access controls              | AES-256, BitLocker |
| Physical          | Locked server rooms, biometrics, surveillance, UPS                         | Keycard access      |
| Policy            | Security policies, user training, incident response plans                 | Acceptable Use Policy |
+-------------------+-----------------------------------------------------------------------------+---------------------+

---

---
6.3 Q: Explain Firewalls, IDS, and IPS
---
A:
+--------------------+-----------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| DEVICE            | FULL NAME                   | FUNCTION                                                                     | EXAMPLE             | LAYER            |
+--------------------+-----------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| Firewall          | -                           | Filters traffic based on rules (allow/deny).                                | Cisco ASA, pfSense | Network (3-4)     |
| Stateful Firewall | -                           | Tracks connection state (e.g., allows return traffic for established connections). | Palo Alto, FortiGate | Network (3-4)     |
| IDS               | Intrusion Detection System | Monitors traffic and alerts on suspicious activity.                        | Snort, Suricata    | Network (3-7)     |
| IPS               | Intrusion Prevention System | Monitors AND blocks suspicious activity.                                   | Cisco FirePOWER    | Network (3-7)     |
| Proxy Server      | -                           | Intermediary for requests; hides internal IPs and filters content.      | Squid, Blue Coat   | Application (7)   |
| DMZ               | Demilitarized Zone          | Isolates public-facing servers from internal network.                      | Web server in DMZ  | Network Architecture |
+--------------------+-----------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

FIREWALL TYPES:
+---------------------------+-----------------------------------------------------------------------------+-------------------+-------------------+
| TYPE                      | DESCRIPTION                                                                 | PROS              | CONS              |
+---------------------------+-----------------------------------------------------------------------------+-------------------+-------------------+
| Packet-Filtering          | Filters based on IP/port (stateless).                                        | Fast, simple     | No context, vulnerable to spoofing |
| Stateful                  | Tracks connection state (e.g., allows return traffic).                      | More secure, context-aware | Higher overhead |
| Application-Layer         | Inspects application data (e.g., HTTP, FTP).                                | Deep inspection, blocks attacks | Slow, complex |
| NGFW (Next-Gen Firewall)  | Combines stateful + application inspection + IPS.                         | Comprehensive protection | Expensive, resource-intensive |
+---------------------------+-----------------------------------------------------------------------------+-------------------+-------------------+

---

---
6.4 Q: Explain AAA (Authentication, Authorization, Accounting)
---
A:
+-------------------+-----------------------------+-----------------------------------------------------------------------------+---------------------+
| COMPONENT         | FULL NAME                   | DEFINITION                                                                 | EXAMPLE             |
+-------------------+-----------------------------+-----------------------------------------------------------------------------+---------------------+
| Authentication     | -                           | Verifies identity (who you are).                                           | Username/password, MFA, biometrics |
| Authorization     | -                           | Determines permissions (what you can do).                                   | Role-based access (e.g., admin vs. user) |
| Accounting        | -                           | Logs actions (what was done, when, by whom).                                | Audit logs, SIEM systems |
+-------------------+-----------------------------+-----------------------------------------------------------------------------+---------------------+

AAA PROTOCOLS:
+--------------+----------+-----------------------------------------------------------------------------+-------------------+
| PROTOCOL     | PORT     | DESCRIPTION                                                                 | USE CASE          |
+--------------+----------+-----------------------------------------------------------------------------+-------------------+
| RADIUS       | 1812/1813 | Centralized AAA for network access (e.g., Wi-Fi, VPN).                   | Enterprise Wi-Fi authentication |
| TACACS+      | 49       | Cisco's AAA protocol for device administration.                         | Router/switch admin access |
| LDAP         | 389      | Directory service for user authentication.                               | Active Directory, OpenLDAP |
| Kerberos     | 88       | Ticket-based authentication (used in Active Directory).                 | Windows domains   |
+--------------+----------+-----------------------------------------------------------------------------+-------------------+

---

---
6.5 Q: Explain Common Threats and Malware
---
A:
+--------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| THREAT                  | DESCRIPTION                                                                 | EXAMPLE             | MITIGATION        |
+--------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| Phishing                | Deceptive emails/sites tricking users into revealing credentials.          | Fake "Bank Login" email | User training, email filtering |
| Spear Phishing          | Targeted phishing (e.g., CEO fraud).                                          | Email from "CEO" asking for funds | MFA, verify requests |
| Man-in-the-Middle (MitM) | Attacker intercepts communications between two parties.                   | ARP poisoning, session hijacking | Encryption (HTTPS, VPN), ARP inspection |
| DoS/DDoS                | Floods a service with traffic to make it unavailable.                      | SYN flood, UDP flood | DDoS protection (Cloudflare), rate limiting |
| ARP Poisoning           | Sends false ARP replies to redirect traffic.                                 | Gratuitous ARP replies | Static ARP entries, ARP inspection |
| Social Engineering      | Manipulating people to bypass security controls.                            | Phone call posing as IT support | User training, verification procedures |
| Eavesdropping           | Listening to unencrypted traffic.                                           | Sniffing Wi-Fi traffic | Encryption (WPA2, HTTPS) |
| Brute Force             | Guessing passwords through repeated attempts.                                | Hydra, John the Ripper | Strong passwords, account lockout |
+--------------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

MALWARE TYPES:
+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| TYPE              | DESCRIPTION                                                                 | EXAMPLE             | MITIGATION        |
+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| Virus             | Self-replicates in files/programs. Requires user action.                   | ILOVEYOU virus    | Antivirus, user training |
| Worm              | Self-replicates without user action. Exploits vulnerabilities.               | WannaCry          | Patch management, firewalls |
| Trojan            | Disguised as legitimate software. Performs malicious actions.             | Fake "Game Crack" | Download from trusted sources |
| Ransomware        | Encrypts data and demands ransom.                                           | Locky, Ryuk       | Backups, user training |
| Spyware           | Secretly monitors user activity (keystrokes, passwords).                   | Keyloggers        | Anti-spyware, endpoint protection |
| Adware            | Displays unwanted ads. Often bundled with free software.                    | Superfish        | Ad blockers, careful installations |
| Rootkit           | Hides itself deep in the OS to avoid detection.                             | Sony CD rootkit  | Rootkit scanners, secure boot |
| Botnet            | Network of infected devices controlled by attacker.                       | Mirai (IoT botnet) | Network segmentation, IPS |
+-------------------+-----------------------------------------------------------------------------+---------------------+-------------------+

---

---
6.6 Q: Explain Device Hardening
---
A:
HARDENING CHECKLIST:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| CATEGORY          | ACTION                                                                     | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| Default Credentials | Change default usernames/passwords on all devices.                      | Router admin: admin/admin → SecurePass123! |
| Unused Services    | Disable unused ports/services (e.g., Telnet, HTTP).                         | no ip http server (Cisco) |
| Patch Management   | Apply firmware/OS patches regularly.                                         | Windows Update, apt update (Linux) |
| Logging           | Enable logging and send to a central server (SIEM).                           | Syslog, Splunk |
| Encryption        | Use encrypted management (SSH, HTTPS).                                         | Disable Telnet, enable SSH |
| Access Control     | Implement ACLs to restrict traffic.                                           | access-list 10 permit 192.168.1.0 0.0.0.255 |
| Physical Security  | Lock racks, restrict access to server rooms.                                | Keycard access, surveillance cameras |
| Disable WPS       | WPS is vulnerable to brute force attacks.                                    | Disable in router settings |
| Network Segmentation | Use VLANs to isolate sensitive systems.                                   | VLAN 10 (HR), VLAN 20 (Finance) |
| Least Privilege    | Grant only necessary permissions.                                           | User vs. Admin accounts |
+-------------------+-----------------------------------------------------------------------------+---------------------+

---

---
6.7 Q: Explain Risk Management Steps
---
A:
6-STEP RISK MANAGEMENT PROCESS:
1. IDENTIFY ASSETS AND THREATS:
   - Assets: Hardware, software, data, personnel.
   - Threats: Natural disasters, cyberattacks, human error.
   - Example: Identify servers, customer databases, and phishing attacks.

2. ASSESS VULNERABILITIES:
   - Vulnerability: Weakness that can be exploited by a threat.
   - Example: Unpatched software, weak passwords, open ports.
   - Tools: Vulnerability scanners (Nessus, OpenVAS).

3. CALCULATE RISK:
   - Risk = Likelihood × Impact
   - Likelihood: Probability of threat exploiting vulnerability (Low/Medium/High).
   - Impact: Severity of damage (Low/Medium/High).
   - Example: Unpatched server + known exploit = High Risk.

4. SELECT CONTROLS:
   +-------------------+-----------------------------------------------------------------------------+---------------------+
   | STRATEGY          | DESCRIPTION                                                                 | EXAMPLE             |
   +-------------------+-----------------------------------------------------------------------------+---------------------+
   | Avoid             | Eliminate the risk entirely.                                                 | Don't store credit card data. |
   | Mitigate          | Reduce likelihood or impact.                                                 | Install a firewall. |
   | Transfer          | Shift risk to a third party.                                                  | Cyber insurance. |
   | Accept            | Accept the risk (if cost of mitigation > risk).                              | Low-risk vulnerabilities. |
   +-------------------+-----------------------------------------------------------------------------+---------------------+

5. IMPLEMENT CONTROLS:
   - Deploy technical controls (firewalls, encryption).
   - Enforce administrative controls (policies, training).
   - Apply physical controls (locks, UPS).

6. MONITOR AND REVIEW:
   - Continuous monitoring (SIEM, logs, audits).
   - Regular reviews (quarterly risk assessments).
   - Update controls as new threats emerge.

---

---
6.8 Q: Explain Network Performance Monitoring
---
A:
KEY PERFORMANCE METRICS:
+--------------------------+-----------------------------------------------------------------------------+---------------------+---------------------+
| METRIC                  | DESCRIPTION                                                                 | ACCEPTABLE VALUES   | TOOLS              |
+--------------------------+-----------------------------------------------------------------------------+---------------------+---------------------+
| Bandwidth Utilization   | % of available bandwidth being used.                                         | < 70% (ideal)       | SNMP, NetFlow       |
| Latency                 | Time for data to travel from source to destination (ms).                      | < 100ms (LAN), < 200ms (WAN) | ping, traceroute   |
| Packet Loss             | % of packets lost in transit.                                                | < 1%                | ping, Wireshark    |
| Jitter                  | Variation in latency (ms).                                                    | < 30ms (for VoIP)   | ping, VoIP tools   |
| Uptime                  | % of time a system is operational.                                           | 99.9% (8.76 hrs downtime/year) | Nagios, PRTG |
| Throughput              | Actual data transfer rate (Mbps/Gbps).                                       | Close to bandwidth | iperf, Speedtest   |
+--------------------------+-----------------------------------------------------------------------------+---------------------+---------------------+

MONITORING TOOLS:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| TOOL              | PURPOSE                                                                     | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| SNMP              | Collects performance data from devices.                                    | snmpget, PRTG, SolarWinds |
| Syslog            | Centralized logging from network devices.                                  | syslog-ng, Splunk, ELK Stack |
| NetFlow/sFlow     | Analyzes traffic flows to identify bandwidth hogs/anomalies.                 | SolarWinds NetFlow, PRTG |
| QoS               | Prioritizes critical traffic (e.g., VoIP, video).                           | Cisco QoS, DiffServ |
| Traffic Shaping   | Limits bandwidth for certain traffic types.                               | CBQ (Class-Based Queuing) |
| Load Balancing    | Distributes traffic across multiple servers.                               | F5 BIG-IP, HAProxy |
+-------------------+-----------------------------------------------------------------------------+---------------------+

---

---
6.9 Q: Explain Disaster Recovery (DR) and Business Continuity
---
A:
KEY DR CONCEPTS:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| CONCEPT           | DEFINITION                                                                 | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| RTO (Recovery Time Objective) | Maximum tolerable downtime before recovery must complete.               | 4 hours (critical systems) |
| RPO (Recovery Point Objective) | Maximum tolerable data loss (how old a backup can be).                   | 1 hour (daily backups) |
| MTTR (Mean Time to Repair) | Average time to repair a system after failure.                          | 2 hours |
| MTBF (Mean Time Between Failures) | Average time between failures.                                       | 10,000 hours |
+-------------------+-----------------------------------------------------------------------------+---------------------+

BACKUP TYPES:
+-------------------+-----------------------------------------------------------------------------+-------------------+-------------------+---------------------+
| TYPE              | DESCRIPTION                                                                 | PROS              | CONS              | EXAMPLE             |
+-------------------+-----------------------------------------------------------------------------+-------------------+-------------------+---------------------+
| Full Backup       | Complete copy of all data.                                                 | Simple restore    | Time-consuming, storage-intensive | Weekly full backup |
| Incremental       | Backs up changes since last backup (full or incremental).                | Fast, storage-efficient | Slow restore (needs all backups) | Daily incremental |
| Differential      | Backs up changes since last full backup.                                  | Faster restore than incremental | Larger than incremental | Daily differential |
+-------------------+-----------------------------------------------------------------------------+-------------------+-------------------+---------------------+

DR PLAN ELEMENTS:
1. Risk Assessment: Identify critical systems and risks.
2. Backup Strategy: Define backup types, frequency, and storage locations.
3. Alternate Site: Hot site (fully equipped), warm site (partial), cold site (empty).
4. Roles and Responsibilities: Who does what during a disaster?
5. Testing Schedule: Test the DR plan regularly (tabletop exercises, live drills).
6. Documentation: Step-by-step recovery procedures.

BUSINESS CONTINUITY PLAN (BCP):
- Ensures critical business functions continue during/after a disaster.
- Includes:
  - Alternative work locations (e.g., remote work).
  - Communication plans (how to notify employees/customers).
  - Supplier/contacts list (emergency contacts).
  - Minimum viable operations (what must keep running?).

---

---
6.10 Q: Explain Incident Response Lifecycle
---
A:
+-------------------+-----------------------------------------------------------------------------+---------------------+
| PHASE             | DESCRIPTION                                                                 | ACTIONS             |
+-------------------+-----------------------------------------------------------------------------+---------------------+
| 1. Preparation     | Develop policies, procedures, and tools for incident response.           | Create IR plan, train team, set up SIEM |
| 2. Identification  | Detect and classify the incident.                                           | Monitor logs, alerts, user reports |
| 3. Containment     | Isolate the incident to prevent further damage.                             | Quarantine infected systems, block IPs |
| 4. Eradication     | Remove the threat (e.g., malware, attacker access).                         | Patch vulnerabilities, remove malware |
| 5. Recovery        | Restore systems to normal operation.                                      | Rebuild systems, restore from backups |
| 6. Lessons Learned | Review and improve processes based on the incident.                        | Post-incident report, update policies |
+-------------------+-----------------------------------------------------------------------------+---------------------+

EXAMPLE INCIDENT RESPONSE:
1. IDENTIFICATION: SIEM alerts on unusual traffic from a server.
2. CONTAINMENT: Disconnect the server from the network.
3. ERADICATION: Scan and remove malware, patch vulnerabilities.
4. RECOVERY: Restore from a clean backup, verify functionality.
5. LESSONS LEARNED: Update firewall rules, improve monitoring.

---

================================================================================
EXAM PREPARATION TIPS
================================================================================

---
7.1 Q: Task Words in Exam Questions
---
A:
+----------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| TASK WORD      | WHAT IT MEANS                                                                 | EXAMPLE QUESTION   | HOW TO ANSWER    |
+----------------+-----------------------------------------------------------------------------+---------------------+-------------------+
| Define         | Give a short, clear description.                                           | Define a router.    | "A router is a Layer 3 device that connects different networks and forwards packets based on IP addresses." |
| Describe       | Explain in detail how something works or appears.                         | Describe how DHCP works. | Step-by-step process (DORA). |
| Explain        | Clarify with reasons (use examples).                                         | Explain why VLANs improve security. | "VLANs isolate traffic by logical grouping, preventing unauthorized access between segments (e.g., HR and Finance)." |
| Compare        | Highlight similarities and differences.                                     | Compare TCP and UDP. | Table or bullet points. |
| Differentiate  | Focus on differences.                                                       | Differentiate between hubs and switches. | "Hubs operate at Layer 1 (dumb repeaters), while switches operate at Layer 2 (intelligent forwarding)." |
| List           | Briefly write down facts/main points.                                        | List 3 types of firewalls. | 1. Packet-filtering 2. Stateful 3. NGFW |
| Discuss        | Explain in depth with comments/opinions.                                     | Discuss the benefits of cloud computing. | Explain pros/cons, use cases, examples. |
| Analyze        | Break into parts and explain relationships.                                 | Analyze the OSI model. | Explain each layer's role and how they interact. |
| Apply          | Use knowledge to solve a problem.                                            | Apply subnetting to divide 192.168.1.0/24 into 4 subnets. | Show calculations and subnet ranges. |
| Evaluate       | Make a judgment (weigh pros/cons).                                           | Evaluate WPA2 vs. WPA3. | Compare security, compatibility, etc. |
| Demonstrate    | Show by example (use diagrams if possible).                                 | Demonstrate troubleshooting a failed network connection. | Use the 7-step methodology with a real example. |
+----------------+-----------------------------------------------------------------------------+---------------------+-------------------+

---

---
7.2 Q: Key Topics to Memorize for Closed-Book Exam
---
A:
OSI MODEL LAYERS (TOP → BOTTOM):
All People Seem To Need Data Processing
1. Application
2. Presentation
3. Session
4. Transport
5. Network
6. Data Link
7. Physical

DEVICES BY LAYER:
- Layer 7: Applications (Chrome, Outlook)
- Layer 5-7: Proxy Servers
- Layer 4: -
- Layer 3: Routers, Layer 3 Switches
- Layer 2: Switches, Bridges, NICs
- Layer 1: Hubs, Repeaters, NICs, Cables

PORT NUMBERS:
+--------------+----------+-------------------+
| PROTOCOL     | PORT     | USE               |
+--------------+----------+-------------------+
| HTTP         | 80       | Web (unencrypted) |
| HTTPS        | 443      | Web (encrypted)   |
| FTP          | 20, 21   | File Transfer     |
| SSH          | 22       | Secure Shell      |
| Telnet       | 23       | Remote Access (insecure) |
| SMTP         | 25       | Send Email        |
| DNS          | 53       | Domain Name System|
| DHCP         | 67, 68   | Dynamic IP Assignment |
| SNMP         | 161      | Network Monitoring |
| RDP          | 3389     | Remote Desktop    |
+--------------+----------+-------------------+

PRIVATE IP RANGES:
- Class A: 10.0.0.0/8 (10.0.0.0 – 10.255.255.255)
- Class B: 172.16.0.0/12 (172.16.0.0 – 172.31.255.255)
- Class C: 192.168.0.0/16 (192.168.0.0 – 192.168.255.255)

SUBNETTING QUICK REFERENCE:
+------+------------------------+------------------+
| CIDR | SUBNET MASK           | USABLE HOSTS     |
+------+------------------------+------------------+
| /24  | 255.255.255.0          | 254              |
| /25  | 255.255.255.128        | 126              |
| /26  | 255.255.255.192        | 62               |
| /27  | 255.255.255.224        | 30               |
| /28  | 255.255.255.240        | 14               |
+------+------------------------+------------------+

WIRELESS STANDARDS:
- 802.11n (Wi-Fi 4): 2.4/5 GHz, 600 Mbps, MIMO.
- 802.11ac (Wi-Fi 5): 5 GHz, ~3.5 Gbps, MU-MIMO.
- 802.11ax (Wi-Fi 6): 2.4/5/6 GHz, ~9.6 Gbps, OFDMA.

---

---
7.3 Q: Exam Strategies
---
A:
1. READ QUESTIONS CAREFULLY:
   - Identify the task word (define, explain, compare, etc.).
   - Underline key terms (e.g., "OSI Layer 3," "VLAN").

2. MANAGE TIME:
   - 100 marks in ~2 hours → ~1.2 minutes per mark.
   - Allocate time based on mark allocation (e.g., 20-mark question = ~24 minutes).

3. ANSWER STRUCTURE:
   - 1-mark questions: 1 fact/point.
   - 2-mark questions: 2 facts or 1 fact + example.
   - 5-mark questions: 5 bullet points or a short paragraph.

4. DIAGRAMS:
   - Draw diagrams where relevant (e.g., OSI model, network topologies, subnetting).
   - Label clearly and explain briefly.

5. REVIEW BEFORE SUBMITTING:
   - Check for grammar/spelling (clarity matters!).
   - Ensure all parts of the question are answered.

6. PRACTICE WITH PAST PAPERS:
   - Work through all revision activities in your prescribed textbook (West, CompTIA Network+ Guide to Networks).
   - Attempt sample questions from the assessment brief.

---

---
7.4 Q: Final Checklist Before the Exam
---
A:
- [ ] Memorize OSI layers (All People Seem To Need Data Processing).
- [ ] Know port numbers (80, 443, 22, 25, 53, 21, 20, 3389, etc.).
- [ ] Understand subnetting (practice CIDR calculations).
- [ ] Review VLANs (purpose, tagging, inter-VLAN routing).
- [ ] Study security (CIA triad, firewalls, AAA, threats).
- [ ] Practice troubleshooting (OSI model, CLI commands).
- [ ] Know cloud models (IaaS, PaaS, SaaS, deployment models).
- [ ] Understand WAN technologies (MPLS, DSL, fiber, satellite).
- [ ] Review wireless standards (802.11n/ac/ax, 2.4 vs. 5 GHz).
- [ ] Memorize private IP ranges (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16).

---
================================================================================
NOTES
================================================================================
- This document is based on the CONE5111 revision PowerPoint and assessment brief.
- Prescribed Text: West, J. (2022). CompTIA Network+: Guide to Networks, 9th Ed.
- Exam is CLOSED BOOK — memorize key concepts, port numbers, and subnet masks.
- For official study materials, always refer to your prescribed textbook and module manual.

================================================================================
END OF DOCUMENT
================================================================================
