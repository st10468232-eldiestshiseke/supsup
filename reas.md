================================================================================
CONE5111 / CONE5111p / CONE5111w / NWEG5111
COMPUTER NETWORKS 1A - ASSESSMENT BRIEF WITH ANSWERS
================================================================================
Module Code: CONE5111/CONE5111p/CONE5111w/NWEG5111
NQF Level: 5
Qualification: BCA1/DMT1/DNM1/HSU1/HSU1p/BCA1w; DNM1w

================================================================================
PART 1: SAMPLE QUESTIONS (Learning Unit 1 to Learning Unit 3) WITH ANSWERS
================================================================================

--------------------------------------------------------
LEARNING UNIT 1: Networking Fundamentals, OSI Model, Topologies, Safety, Troubleshooting
--------------------------------------------------------

---
Q1: A topology describes how the parts of a whole work together. Using suitable examples, differentiate between a physical topology and a logical topology.

ANSWER:
- Physical Topology: The ACTUAL layout of devices, cables, and connections (e.g., STAR topology with a central switch, BUS with a single backbone cable).
- Logical Topology: The PATH data takes through the network (e.g., ETHERNET uses a BUS logical topology even if physically wired as a star, because data is broadcast to all devices on the segment).

---
Q2: Discuss the three ways resources can be shared if all computers in a P2P network are running a Windows OS.

ANSWER:
1. File Sharing: Enable shared folders via Windows File Sharing (SMB/CIFS).
2. Printer Sharing: Share a printer connected to one PC with others on the network.
3. Internet Connection Sharing (ICS): One PC with internet access can share its connection with others.

---
Q3: Describe the advantages of a client/server network relative to a peer-to-peer network.

ANSWER:
+-------------------+------------------+------------------+
| ADVANTAGE         | CLIENT/SERVER    | P2P              |
+-------------------+------------------+------------------+
| Centralized Mgmt | YES (Admin       | NO (Each user    |
|                   | controls access) | manages own)    |
| Scalability       | YES (Handles     | NO (Performance  |
|                   | many users)      | degrades)        |
| Security          | YES (Centralized)| NO (No central   |
|                   | backups)         | security)        |
| Performance       | YES (Dedicated   | NO (Slower; user |
|                   | servers)         | PCs share load)  |
| Data Backup       | YES (Centralized)| NO (Each user    |
|                   | management)      | backs up own)    |
+-------------------+------------------+------------------+

---
Q4: Explain how the Application Layer facilitates communication between software applications and lower-layer network services.

ANSWER:
- The Application Layer (Layer 7) provides NETWORK SERVICES to end-user applications (e.g., HTTP for web browsers, SMTP for email).
- It TRANSLATES data between the application and the network (e.g., encodes a web request into HTTP format).
- Uses PROTOCOLS (HTTP, FTP, DNS) to INTERFACE with lower layers (e.g., passes data to the Transport Layer as segments).
- Manages DIALOGUE CONTROL (who transmits when), DATA SYNTAX (format), and SYNCHRONIZATION (timing).

---
Q5: Explain how the data unit accepted from the Transport layer is transformed into a packet.

ANSWER:
1. The TRANSPORT LAYER passes a SEGMENT (with source/destination PORTS, sequence numbers, checksum) to the NETWORK LAYER.
2. The NETWORK LAYER adds an IP HEADER (source/destination IP ADDRESSES, TTL, protocol ID, etc.).
3. The result is a PACKET (or IP DATAGRAM), which includes:
   - HEADER (IP metadata)
   - PAYLOAD (the Transport Layer segment)

---
Q6: Describe the communication mishap referred to as partial communication.

ANSWER:
- Partial communication occurs when ONLY PART OF A MESSAGE is transmitted/received due to:
  * Network interruptions (e.g., cable disconnects mid-transmission).
  * Buffer overflows (receiver's buffer fills up, dropping later data).
  * Errors in transmission (corrupted packets discarded).
- RESULT: Incomplete or corrupted data at the destination (e.g., a half-downloaded file).

---
Q7: Explain the different signal types corresponding to the different transmission media.

ANSWER:
+------------+------------------+-----------------------------+
| MEDIUM     | SIGNAL TYPE      | EXAMPLE                      |
+------------+------------------+-----------------------------+
| Copper     | Electrical       | Voltage changes (Ethernet)  |
| Fiber-Optic| Light pulses     | LED/laser pulses             |
| Wireless   | Radio Frequency  | Electromagnetic waves (Wi-Fi)|
+------------+------------------+-----------------------------+

---
Q8: Describe the three common levels of fire suppression systems: a. Building level. b. Room level. c. Rack level.

ANSWER:
a. BUILDING LEVEL:
   - Fire sprinklers (water-based) or gas suppression systems (e.g., FM-200) covering the entire building.
   - Activated by smoke/heat detectors.

b. ROOM LEVEL:
   - Dedicated suppression (e.g., clean agent systems like Novec 1230) in server rooms/data centers.
   - Avoids water damage to equipment.

c. RACK LEVEL:
   - Localized suppression (e.g., in-rack fire suppression canisters) targeting individual server racks.
   - Fast response to contain fires before they spread.

---
Q9: Discuss four (4) general OSHA guidelines that should be followed when using power tools or other hand tools in the workplace.

ANSWER:
1. INSPECT TOOLS BEFORE USE: Check for damage (e.g., frayed cords, cracked casings).
2. USE PERSONAL PROTECTIVE EQUIPMENT (PPE): Gloves, safety goggles, ear protection.
3. ENSURE PROPER GROUNDING: For electric tools, use 3-prong plugs and GFCIs (Ground Fault Circuit Interrupters).
4. FOLLOW MANUFACTURER INSTRUCTIONS: Operate tools within rated voltage/load limits and use correct accessories.

---
Q10: Discuss the negative effects that static electricity (ESD) can have on electronic components.

ANSWER:
- IMMEDIATE DAMAGE:
  * Permanently destroys sensitive components (e.g., CPUs, RAM, motherboards).
  * Causes catastrophic failure (e.g., burned circuits).
- LATENT DEFECTS:
  * Weakens components without immediate failure (e.g., reduced lifespan, intermittent errors).
- DATA CORRUPTION:
  * Alters stored data in memory or storage devices.
- SYSTEM INSTABILITY:
  * Causes random crashes, errors, or malfunctions over time.

---
Q11 & Q12: Describe each of the seven steps of the troubleshooting methodology using examples. In your answer, explain using the seven steps how to troubleshoot a failed network connection.

ANSWER:
+-------+-------------------------------+--------------------------------------------------+
| STEP  | DESCRIPTION                   | EXAMPLE (Failed Network Connection)             |
+-------+-------------------------------+--------------------------------------------------+
| 1     | Identify the Problem           | User reports: "I can't access the internet."     |
| 2     | Establish a Theory             | Loose cable, faulty NIC, DHCP issue, router down |
| 3     | Test the Theory                | Check link lights, try different cable/port,    |
|       |                               | run ipconfig /all (no IP -> DHCP issue)         |
| 4     | Plan Action                    | Replace cable, restart NIC, or renew DHCP lease   |
| 5     | Implement Solution             | Replace the faulty Ethernet cable               |
| 6     | Verify Functionality          | Test internet access, run ping 8.8.8.8          |
| 7     | Document Findings              | Log: "User X's cable was damaged; replaced with  |
|       |                               | Cat6 cable. Issue resolved."                    |
+-------+-------------------------------+--------------------------------------------------+

--------------------------------------------------------
LEARNING UNIT 2: Cabling, Standards, Documentation, Performance, Multiplexing, Troubleshooting Tools
--------------------------------------------------------

---
Q13: Discuss the three (3) basic types of cable installations allowed by structured cabling standards.

ANSWER:
1. HORIZONTAL CABLING:
   - Runs from workstation outlets to the telecommunications closet (max 90m for copper).
   - Includes patch cables (max 10m total for horizontal + patch).

2. BACKBONE CABLING:
   - Connects telecommunications closets, equipment rooms, and entrance facilities.
   - Uses fiber-optic or high-grade copper (e.g., Cat6a).

3. WORK AREA CABLING:
   - From the wall jack to the end device (e.g., PC, phone).
   - Includes patch cords and adapters.

---
Q14: Discuss five (5) cable installation tips that will help prevent Physical layer failures.

ANSWER:
1. AVOID EXCEEDING BEND RADIUS:
   - Copper: Max 4x cable diameter (e.g., Cat6: ~10cm).
   - Fiber: Single-mode: ~5cm; Multimode: ~3cm.

2. SEPARATE FROM POWER CABLES: Maintain minimum distance (e.g., 30cm for parallel runs) to avoid EMI/RFI.

3. USE CABLE MANAGEMENT: Velcro ties (not zip ties) to avoid crushing cables.

4. LABEL CABLES CLEARLY: Use consistent naming conventions (e.g., Floor1-Switch1-Port24).

5. TEST AFTER INSTALLATION: Use a cable certifier to verify continuity, crosstalk, attenuation.

---
Q15: Explain the importance of network documentation and how it makes managing and troubleshooting a network more efficient. In your answer, describe the components of the network documentation.

ANSWER:
IMPORTANCE:
- Faster Troubleshooting: Quickly locate issues (e.g., trace a cable path).
- Change Management: Plan upgrades without disrupting services.
- Compliance: Meet audit/regulatory requirements (e.g., ISO 27001).
- Knowledge Sharing: New admins can understand the network quickly.

COMPONENTS OF NETWORK DOCUMENTATION:
1. Network Diagrams: Logical (IPs, subnets, VLANs) and Physical (cable routes, rack layouts).
2. IP Address Scheme: Subnet allocations, DHCP ranges, reserved IPs.
3. Device Configurations: Backup configs for routers, switches, firewalls.
4. Cabling Layouts: Patch panel ports, cable types (Cat6, fiber), lengths.
5. Policies & Procedures: Password policies, change management workflows.
6. Inventory List: Hardware/software versions, serial numbers, warranties.

---
Q16: Describe a wiring schematic using an example.

ANSWER:
- A wiring schematic is a DIAGRAM showing how devices are PHYSICALLY CONNECTED via cables.
- EXAMPLE:
  [Patch Panel Port 1] ---(Cat6)--- [Switch Port 1]
  [Patch Panel Port 2] ---(Cat6)--- [Switch Port 2]
  * Labels: Each connection is tagged (e.g., PP-1 -> SW1-Gi1/0/1).
  * Purpose: Helps technicians TRACE CABLES and VERIFY CONNECTIONS.

---
Q17: Discuss the importance of establishing a naming convention when labeling devices. In your answer, outline any five (5) naming convention tips.

ANSWER:
IMPORTANCE:
- Consistency: Avoids confusion (e.g., Switch1 vs SW-01-Floor2).
- Scalability: Easy to add new devices.
- Troubleshooting: Quickly identify device location/purpose.

5 NAMING CONVENTION TIPS:
1. Use a Standard Format: [Location]-[DeviceType]-[Number] (e.g., L2-SW-03 = Level 2, Switch 3).
2. Include Meaningful Info: DC1-RTR-01 (Data Center 1, Router 1).
3. Avoid Special Characters: Stick to letters, numbers, hyphens (e.g., no spaces or !@#).
4. Keep It Short: Max 15-20 characters (e.g., HR-VLAN-10).
5. Document the Convention: Maintain a legend (e.g., L2 = Level 2, SW = Switch).

---
Q18: Discuss the purpose and structure of the following business documents in the context of a network design solution project:
a. RFP (Request for Proposal) b. MOU (Memorandum of Understanding) c. SOW (Statement of Work)
d. SLA (Service-Level Agreement) e. MSA (Master Service Agreement) f. MLA (Master License Agreement)

ANSWER:
+------+--------------------------------+----------------------------------------------+
| DOC  | PURPOSE                        | STRUCTURE                                  |
+------+--------------------------------+----------------------------------------------+
| a. RFP| Solicit bids from vendors       | 1. Project Overview (goals, scope)           |
|      | for a project.                 | 2. Requirements (technical, timeline)       |
|      |                                | 3. Evaluation Criteria (cost, experience)   |
|      |                                | 4. Submission Deadline                     |
+------+--------------------------------+----------------------------------------------+
| b. MOU| Outline a NON-BINDING           | 1. Parties Involved                          |
|      | agreement between parties.      | 2. Purpose (e.g., collaboration)             |
|      |                                | 3. Responsibilities                         |
|      |                                | 4. Duration                                  |
+------+--------------------------------+----------------------------------------------+
| c. SOW| Define DELIVERABLES, TIMELINE,  | 1. Scope of Work                              |
|      | and TASKS for a project.        | 2. Milestones                                |
|      |                                | 3. Acceptance Criteria                       |
|      |                                | 4. Payment Terms                             |
+------+--------------------------------+----------------------------------------------+
| d. SLA| Define PERFORMANCE METRICS      | 1. Service Description                       |
|      | (e.g., uptime, response time).   | 2. Availability (e.g., 99.9% uptime)          |
|      |                                | 3. Penalties for non-compliance              |
+------+--------------------------------+----------------------------------------------+
| e. MSA| OVERARCHING CONTRACT for        | 1. Terms & Conditions                        |
|      | long-term services.             | 2. Confidentiality                           |
|      |                                | 3. Liability                                 |
|      |                                | 4. Termination Clauses                       |
+------+--------------------------------+----------------------------------------------+
| f. MLA| SOFTWARE LICENSING TERMS for    | 1. Licensed Software                         |
|      | an organization.                | 2. Usage Rights                              |
|      |                                | 3. Restrictions                              |
|      |                                | 4. Support Terms                             |
+------+--------------------------------+----------------------------------------------+

---
Q19: Explain why managing change while maintaining a network's efficiency and availability requires good planning.

ANSWER:
- MINIMIZES DOWNTIME: Changes are scheduled during maintenance windows.
- REDUCES ERRORS: Tested in a lab before deployment.
- ROLLBACK PLAN: If the change fails, revert to the previous state quickly.
- DOCUMENTATION: Updates to network diagrams/configs ensure future troubleshooting is easier.
- STAKEHOLDER COMMUNICATION: Notifies users of expected outages or new features.

---
Q20: Explain three (3) factors that can degrade network performance using examples.

ANSWER:
1. BANDWIDTH CONGESTION:
   - Example: 100 users streaming 4K video on a 100 Mbps link -> buffering, slow speeds.

2. LATENCY:
   - Example: A gamer in South Africa connecting to a US server -> high ping (200ms+) -> lag.

3. PACKET LOSS:
   - Example: Faulty switch port drops 10% of packets -> VoIP calls break up.

---
Q21: Discuss the two (2) common sources of noise in the context of transmission flaws.

ANSWER:
1. ELECTROMAGNETIC INTERFERENCE (EMI):
   - Caused by power lines, motors, fluorescent lights.
   - Affects copper cables (e.g., Cat6 near a power cable).

2. RADIO FREQUENCY INTERFERENCE (RFI):
   - Caused by radio transmitters, Wi-Fi, microwave ovens.
   - Affects wireless signals (e.g., 2.4 GHz Wi-Fi vs. microwave).

---
Q22: Using an example, discuss why latency causes problems. In your answer, also explain what packet jitter is and how it affects streaming communication, such as video and audio transmissions.

ANSWER:
- LATENCY PROBLEM EXAMPLE:
  In VIDEO CALLS, high latency (e.g., 500ms) causes DELAYED RESPONSES, making conversations unnatural.

- PACKET JITTER:
  * Definition: VARIATION IN PACKET ARRIVAL TIME (e.g., packets arrive at 10ms, 50ms, 20ms intervals).
  * Effect on Streaming:
    - BUFFER UNDERFLOWS: Video/audio STUTTERS OR FREEZES (e.g., Netflix buffering).
    - POOR SYNCHRONIZATION: Lip-sync issues in VoIP (e.g., Zoom calls).

---
Q23: Explain how multiple signals are carried using subchannels.

ANSWER:
- MULTIPLEXING divides a SINGLE TRANSMISSION MEDIUM into MULTIPLE SUBCHANNELS.
- Each subchannel carries a SEPARATE SIGNAL (e.g., phone call, data stream).
- EXAMPLES:
  * TDM (Time-Division Multiplexing): Each signal gets a TIME SLOT (e.g., 24 phone calls on a T1 line).
  * FDM (Frequency-Division Multiplexing): Each signal uses a DIFFERENT FREQUENCY (e.g., radio stations).
  * WDM (Wavelength-Division Multiplexing): Each signal uses a DIFFERENT LIGHT WAVELENGTH (fiber-optic).

---
Q24: Discuss the three common types of multiplexing used on copper lines.

ANSWER:
1. TIME-DIVISION MULTIPLEXING (TDM): Divides bandwidth into FIXED TIME SLOTS (e.g., E1/T1 lines).
2. FREQUENCY-DIVISION MULTIPLEXING (FDM): Uses DIFFERENT FREQUENCY BANDS (e.g., DSL combines voice + data on a phone line).
3. STATISTICAL TDM (STDM): DYNAMICALLY ALLOCATES TIME SLOTS based on demand (more efficient than TDM).

---
Q25: Discuss the three types of multiplexing technologies used with fiber-optic cable.

ANSWER:
1. WAVELENGTH-DIVISION MULTIPLEXING (WDM): Multiple LIGHT WAVELENGTHS (colors) on a single fiber.
2. DENSE WDM (DWDM): 80+ CHANNELS, each on a different wavelength (e.g., 100G+ speeds).
3. COARSE WDM (CWDM): FEWER CHANNELS (up to 18), CHEAPER than DWDM (e.g., 10G per channel).

---
Q26: Using any two characteristics, differentiate between two (2) categories of twisted pair cable.

ANSWER:
COMPARISON: Cat5e vs. Cat6
+-------------------+----------+----------+
| CHARACTERISTIC    | Cat5e    | Cat6     |
+-------------------+----------+----------+
| Max Speed         | 1 Gbps   | 10 Gbps  |
|                   | (100m)   | (55m)    |
| Bandwidth         | 100 MHz  | 250 MHz  |
| Crosstalk Resist. | Lower    | Higher   |
| Cost              | Cheaper  | Expensive|
+-------------------+----------+----------+

---
Q27: Describe the similarities and differences between STP and UTP under each of the following topics: a. Throughput b. Cost c. Connector d. Noise immunity e. Size and scalability

ANSWER:
+-------------------+----------------------------+----------------------------+------------------+
| TOPIC             | STP                        | UTP                        | SIMILARITY       |
+-------------------+----------------------------+----------------------------+------------------+
| Throughput        | Higher (less interference)| Lower (susceptible to EMI) | Both support     |
|                   |                            |                            | 10/100/1000 Mbps  |
| Cost              | More expensive (shielding) | Cheaper                    | -                |
| Connector         | RJ-45 (grounded connectors)| RJ-45                      | Both use RJ-45   |
| Noise Immunity    | HIGH (blocks EMI/RFI)      | LOW                        | -                |
| Size & Scalability| Bulkier (shielding)        | Thinner, more flexible    | Both scale well  |
|                   |                            |                            | for LANs         |
+-------------------+----------------------------+----------------------------+------------------+

---
Q28: Explain why closely following proper termination techniques is critical. In your answer, also identify the two TIA/EIA standards for terminating twisted pair cable.

ANSWER:
WHY PROPER TERMINATION MATTERS:
- PREVENTS SIGNAL REFLECTION: Poor terminations cause IMPEDANCE MISMATCHES -> DATA ERRORS.
- ENSURES RELIABILITY: Loose connections lead to INTERMITTENT FAILURES.
- MEETS PERFORMANCE STANDARDS: Required for CERTIFICATION (e.g., Cat6 must meet 1 Gbps).

TIA/EIA STANDARDS:
1. TIA/EIA-568-A: Older standard (now OBSOLETE).
2. TIA/EIA-568-B: Current standard (defines WIRING PINOUTS for RJ-45).

---
Q29: Explain what a crossover cable is and discuss why they are now largely obsolete, except when needed to support older devices.

ANSWER:
- CROSSOVER CABLE:
  * Swaps transmit/receive pairs (e.g., Pin 1 -> Pin 3, Pin 2 -> Pin 6).
  * Used to connect SIMILAR DEVICES (e.g., switch-to-switch, PC-to-PC).

- WHY OBSOLETE?
  * AUTO-MDI/MDIX: Modern ETHERNET PORTS (Gigabit+) AUTOMATICALLY DETECT and configure the connection.
  * NO MANUAL SWAPPING NEEDED -> STRAIGHT-THROUGH CABLES work for all connections.

---
Q30: Discuss the benefits fiber-optic cable provides over copper cabling.

ANSWER:
+-------------------+------------------+------------------+
| BENEFIT           | FIBER-OPTIC      | COPPER           |
+-------------------+------------------+------------------+
| Bandwidth         | HIGHER (100 Gbps+)| LOWER (10 Gbps max)|
| Distance          | LONGER (80km+)   | SHORTER (100m max)|
| EMI/RFI Immunity  | UNAFFECTED       | SUSCEPTIBLE       |
| Security          | HARDER TO TAP    | EASIER TO INTERCEPT|
| Weight & Size     | LIGHTER, THINNER | HEAVIER, BULKIER |
| Cost              | MORE EXPENSIVE   | CHEAPER           |
+-------------------+------------------+------------------+

---
Q31: Discuss any two (2) common problems that are unique to fiber cable.

ANSWER:
1. FIBER BENDS & BREAKS:
   - MACROBENDS (sharp bends > 10x cable diameter) cause SIGNAL LOSS.
   - MICROBENDS (tiny kinks) degrade performance.

2. DIRTY/IMPROPER CONNECTORS:
   - DUST OR SCRATCHES on connector ends -> LIGHT REFLECTION/LOSS.
   - Requires CLEANING WITH ALCOHOL WIPES and INSPECTION WITH A MICROSCOPE.

---
Q32: Discuss the basic steps to take to start troubleshooting a network connection problem.

ANSWER:
1. CHECK PHYSICAL LAYER:
   - Verify CABLES ARE PLUGGED IN (link lights on NIC/switch).
   - Try a DIFFERENT CABLE/PORT.

2. VERIFY IP CONFIGURATION:
   - Run ipconfig /all (Windows) or ifconfig (Linux) -> Check for VALID IP, SUBNET MASK, GATEWAY.

3. TEST CONNECTIVITY:
   - ping 127.0.0.1 (loopback test).
   - ping [gateway IP] (e.g., ping 192.168.1.1).

4. CHECK DNS:
   - ping 8.8.8.8 (tests internet) vs. ping google.com (tests DNS).

5. INSPECT FIREWALL/SECURITY:
   - Disable WINDOWS FIREWALL temporarily to test.

---
Q33: Explain the differences between continuity testers and performance testers. Outline some of the tasks a performance tester can be used to measure.

ANSWER:
+-------------------+----------------------------+----------------------------+
| FEATURE           | CONTINUITY TESTER         | PERFORMANCE TESTER         |
+-------------------+----------------------------+----------------------------+
| Purpose           | Checks if cable is INTact  | CERTIFIES cable performance|
|                   | (no breaks)                | (speed, noise)              |
| What It Tests     | Open circuits, short       | Attenuation, crosstalk,    |
|                   | circuits, miswires         | delay, bandwidth            |
| Complexity        | Simple, cheap ($20)        | Advanced, expensive        |
|                   |                            | (Fluke Networks ~$10K)     |
| Use Case          | Quick checks during        | FINAL CERTIFICATION for     |
|                   | installation               | Cat6/6a/fiber              |
+-------------------+----------------------------+----------------------------+

PERFORMANCE TESTER TASKS:
- WIREMAP: Verify PAIR ASSIGNMENTS (e.g., T568A vs. T568B).
- LENGTH MEASUREMENT: Ensure cable doesn't exceed MAX LENGTH (e.g., 100m for Ethernet).
- ATTENUATION: Measure SIGNAL LOSS over distance.
- NEAR-END CROSSTALK (NEXT): Check for INTERFERENCE BETWEEN PAIRS.
- RETURN LOSS: Test for SIGNAL REFLECTIONS (impedance mismatches).

--------------------------------------------------------
LEARNING UNIT 3: IP Addressing, DNS, Encryption, Remote Access
--------------------------------------------------------

---
Q34: Explain the two types of IP addresses that can be assigned to a device.

ANSWER:
1. PUBLIC IP ADDRESS:
   - Globally unique, assigned by IANA/ISP.
   - Routable on the internet (e.g., 203.0.113.45).

2. PRIVATE IP ADDRESS:
   - Non-routable, used in private networks (e.g., 192.168.1.10).
   - Defined in RFC 1918:
     * 10.0.0.0/8
     * 172.16.0.0/12
     * 192.168.0.0/16

---
Q35: Describe the three classes of IP addresses used for LANs in traditional IP addressing.

ANSWER:
+-------+-------------------------------+---------------------+--------------------------+
| CLASS | RANGE                         | DEFAULT SUBNET MASK | USE CASE                |
+-------+-------------------------------+---------------------+--------------------------+
| A     | 1.0.0.0 - 126.255.255.255     | 255.0.0.0 (/8)       | Large networks          |
|       |                               |                     | (e.g., governments)     |
| B     | 128.0.0.0 - 191.255.255.255   | 255.255.0.0 (/16)    | Medium networks         |
|       |                               |                     | (e.g., universities)    |
| C     | 192.0.0.0 - 223.255.255.255   | 255.255.255.0 (/24)  | Small networks          |
|       |                               |                     | (e.g., home/office LANs)|
+-------+-------------------------------+---------------------+--------------------------+

---
Q36: Discuss the concepts of classless and classful addressing using examples. In your answer, explain the relevance of CIDR in classless addressing.

ANSWER:
- CLASSFUL ADDRESSING:
  * Fixed class boundaries (A, B, C).
  * Wasteful: If a Class A network (/8) only needs 10,000 IPs, the rest are unused.
  * Example: 10.0.0.0/8 (all 16.7M IPs assigned to one org).

- CLASSLESS ADDRESSING (CIDR):
  * Variable-Length Subnet Masking (VLSM): Subnets can be ANY SIZE (e.g., /26, /27).
  * Efficient: Allocates ONLY NEEDED IPs (e.g., /24 for 254 hosts).
  * Example: 192.168.1.0/26 (62 hosts) instead of wasting a full /24.

- RELEVANCE OF CIDR:
  * Eliminates class boundaries -> BETTER IP UTILIZATION.
  * Enables ROUTE AGGREGATION (e.g., 192.168.0.0/24 + 192.168.1.0/24 = 192.168.0.0/23).

---
Q37: Describe how dynamic IP address assignment using DHCP works.

ANSWER:
DHCP (Dynamic Host Configuration Protocol) PROCESS:
1. DHCP DISCOVER:
   - Client BROADCASTS DHCP Discover (source IP: 0.0.0.0, dest: 255.255.255.255).

2. DHCP OFFER:
   - Server RESPONDS with DHCP Offer (proposed IP, subnet mask, lease time, gateway, DNS).

3. DHCP REQUEST:
   - Client REQUESTS the offered IP via DHCP Request.

4. DHCP ACKNOWLEDGE (ACK):
   - Server CONFIRMS the lease with DHCP ACK.

- LEASE TIME: IP is TEMPORARILY ASSIGNED (e.g., 24 hours). Client must RENEW before expiry.

---
Q38: Discuss the reasons why an administrator would choose to implement address translation.

ANSWER:
1. CONSERVES PUBLIC IPS:
   - NAT (Network Address Translation) allows THOUSANDS OF PRIVATE IPs to share ONE PUBLIC IP.

2. SECURITY:
   - HIDES INTERNAL IPs from the internet (harder to attack).

3. SIMPLIFIES NETWORKING:
   - PRIVATE IPs can be reused across organizations (e.g., 192.168.1.0/24).

4. ENABLES INTERNET ACCESS:
   - Devices with PRIVATE IPs can ACCESS THE INTERNET via NAT.

---
Q39: Using examples, describe the three types of IP addresses supported by IPv6: a. Unicast b. Multicast c. Anycast

ANSWER:
+-------+-------------------------------+-------------+--------------------------+
| TYPE  | DESCRIPTION                   | EXAMPLE     | USE CASE                |
+-------+-------------------------------+-------------+--------------------------+
| Unicast| ONE-TO-ONE communication      | 2001:db8::1 | Normal host             |
|       |                               |             | communication           |
| Multicast| ONE-TO-MANY communication     | FF02::1     | Video streaming (IPTV)  |
| Anycast| ONE-TO-NEAREST communication   | 2001:db8::1 | DNS root servers        |
|       |                               |             | (client connects to     |
|       |                               |             | closest server)         |
+-------+-------------------------------+-------------+--------------------------+

---
Q40: Discuss the four (4) common types of DNS servers: a. Primary DNS server. b. Secondary DNS server. c. Caching DNS server. d. Forwarding DNS server.

ANSWER:
+-------+--------------------------------+----------------------------------+
| TYPE  | ROLE                           | EXAMPLE                          |
+-------+--------------------------------+----------------------------------+
| a. Primary DNS | AUTHORITATIVE for a zone;    | ns1.example.com (hosts          |
|       | stores MASTER COPY of DNS       | example.com zone file)          |
|       | records                        |                                  |
| b. Secondary DNS| BACKUP for primary; gets     | ns2.example.com (slave to        |
|       | ZONE TRANSFERS (AXFR/IXFR)      | ns1.example.com)                |
|       | from primary                   |                                  |
| c. Caching DNS | STORES DNS QUERY RESULTS to   | Your ISP's DNS server            |
|       | speed up future requests       | (e.g., 8.8.8.8)                  |
| d. Forwarding DNS| FORWARDS QUERIES to another  | A corporate DNS server that      |
|       | DNS server (e.g., upstream ISP)| forwards to Google DNS (8.8.8.8) |
+-------+--------------------------------+----------------------------------+

---
Q41: Using examples, describe the two types of DNS requests: a. Recursive lookups b. Iterative lookups

ANSWER:
+-------+--------------------------------+----------------------------------+
| TYPE  | DESCRIPTION                    | EXAMPLE                          |
+-------+--------------------------------+----------------------------------+
| a. Recursive | DNS server RESOLVES THE FULL   | Client asks A record for          |
|       | QUERY and returns the FINAL     | google.com -> DNS server queries |
|       | ANSWER to the client            | root -> TLD -> authoritative ->   |
|       |                                | returns IP to client             |
| b. Iterative| DNS server PROVIDES THE BEST   | Client asks A record for          |
|       | REFERRAL it has (client must    | google.com -> Root DNS says      |
|       | query next server)              | "Ask .com TLD server" -> Client  |
|       |                                | asks TLD -> TLD says "Ask         |
|       |                                | Google's authoritative server"   |
+-------+--------------------------------+----------------------------------+

---
Q42: Explain the concept of the Time to Live (TTL) field associated with DNS zones and records. In your answer, also explain how the TTL prevents stale records from accumulating in the cache on clients and servers.

ANSWER:
- TTL (Time to Live):
  * Specifies HOW LONG (in seconds) a DNS record can be CACHED before it must be REFRESHED.
  * Example: A record with TTL=3600 (1 hour) must be re-queried after 1 hour.

- PREVENTS STALE RECORDS:
  * If a DNS RECORD CHANGES (e.g., example.com moves to a new IP), the OLD RECORD EXPIRES after TTL.
  * Forces CLIENTS/SERVERS TO FETCH THE LATEST RECORD instead of using outdated cached data.

---
Q43: Discuss the three benchmarks that are used to evaluate encryption methods. Use a suitable example for each benchmark in your discussion. a. Confidentiality b. Integrity c. Availability

ANSWER:
+---------------+-------------------------------+----------------------------------+
| BENCHMARK     | DEFINITION                     | EXAMPLE                          |
+---------------+-------------------------------+----------------------------------+
| Confidentiality| Ensures ONLY AUTHORIZED        | AES-256 encryption (used in      |
|               | PARTIES can read data         | HTTPS, VPNs)                     |
| Integrity     | Ensures data HASN'T BEEN       | SHA-256 hash (used in digital    |
|               | ALTERED                       | signatures, SSL certificates)    |
| Availability   | Ensures data is ACCESSIBLE     | DDoS protection (e.g.,           |
|               | WHEN NEEDED                    | Cloudflare) prevents attacks     |
|               |                               | from taking down a website       |
+---------------+-------------------------------+----------------------------------+

---
Q44: Discuss the five steps by which IPsec creates a secure connection.

ANSWER:
1. SECURITY ASSOCIATION (SA) ESTABLISHMENT:
   - Negotiates ENCRYPTION KEYS, ALGORITHMS (e.g., AES, SHA).

2. IKE (Internet Key Exchange) PHASE 1:
   - AUTHENTICATES peers (using PRE-SHARED KEYS or CERTIFICATES).

3. IKE PHASE 2:
   - Establishes SAs FOR DATA ENCRYPTION (e.g., ESP for encryption, AH for authentication).

4. DATA ENCAPSULATION:
   - ENCAPSULATES IP packets in IPSEC HEADERS (tunnel mode or transport mode).

5. SECURE DATA TRANSMISSION:
   - ENCRYPTS/DECRYPTS data in transit (e.g., VPN traffic).

---
Q45: Discuss HTTPS and its use of SSL/TLS to establish a secure HTTP connection.

ANSWER:
- HTTPS = HTTP OVER SSL/TLS.

- HOW SSL/TLS WORKS:
  1. HANDSHAKE: Client and server NEGOTIATE encryption (e.g., TLS 1.3).
  2. AUTHENTICATION: Server presents a DIGITAL CERTIFICATE (verified by CA like DigiCert).
  3. KEY EXCHANGE: SYMMETRIC SESSION KEY is generated (e.g., via ECDHE).
  4. ENCRYPTED COMMUNICATION: All HTTP traffic is ENCRYPTED (e.g., AES-256).

- RESULT: CONFIDENTIALITY, INTEGRITY, AND AUTHENTICATION for web traffic.

---
Q46: Explain a handshake protocol and discuss the three steps in an SSL/TLS handshake.

ANSWER:
- HANDSHAKE PROTOCOL: A NEGOTIATION PROCESS to establish a SECURE CONNECTION (e.g., TLS handshake).

- 3 KEY STEPS:
  1. CLIENT HELLO:
     - Client sends SUPPORTED CIPHER SUITES (e.g., TLS_AES_256_GCM_SHA384).

  2. SERVER HELLO + CERTIFICATE:
     - Server selects a CIPHER SUITE and sends its DIGITAL CERTIFICATE (proving identity).

  3. KEY EXCHANGE & AUTHENTICATION:
     - Client VERIFIES THE CERTIFICATE (checks CA signature).
     - PRE-MASTER SECRET is generated (used to derive SYMMETRIC KEYS).

---
Q47: Explain why a user might need to connect to a remote network for services.

ANSWER:
1. ACCESS REMOTE RESOURCES: Company files/servers (e.g., file shares, databases).
2. WORK FROM ANYWHERE: Remote employees access internal apps (e.g., SAP, email).
3. CENTRALIZED MANAGEMENT: IT admins manage servers, switches, firewalls remotely.
4. CLOUD SERVICES: Access AWS, Azure, or private cloud resources.
5. COLLABORATION: Video conferencing, VoIP (e.g., Microsoft Teams, Zoom).

---
Q48: Explain the purpose of a RAS (Remote Access Server). In your answer, also describe the two (2) types of remote access servers.

ANSWER:
- PURPOSE OF RAS:
  * Provides SECURE REMOTE ACCESS to a PRIVATE NETWORK (e.g., corporate LAN).
  * AUTHENTICATES USERS and ENCAPSULATES TRAFFIC (e.g., via PPP, VPN).

- TWO TYPES OF RAS:
  1. DIAL-UP RAS:
     - Uses TELEPHONE LINES (e.g., PSTN, ISDN).
     - SLOW (max 56 Kbps for analog).

  2. VPN RAS:
     - Uses INTERNET + VPN PROTOCOLS (e.g., PPTP, L2TP, OpenVPN).
     - FASTER (depends on internet speed).

---
Q49: Discuss the VPN (Virtual Private Network) as one of the common types of remote access methods.

ANSWER:
- WHAT IS A VPN?
  * Creates a SECURE TUNNEL over a PUBLIC NETWORK (e.g., internet).

- HOW IT WORKS:
  1. ENCRYPTION: Uses IPSEC, SSL/TLS, OR WIREGUARD to encrypt traffic.
  2. AUTHENTICATION: Verifies users via USERNAME/PASSWORD, CERTIFICATES, or 2FA.
  3. TUNNELING: Encapsulates data in IP PACKETS (e.g., PPTP, L2TP, OpenVPN).

- BENEFITS:
  * SECURITY: Protects against EAVESDROPPING (e.g., on public Wi-Fi).
  * PRIVACY: Hides REAL IP ADDRESS (useful for bypassing geo-restrictions).
  * ACCESS CONTROL: Only AUTHORIZED USERS can connect.

---
Q50: List and describe the steps used to authenticate with SSH using keys.

ANSWER:
SSH KEY AUTHENTICATION STEPS:
1. GENERATE KEY PAIR (on client):
   - Run ssh-keygen -t rsa -> Creates PRIVATE KEY (id_rsa) and PUBLIC KEY (id_rsa.pub).

2. COPY PUBLIC KEY TO SERVER:
   - Use ssh-copy-id user@server -> Adds public key to ~/.ssh/authorized_keys on the server.

3. CLIENT INITIATES CONNECTION:
   - Run ssh user@server -> Server checks authorized_keys.

4. SERVER VERIFIES KEY:
   - If the CLIENT'S PRIVATE KEY MATCHES THE PUBLIC KEY, access is granted.

5. OPTIONAL PASSPHRASE:
   - If the PRIVATE KEY IS ENCRYPTED, the user must enter the PASSPHRASE.

================================================================================
PART B: SCENARIO-BASED QUESTIONS (LU1-LU3) WITH ANSWERS
================================================================================

--------------------------------------------------------
LEARNING UNIT 1: OSI Model Troubleshooting
--------------------------------------------------------

---
Q51: A computer is unable to access the network. When you check the LED lights near the computer's network port, you discover the lights are not lit. Which layer of the OSI model are you using to troubleshoot this problem? At which two layers does the network adapter work?

ANSWER:
- TROUBLESHOOTING LAYER: PHYSICAL LAYER (Layer 1) (no link lights = NO PHYSICAL CONNECTION).
- NETWORK ADAPTER LAYERS:
  * PHYSICAL LAYER (Layer 1): Transmits/receives ELECTRICAL SIGNALS.
  * DATA LINK LAYER (Layer 2): Handles MAC ADDRESSING and FRAMING.

---
Q52: A user complains that their computer cannot access email, although the computer can access websites. At which layer of the OSI model should you begin troubleshooting this problem and why?

ANSWER:
- START AT APPLICATION LAYER (Layer 7).
- WHY?
  * Email (e.g., SMTP/IMAP) and web (HTTP/HTTPS) use DIFFERENT APPLICATION PROTOCOLS.
  * If WEB WORKS BUT EMAIL FAILS, the issue is likely with the EMAIL CLIENT/SERVER (e.g., misconfigured SMTP settings, firewall blocking port 25/587).

---
Q53: While troubleshooting a problem, you realize the problem is caused by a complex series of issues that will affect a large number of users, and even to test your theory as to the cause, that process won't even solve the problem. What should you do next in the troubleshooting process?

ANSWER:
- ESCALATE THE PROBLEM:
  * DOCUMENT FINDINGS (symptoms, theories tested).
  * NOTIFY MANAGEMENT or HIGHER-LEVEL SUPPORT (e.g., network team, vendor).
  * CREATE A CHANGE REQUEST if a SYSTEM-WIDE FIX is needed (e.g., firmware update, hardware replacement).

--------------------------------------------------------
LEARNING UNIT 2: Cabling & Performance
--------------------------------------------------------

---
Q54: Suppose you're assisting with a cable installation using fiber-optic cabling that will support Gigabit Ethernet. You're approved to install segments up to 4000 m in length. What mode of fiber cable are you using?

ANSWER:
- SINGLE-MODE FIBER (SMF).
- WHY?
  * Single-mode supports LONG DISTANCES (up to 80km+ for 1 Gbps).
  * Multimode is limited to ~550m for Gigabit Ethernet.

--------------------------------------------------------
LEARNING UNIT 3: IP Addressing, DNS, Protocols, Troubleshooting
--------------------------------------------------------

---
Q55: You are the network manager for a computer training center that allows students to bring their own laptops to class for learning and taking notes. Students need access to the Internet, so you have configured your network's DHCP server to issue IP addresses automatically. Which DHCP option should you modify to make sure you are not wasting addresses used by students who have left for the day?

ANSWER:
- DHCP OPTION 51: IP ADDRESS LEASE TIME.
- SOLUTION: Set a SHORT LEASE TIME (e.g., 1-2 hours) so IPs are RELEASED QUICKLY when students disconnect.

---
Q56: You have decided to use SNAT and PAT on your small office network. At minimum, how many IP addresses must you obtain from your ISP for all five clients in your office to be able to access servers on the Internet?

ANSWER:
- 1 PUBLIC IP ADDRESS.
- WHY?
  * PAT (Port Address Translation) allows MULTIPLE CLIENTS to share ONE PUBLIC IP by using DIFFERENT PORT NUMBERS.

---
Q57: You issue a transmission from your workstation to the following socket on your LAN: 10.1.1.145:53. Assuming your network uses standard port designations, what application layer protocol handles your transmission?

ANSWER:
- DNS (Domain Name System).
- WHY?
  * PORT 53 is the STANDARD PORT for DNS (both TCP for zone transfers and UDP for queries).

---
Q58: Suppose you want to change the default port for RDP as a security precaution. What port does RDP use by default, and from what range of numbers should you select a private port number?

ANSWER:
- DEFAULT RDP PORT: 3389.
- PRIVATE PORT RANGE: 49152-65535 (IANA dynamic/private ports).

---
Q59: While troubleshooting a network connection problem for a coworker, you discover the computer is querying a nonexistent DNS server. What command-line utility can you use to assign the correct DNS server IP address?

ANSWER:
- WINDOWS: netsh interface ipv4 set dnsserver name="Ethernet" static 8.8.8.8 primary
- ALTERNATIVE: Use GUI (Control Panel > Network > IPv4 Properties).
- LINUX: nmcli con mod "Ethernet" ipv4.dns "8.8.8.8" or edit /etc/resolv.conf

---
Q60: When running a scan on your computer, you find that a session has been established with a host at the address 208.85.40.44:443. Which application layer protocol is in use for this session? What command-line utility might you use to determine the domain name of the other computer?

ANSWER:
- PROTOCOL: HTTPS (port 443 = HTTP SECURE).
- COMMAND TO FIND DOMAIN NAME:
  * nslookup 208.85.40.44 (Windows/Linux).
  * dig -x 208.85.40.44 (Linux reverse DNS lookup).

---
Q61: When surfing online, you get some strange data on an apparently secure website, and you realize you need to check the legitimacy of the site. What kind of organization issues digital certificates for websites?

ANSWER:
- CERTIFICATE AUTHORITY (CA).
- EXAMPLES:
  * DigiCert, Let's Encrypt, Sectigo, GoDaddy, VeriSign.

---
Q62: You're getting a duplicate IP address error on your computer and need to figure out which other device on your network is using the IP address 192.168.1.56. What command will show you which MAC address is mapped to that IP address?

ANSWER:
- WINDOWS: arp -a | findstr "192.168.1.56"
- LINUX/MACOS: arp -n | grep 192.168.1.56
- ALTERNATIVE: ping 192.168.1.56 (populates ARP cache) -> then arp -a

================================================================================
EXAM PREP TIPS
================================================================================

1. FOCUS ON LU1-LU3 (60% of the exam questions).
2. UNDERSTAND OSI MODEL TROUBLESHOOTING (Q51-Q53 are HIGH-YIELD).
3. MEMORIZE PORT NUMBERS: 22 (SSH), 25 (SMTP), 53 (DNS), 80 (HTTP), 443 (HTTPS), 3389 (RDP).
4. PRACTICE SUBNETTING & CIDR (Q35-Q37, Q56).
5. REVIEW DHCP & NAT (Q37, Q55, Q56).
6. KNOW CABLE STANDARDS (Q13, Q26-Q30, Q54).
7. UNDERSTAND TROUBLESHOOTING STEPS (Q11, Q12, Q32, Q53).

================================================================================
NOTE: This document was generated by Mistral AI. For official study materials,
always refer to your prescribed textbook and module manual.
================================================================================
