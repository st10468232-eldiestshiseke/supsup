 Learning Unit 4: Network Architecture and Network Segmentation

1. Explain the importance of abstraction levels in network architecture design.
Answer:
Abstraction levels (e.g., OSI model layers) simplify network design by:

Hiding complexity: Higher layers (e.g., Application) don’t need to understand lower layers (e.g., Physical).
Modularity: Changes in one layer (e.g., switching from copper to fiber) don’t affect others.
Interoperability: Standardized interfaces (e.g., TCP/IP) enable multi-vendor compatibility.
Easier troubleshooting: Isolate issues to specific layers (e.g., a physical layer cable fault vs. an application layer protocol error).
Exam Tip: Link to OSI model or TCP/IP stack as examples of abstraction.

2. Compare traditional networking with virtualised networking infrastructures.
Answer:


  
    
      Aspect
      Traditional Networking
      Virtualised Networking
    
  
  
    
      Hardware
      Dedicated physical devices (e.g., routers)
      Software-defined (e.g., virtual switches, NFV)
    
    
      Scalability
      Limited by hardware capacity
      Elastic (scale up/down on demand)
    
    
      Configuration
      Manual, static
      Automated, dynamic (e.g., SDN controllers)
    
    
      Cost
      High CapEx (hardware purchases)
      Lower CapEx, higher OpEx (subscriptions)
    
    
      Flexibility
      Rigid (hardware changes required)
      Agile (e.g., spin up a VLAN in minutes)
    
    
      Example
      Cisco routers, physical firewalls
      VMware NSX, AWS VPC, Cisco ACI
    
  



Exam Tip: Highlight SDN (Software-Defined Networking) as a key enabler of virtualisation.

3. Evaluate the advantages and risks associated with cloud computing adoption.
Answer:
Advantages:

Cost-efficiency: Pay-as-you-go (no upfront hardware costs).
Scalability: Auto-scaling (e.g., AWS Auto Scaling for web apps).
Accessibility: Global access via the internet (e.g., SaaS like Google Workspace).
Disaster Recovery: Built-in redundancy (e.g., multi-region backups in Azure).
Maintenance: Provider handles updates/patching (e.g., managed databases like AWS RDS).
Risks:

Security: Shared responsibility model (e.g., misconfigured S3 buckets).
Compliance: Data sovereignty issues (e.g., GDPR for EU customer data).
Vendor Lock-in: Difficulty migrating between providers (e.g., AWS-specific services).
Downtime: Dependency on provider uptime (e.g., AWS outages in 2021).
Latency: Performance varies by location (e.g., cloud-hosted apps for remote users).
Exam Tip: Use real-world examples (e.g., AWS outage 2021, Capital One breach 2019).

4. Explain the purpose and benefits of network segmentation.
Answer:
Purpose: Divide a network into smaller, isolated segments to:

Improve Security: Limit lateral movement of threats (e.g., contain a breach to one segment).
Enhance Performance: Reduce broadcast traffic (e.g., separate VoIP and data VLANs).
Simplify Management: Apply policies per segment (e.g., QoS for video traffic).
Compliance: Meet regulatory requirements (e.g., PCI-DSS for payment systems).
Benefits:

Reduced Attack Surface: Isolate critical systems (e.g., HR database in a separate VLAN).
Traffic Optimization: Prioritize critical apps (e.g., VoIP over file transfers).
Easier Troubleshooting: Localize issues to specific segments.
Exam Tip: Link to VLANs, subnetting, and micro-segmentation as implementation methods.

5. Apply subnetting calculations to create efficient network addressing plans.
Answer:
Scenario: Design a subnet for a company with 3 departments (50, 30, 20 hosts).
Steps:

Determine Host Requirements:

Largest department: 50 hosts → 64 hosts (2⁶) → /26 (255.255.255.192).

Calculate Subnets:

Network Increment: 256 - 192 = 64.
Subnet 1 (HR): 192.168.1.0/26 (Usable: 192.168.1.1–192.168.1.62).
Subnet 2 (Finance): 192.168.1.64/26 (Usable: 192.168.1.65–192.168.1.126).
Subnet 3 (IT): 192.168.1.128/26 (Usable: 192.168.1.129–192.168.1.190).

Exam Tip: Practice CIDR notation and subnet mask conversions (e.g., /26 = 255.255.255.192).

🌐 Learning Unit 5: Wide Area Networks (WANs) and Wireless Transmissions

1. Explain the purpose and characteristics of Wide Area Networks (WANs).
Answer:
Purpose: Connect geographically dispersed networks (e.g., HQ to branches, ISPs to customers) for long-distance communication.
Characteristics:

Large Geographic Coverage: Spans cities, countries, or continents.
Diverse Technologies: Uses MPLS, leased lines, broadband, VPNs, or satellite.
Shared or Dedicated: Public (e.g., internet) or private (e.g., MPLS).
Lower Speed/Higher Latency: Compared to LANs (e.g., 100 Mbps vs. 1 Gbps).
Ownership: Typically leased from service providers (e.g., Telkom, AT&T).
Protocols: Uses WAN-specific protocols (e.g., PPP, HDLC, BGP).
Exam Tip: Contrast with LANs (e.g., WANs cover larger areas, LANs are faster and private).

2. Compare MPLS, leased lines, broadband, and VPN technologies for WAN connectivity.
Answer:


  
    
      Technology
      Pros
      Cons
      Use Case
    
  
  
    
      MPLS
      High performance, QoS, low latency
      Expensive, complex setup
      Enterprises (e.g., banks, healthcare)
    
    
      Leased Lines
      Guaranteed bandwidth, secure
      Very expensive, rigid
      Critical links (e.g., stock exchanges)
    
    
      Broadband
      Affordable, widely available
      No QoS, shared bandwidth
      SMBs, remote workers
    
    
      VPN
      Cost-effective, flexible
      Security depends on encryption, latency
      Remote access, branch connectivity
    
  



Exam Tip: MPLS is best for high-performance, private networks, while VPN is best for cost-effective, secure remote access.

3. Analyse the role of routers and routing tables in WAN communication.
Answer:
Routers:

Forward packets between networks (e.g., LAN to WAN).
Functions:

Packet Forwarding: Use routing tables to determine the next hop.
NAT: Translate private IPs to public IPs (e.g., for internet access).
QoS: Prioritize traffic (e.g., VoIP over email).
Security: Filter traffic with ACLs or firewalls.

Routing Tables:

Components:

Destination Network: IP range (e.g., 192.168.1.0/24).
Next Hop: Next router’s IP (e.g., 10.0.0.1).
Metric: Cost/path preference (e.g., OSPF cost, BGP path attributes).
Interface: Outgoing port (e.g., GigabitEthernet0/1).

Types:

Static Routes: Manually configured (e.g., ip route 192.168.1.0 255.255.255.0 10.0.0.1).
Dynamic Routes: Learned via protocols (e.g., OSPF, BGP).

Exam Tip: Know how to read a routing table and explain static vs. dynamic routing.

4. Explain the principles of wireless transmission in WLAN environments.
Answer:
Principles:

Radio Frequency (RF) Signals:

Modulation: Encode data onto RF waves (e.g., OFDM for 802.11ac/ax).
Frequency Bands:

2.4 GHz: Longer range, more interference (e.g., microwaves, Bluetooth).
5 GHz: Shorter range, less interference, higher speeds.
6 GHz: New for Wi-Fi 6E, less congestion.


Spread Spectrum:

DSSS: Direct Sequence Spread Spectrum (used in 802.11b).
OFDM: Orthogonal Frequency-Division Multiplexing (used in 802.11a/g/n/ac/ax).

Channel Width:

20 MHz: Standard (e.g., 802.11n).
40/80/160 MHz: Wider channels for higher speeds (e.g., 802.11ac/ax).

MIMO (Multiple Input Multiple Output):

Uses multiple antennas to increase throughput and reduce interference.
SU-MIMO: Single-user (e.g., 802.11n).
MU-MIMO: Multi-user (e.g., 802.11ac/ax).

CSMA/CA:

Carrier Sense Multiple Access with Collision Avoidance: Devices listen before transmitting to avoid collisions (unlike Ethernet’s CSMA/CD).

Exam Tip: Link to 802.11 standards (e.g., 802.11ax uses OFDMA + MU-MIMO).

5. Design a WAN solution for a retail organisation with multiple branches nationwide.
Answer:
Requirements:

50 branches, 20–50 employees each.
Centralized inventory/POS system at HQ.
Internet access for all branches.
Budget: Moderate.
Solution:

Connectivity:

Primary: MPLS for HQ-branch links (guaranteed QoS for POS traffic).
Backup: Broadband + IPSec VPN for each branch (cost-effective redundancy).

Hardware:

HQ: Dual ISPs (fiber + broadband), Cisco ASR 1000 routers.
Branches: Cisco ISR 4000 routers with VPN capability.

Routing:

OSPF: For dynamic routing between HQ and branches.
Default Route: Branches send internet traffic via local broadband.

Security:

Firewall: Palo Alto at HQ, Cisco Firepower at branches.
VPN: IPSec tunnels for all branch-HQ traffic.

QoS:

Prioritize POS traffic (TCP 443) over email/web.

Exam Tip: Justify MPLS for critical traffic and VPN for cost savings.

🔒 Learning Unit 6: Risk Management, Network Security, Performance and Recovery

1. Explain the importance of confidentiality, integrity, and availability (CIA) in network security.
Answer:
The CIA Triad is the cornerstone of network security:


  
    
      Principle
      Definition
      Example
    
  
  
    
      Confidentiality
      Ensure data is only accessible to authorized users
      Encryption (AES, TLS), access controls (RBAC)
    
    
      Integrity
      Ensure data is accurate and unaltered
      Hashing (SHA-256), digital signatures
    
    
      Availability
      Ensure systems/data are accessible when needed
      Redundancy (load balancers), backups
    
  



Why It Matters:

Compliance: Regulations like GDPR, HIPAA, PCI-DSS require CIA.
Trust: Customers/partners expect secure, reliable systems.
Business Continuity: Downtime = lost revenue (e.g., Amazon loses $66,240/minute during outages).
Exam Tip: Use real-world examples (e.g., TLS for confidentiality, checksums for integrity).

2. Analyse how defence-in-depth strategies reduce organisational security risks.
Answer:
Defence-in-Depth (DiD) uses multiple security layers to protect against threats. If one layer fails, others remain.
Layers:

Physical: Biometric locks, surveillance, mantraps.
Network: Firewalls, IDS/IPS, VLANs, micro-segmentation.
Endpoint: Antivirus, EDR, DLP.
Application: WAF, input validation, API gateways.
Data: Encryption (at rest/in transit), tokenization, masking.
User: MFA, security awareness training, least privilege.
How It Reduces Risk:

Attacker Must Bypass All Layers: E.g., a hacker bypasses the firewall but is stopped by MFA.
Redundancy: If IDS fails, the WAF may still block the attack.
Compliance: Meets NIST, ISO 27001 requirements.
Exam Tip: Draw a diagram of DiD layers if the exam allows visuals.

3. Compare the functions of firewalls, IDS, IPS, and proxy servers in protecting networks.
Answer:


  
    
      Device
      Function
      How It Works
      Example
    
  
  
    
      Firewall
      Filters traffic between networks
      Inspects packets against ACLs/rules
      Cisco ASA, Palo Alto VM-Series
    
    
      IDS
      Monitors for suspicious activity
      Passively analyzes traffic, alerts on threats
      Snort, Suricata
    
    
      IPS
      Blocks suspicious traffic
      Actively drops/resets malicious packets
      Cisco Firepower, Fortinet FortiGate
    
    
      Proxy Server
      Mediates client-server requests
      Acts as an intermediary, hides client IPs
      Squid, Blue Coat
    
  



Key Differences:

Firewall vs. IDS/IPS: Firewall prevents known threats, IDS detects threats, IPS prevents threats.
Proxy vs. Firewall: Proxy works at application layer, firewall at network layer.
Exam Tip: Know where each device is placed (e.g., firewall at network perimeter, proxy between users and internet).

4. Evaluate the role of AAA in controlling access to organisational resources.
Answer:
AAA (Authentication, Authorization, Accounting) is a framework for access control:


  
    
      Component
      Definition
      Example
    
  
  
    
      Authentication
      Verify identity (who are you?)
      Passwords, MFA, biometrics, 802.1X
    
    
      Authorization
      Determine permissions (what can you do?)
      RBAC (Role-Based Access Control), ACLs
    
    
      Accounting
      Track activity (what did you do?)
      RADIUS/TACACS+ logs, SIEM tools
    
  



How AAA Works:

User Requests Access (e.g., logs into VPN).
Authentication: User provides credentials (e.g., username + password + MFA).
Authorization: System checks permissions (e.g., HR can access payroll, but not R&D).
Accounting: Logs actions (e.g., "User X accessed Server Y at 10:00 AM").
Protocols:

RADIUS: UDP-based, widely used for network access (e.g., Wi-Fi, VPN).
TACACS+: TCP-based, Cisco proprietary, encrypts entire packet.
Diameter: Successor to RADIUS, used in 4G/5G networks.
Exam Tip: Link to 802.1X for network access control.

5. Design a disaster recovery and incident response plan for a cloud-based organisation.
Answer:
Scenario: SaaS startup (100 employees, 10,000 customers) using AWS.
Disaster Recovery (DR) Plan:

Objectives:

RTO: < 1 hour for web app, < 4 hours for database.
RPO: < 15 minutes for database, < 1 hour for files.

Strategies:

Web App (EC2): Multi-AZ Deployment (RTO: 5 min, RPO: 1 min).
Database (RDS): Multi-AZ + Read Replicas (RTO: 10 min, RPO: 5 min).
File Storage (S3): Cross-Region Replication (RTO: 1 hour, RPO: 1 hour).
Lambda Functions: Multi-Region Deployment (RTO: 15 min, RPO: 5 min).

Testing:

Backup Verification: Weekly.
Failover Test: Quarterly.
Full DR Drill: Annually.

Incident Response (IR) Plan:

Detection:

AWS GuardDuty + SIEM (Splunk) for alerts.
Thresholds: > 5% error rate or unusual API calls.

Containment:

Isolate affected systems (e.g., Security Groups: Deny All).
Revoke compromised IAM credentials.

Eradication:

Remove malware (e.g., CrowdStrike scan).
Patch vulnerabilities (e.g., AWS Systems Manager Patch Manager).

Recovery:

Restore from backups (e.g., RDS snapshot, S3 versioning).

Lessons Learned:

Post-Incident Review (PIR) with 5 Whys analysis.
Update IR Plan and train staff.

Exam Tip: Focus on cloud-native tools (e.g., AWS Multi-AZ, GuardDuty, Splunk).

📌 Exam Tips for All Units

Understand Key Concepts: Know definitions of abstraction, virtualization, CIA triad, DiD, QoS, etc.
Compare and Contrast: Be ready to compare technologies (e.g., MPLS vs. VPN, IaaS vs. PaaS).
Practical Applications: Practice subnetting, WAN design, DR/IR planning.
Real-World Examples: Use case studies (e.g., WannaCry, AWS outages, GDPR fines).
Diagrams: If allowed, draw network diagrams (e.g., VLANs, WAN topologies, DiD layers).





3













