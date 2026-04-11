# Network & Infrastructure Security

---

## 🌐 Ports and Protocols (OBJ 4.5)

- **Port** — Logical communication endpoint on a computer or server
- **Inbound Port** — A server listening for a connection from a client
- **Outbound Port** — A client calling out to a server

| Port Range | Category |
|---|---|
| 0 – 1023 | Well-Known Ports (assigned by IANA) |
| 1024 – 49,151 | Registered Ports (proprietary protocols) |
| 49,152 – 65,535 | Dynamic and Private Ports (any application) |

### Common Ports to Know

| Port | Protocol | Service |
|---|---|---|
| 21 | FTP | File Transfer |
| 22 | SSH | Secure Shell |
| 23 | Telnet | Unencrypted remote access |
| 25 | SMTP | Email sending |
| 53 | DNS | Domain Name System |
| 80 | HTTP | Web traffic |
| 443 | HTTPS | Encrypted web traffic |
| 3306 | MySQL | Database |
| 3389 | RDP | Remote Desktop Protocol |

---

## 🔥 Firewalls (OBJ 3.2)

Safeguards networks by monitoring and controlling traffic based on predefined security rules.

| Firewall Type | Description |
|---|---|
| **Packet-Filtering** | Checks packet headers based on IP addresses and port numbers |
| **Stateful** | Monitors inbound and outbound connections and state |
| **Proxy (Circuit Level)** | Operates at Layer 5 of OSI model (SOCKS firewall) |
| **Application Level (Layer 7)** | Conducts proxy functions for each type of application |
| **Kernel Proxy (5th Gen)** | Minimal performance impact while inspecting all layers |
| **NGFW (Next-Gen)** | More aware of applications and their behaviors |
| **UTM** | Multiple security functions in a single appliance |
| **WAF (Web Application Firewall)** | Focused on inspecting HTTP traffic |

- **Screened Subnet (Dual-homed Host)** — Security barrier between external and internal networks
- **Access Control List (ACL)** — Rule set that permits or denies traffic on a specific interface

---

## 🚨 IDS and IPS (OBJ 3.2)

- **IDS** — Logs and alerts only
- **IPS** — Logs, alerts, AND takes action to block threats

| Type | Description |
|---|---|
| **NIDS** | Network Intrusion Detection System — monitors traffic in/out of a network |
| **HIDS** | Host-Based IDS — looks at suspicious traffic to/from a single endpoint |
| **WIDS** | Wireless IDS — detects DoS attempts on a wireless network |
| **Signature-based IDS** | Recognizes attacks based on previously identified attack signatures |
| **Anomaly/Behavioral-based IDS** | Compares traffic to a normal baseline to detect threats |

---

## 🖧 Network Appliances (OBJ 3.2)

| Appliance | Description |
|---|---|
| **Load Balancer** | Distributes network traffic across multiple servers for high availability |
| **Proxy Server** | Intermediary between client and server for caching, filtering, and login management |
| **Network Sensor** | Monitors, detects, and analyzes traffic for unusual activities |
| **Jump Server/Box** | Dedicated gateway for admins to securely access different security zones |

---

## 🔌 Port Security (OBJ 3.2)

- Restricts which devices can connect to a specific port based on MAC address
- **CAM Table (Content Addressable Memory)** — Stores info about MAC addresses available on switch ports
- **Persistent (Sticky) MAC Learning** — Switch automatically learns and associates MAC addresses with interfaces
- **802.1x Protocol** — Standardized framework for port-based authentication on wired and wireless networks

### 802.1x Authentication Variants
| Protocol | Description |
|---|---|
| **RADIUS** | Cross-platform AAA services for network users |
| **TACACS+** | Cisco-proprietary, separates AAA functions for more granular control |
| **EAP-MD5** | Uses simple passwords and challenge handshake |
| **EAP-TLS** | Uses PKI with digital certificates on both client and server |
| **EAP-TTLS** | Requires certificate on server only, not client |
| **EAP-FAST** | Uses protected access credential instead of certificate (Cisco) |
| **PEAP** | Uses server certificates and Microsoft Active Directory for authentication |
| **LEAP** | Only works on Cisco-based devices |

---

## 🔐 VPNs and Secure Communications (OBJ 3.2)

- **VPN** — Extends a private network over a public one for secure data transmission

| VPN Type | Description |
|---|---|
| **Site-to-site** | Connects remote sites over public internet |
| **Client-to-site** | Connects individual devices to org headquarters |
| **Full Tunnel** | All traffic encrypted to HQ — more secure |
| **Split Tunnel** | Divides traffic between org and internet — better performance |
| **Clientless VPN** | Browser-based VPN without needing client software |

### VPN Protocols
- **IPSec** — Protocol suite for secure IP communication through authentication and encryption
  - **Transport Mode** — Uses original IP header; ideal for client-to-site VPNs
  - **Tunneling Mode** — Adds an extra header; used for site-to-site VPNs
  - **Authentication Header (AH)** — Provides data integrity and origin authentication
  - **Encapsulating Security Payload (ESP)** — Provides authentication, integrity, and data encryption
- **DTLS (Datagram Transport Layer Security)** — UDP-based version of TLS for faster operations
- **SD-WAN** — Virtualized approach to managing WAN connections efficiently
- **SASE (Secure Access Service Edge)** — Consolidates networking and security into a single cloud-native service

---

## 🏗️ Security Architecture (OBJ 3.1)

### On-Premise vs. Cloud

| Factor | On-Premise | Cloud |
|---|---|---|
| Control | High | Shared (Responsibility Matrix) |
| Cost | High upfront | Ongoing subscription |
| Scalability | Limited | High |
| Maintenance | Your responsibility | Shared or provider's |

- **Hybrid Solutions** — Combines on-premise, private cloud, and public cloud

### Cloud Security Threats
- Shared physical server vulnerabilities, inadequate virtual environment security
- Inadequate user access management, lack of up-to-date security measures
- Single points of failure, weak authentication and encryption, unclear policies
- **Data Remnants** — Residual data left after deletion processes

### Virtualization and Containerization
- **Type 1 Hypervisor** — Runs directly on host hardware (Hyper-V, VMware ESXi) — faster and more efficient
- **Type 2 Hypervisor** — Operates within a standard OS (VirtualBox, VMware Workstation)
- **Containerization** — Lightweight alternative to full virtualization; containers share the OS kernel

#### Virtualization Vulnerabilities
- **VM Escape** — Attacker breaks out of an isolated virtual machine
- **Privilege Elevation** — User gains ability to run functions at a higher level
- **Live VM Migration** — Security risks when a VM moves between physical hosts
- **Resource Reuse** — Risks from reusing memory or processing power

### Software-Defined Networking (SDN)
- Separates the network into three planes:
  - **Data/Forwarding Plane** — Handles packets and makes decisions based on protocols
  - **Control Plane** — The brain of the network; determines where traffic is sent (centralized)
  - **Application Plane** — Where all network applications interacting with the SDN controller reside

### Infrastructure as Code (IaC)
- IT infrastructure defined in code files that can be versioned, tested, and audited
- **Idempotence** — An idempotent script sets up identical infrastructure every time it runs
- **Snowflake System** — A unique config that must be eliminated for consistency
- Benefits: Speed, consistency, scalability, cost savings, auditability
- Risks: Learning curve, complexity, security risks from exposed sensitive data

### Network Separation
- **Physical Separation/Air Gapping** — Isolation by removing all direct and indirect connections
- **Logical Separation** — Uses firewalls, VLANs, and other devices to control traffic based on rules

---

## 📡 Wireless Security (OBJ 4.1)

### Access Point Placement
- Place access points near the center of the facility to minimize unauthorized access risk
- Place access points in higher locations
- **Extended Service Set (ESS)** — Multiple APs working together for unified coverage
- **Adjacent Channel Interference** — When channels for adjacent APs don't have enough space between them
- **Site Survey** — Process of planning and designing a wireless network
- **Heat Map** — Graphical representation of wireless coverage and signal strength

### Wireless Encryption Standards

| Standard | Year | Notes |
|---|---|---|
| **WEP** | 1999 | Outdated, considered insecure |
| **WPA** | 2003 | Improved over WEP, but insecure due to TKIP weaknesses |
| **WPA2** | — | Improved data protection, addresses WPA weaknesses |
| **WPA3** | — | Latest version; uses AES, SAE, Enhanced Open, management protection frames |

- **SAE (Simultaneous Authentication of Equals)** — Guards against offline dictionary attacks
- **Enhanced Open/OWE** — Advancement in security for open authentication networks
- **GCMP (Galois Counter Mode Protocol)** — 128-bit AES for personal, 192-bit AES for enterprise (WPA3)
- **Management Protection Frames** — Required to protect against key recovery attacks

---

## 🏭 ICS and SCADA (OBJ 3.1 & 4.1)

- **ICS (Industrial Control Systems)** — Used to monitor and control industrial processes
- **DCS (Distributed Control Systems)** — Controls production systems within a single location
- **PLCs (Programmable Logic Controllers)** — Controls specific processes like assembly lines
- **SCADA** — Monitors and controls geographically dispersed industrial processes
- Securing ICS/SCADA: Strong access control, regular patching, firewalls and IDS, regular security audits, employee training

---

## 📱 IoT Security (OBJ 3.2 & 4.1)

- **Hub** — Central point connecting all IoT devices
- **Smart Devices** — Everyday objects with computing capabilities and internet connectivity
- **Sensors** — Detect changes in the environment
- Common risks: Weak default passwords, poorly configured network services

---

## 🧱 Infrastructure Considerations (OBJ 3.2)

- **Security Zone** — Distinct segment within a network created by logically isolating using a firewall
- **Screened Subnet** — Hosts public-facing services and protects the internal network
- **Attack Surface** — All points where unauthorized users can enter or extract data
- **Inline Device** — Sits in the network traffic path; can control or block traffic (firewall, router, IPS)
- **Fail-Open** — Allows all traffic in the event of a device failure
- **Fail-Close** — Denies all traffic in the event of a device failure

### Selecting Infrastructure Controls
- **Least Privilege** — Grant only necessary access rights to reduce attack surface
- **Defense in Depth** — Multiple layers of security to mitigate threats even if one fails
- **Risk-based Approach** — Prioritize controls based on potential risks
- **Lifecycle Management** — Regularly review, update, and retire controls
- **Open Design Principle** — Transparency and accountability through rigorous testing
