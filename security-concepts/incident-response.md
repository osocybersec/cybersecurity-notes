# Incident Response & Forensics

---

## 🚨 Incident Response Process (OBJ 4.8)

- **Incident** — Act of violating an explicit or implied security policy
- 3 goals: Minimize impact, reduce response time, hasten recovery

### 7 Phases of the CompTIA Incident Response Cycle

| Phase | Description |
|---|---|
| **1. Preparation** | Strengthening systems to resist attacks |
| **2. Detection** | Identifies security incidents |
| **3. Analysis** | Thorough examination and evaluation of the incident |
| **4. Containment** | Limits the incident's impact by securing data and protecting operations |
| **5. Eradication** | Removes malicious activity from the system or network |
| **6. Recovery** | Restores systems and services to their secure state |
| **7. Post-Incident Activity / Lessons Learned** | Root cause analysis, lessons learned, after-action report |

---

## 🎯 Threat Hunting (OBJ 4.8)

- Cybersecurity method for finding hidden threats not caught by regular security monitoring
- **Advisories and Bulletins** — Published by vendors and researchers when new TTPs and vulnerabilities are discovered
- **Intelligence Fusion and Threat Data** — Uses SIEM and analysis platforms to spot concerns in logs

---

## 🔎 Root Cause Analysis (OBJ 4.8)

- Systematic process to identify the initial source of the incident and how to prevent recurrence
- Primary purpose is **not to assign blame** but to understand exactly what happened

---

## 🏋️ Incident Response Training and Testing (OBJ 4.8)

- **Training** — Ensures staff understand processes and priorities for incident response
- **Testing** — Practical exercise of incident response procedures
- **Tabletop Exercise (TTX)** — Simulates incidents within a controlled framework without deploying actual resources

---

## 🔬 Digital Forensics (OBJ 4.8)

- **Digital Forensics** — Investigating and analyzing digital devices and data to uncover evidence for legal purposes

### Forensic Phases

| Phase | Description |
|---|---|
| **Identification** | Secure the scene, prevent evidence contamination, determine scope of evidence |
| **Collection** | Gather, preserve, and document physical or digital evidence |
| **Analysis** | Systematically scrutinize data for signs of criminal activity, hidden files, timestamps |
| **Reporting** | Document findings, processes, and methodologies used |

### Key Concepts
- **Order of Volatility** — Sequence for collecting data sources based on susceptibility to loss (most volatile first)
- **Chain of Custody** — Documented record tracking handling, transfer, and preservation of evidence from collection to court
- **Disk Imaging** — Creating a bit-by-bit copy of a storage device, preserving deleted files and unallocated space
- **File Carving** — Extracting files and data fragments without relying on the file system
- **Legal Hold** — Formal notification to preserve all potentially relevant electronic data
- **Electronic Discovery** — Identifying, collecting, and producing electronically stored info during legal proceedings

### Data Acquisition
- **Data Acquisition** — Method and tools used to create a forensically sound copy of data from a source device
- Some Windows registry keys (like HKLM\\Hardware) only exist in memory and require a memory dump to analyze

---

## 🤖 Automation and Orchestration (OBJ 4.7)

- **Automation** — Automatic execution of individual tasks without manual involvement
- **Orchestration** — Coordination of multiple automated tasks for a specific outcome or workflow
- **SOAR** — Security, Orchestration, Automation, and Response
- **Playbook** — Checklist of actions for specific incident responses
- **Runbook** — Automated version of a playbook with human interaction points

### When to Consider Before Automating
- Complexity, cost, single points of failure, technical debt, ongoing supportability

### Benefits of Automation
- Increasing efficiency and time savings
- Enforcing baselines consistently
- Implementing standard infrastructure configurations
- Scaling in a secure manner
- Increasing employee retention by removing repetitive tasks
- Decreasing reaction times to security incidents
- Being a workforce multiplier

### What Can Be Automated
- **Support Tickets** — Ticket creation and escalation
- **Onboarding** — Speeds up process, reduces errors, ensures compliance
- **Security** — Guardrails, security groups, permission management
- **Application Development** — CI/CD pipelines

### CI/CD Pipeline

| Term | Description |
|---|---|
| **Continuous Integration (CI)** | Developers merge code changes frequently in one place |
| **Continuous Delivery** | Maintains deployable code; allows manual control of production deployment |
| **Continuous Deployment** | Automates deployment from testing to production |

- **Rollback Capability** — Crucial for ensuring service continuity in continuous deployment

### APIs and Integrations (OBJ 4.7)
- **Integration** — Combining subsystems into one comprehensive system
- **API** — Set of rules and protocols for building and integrating application software
- **REST** — Uses standard HTTP methods, URIs, and MIME types
- **SOAP** — Defines a strict message structure, usually in XML format
- **CURL** — Tool to transfer data to/from a server using supported protocols

---

## 📊 Alerting and Monitoring (OBJ 4.4)

- **Alerting** — Notifying relevant personnel when a potential security incident occurs
- **Monitoring** — Continuous observation of a system or network

### Monitoring Types
- **System Monitoring** — Observation of resource utilization and consumption
- **Application Monitoring** — Management and monitoring of software application performance
- **Infrastructure Monitoring** — Observation of performance and availability of physical and virtual infrastructure

### Monitoring Activities
| Activity | Description |
|---|---|
| **Log Aggregation** | Collecting and consolidating log data into a centralized location |
| **Alerting** | Notifications when specific events or conditions occur |
| **Scanning** | Examining systems for vulnerabilities or configuration issues |
| **Reporting** | Generating summaries based on collected and analyzed data |
| **Archiving** | Storing data for long-term retention |
| **Quarantining** | Isolating a system to prevent spread of a threat |
| **Alert Tuning** | Adjusting alert parameters to reduce false positives |

---

## 📡 SIEM (OBJ 4.4)

- **SIEM** — Provides real-time analysis of security alerts from network hardware and applications
- **Agent** — Software installed on each system to collect log data
- **Agentless** — SIEM collects logs directly using standard protocols (SNMP or WMI)

### SIEM Tools
| Tool | Description |
|---|---|
| **Splunk** | Market-leading big data analysis tool |
| **Elastic Stack (ELK)** | Free and open-source SIEM tools for storage, search, and analysis |
| **ArcSight** | SIEM for compliance reporting (HIPAA, SOX, PCI DSS) |
| **QRadar** | IBM's SIEM for log management and compliance |

### SNMP (OBJ 4.4)
- **SNMP** — Protocol for collecting and organizing info about managed devices on IP networks
- **MIB (Management Information Base)** — Describes structure of management data using a hierarchical namespace
- **Granular Trap** — Each trap message gets a unique identifier
- **Verbose Trap** — Contains all info about an alert as a payload

---

## 🌊 NetFlow and Flow Analysis (OBJ 4.4)

- **Full Packet Capture (FPC)** — Captures the entire packet including header and payload
- **Flow Analysis** — Records metadata and stats rather than each frame
- **NetFlow** — Cisco-developed system for reporting network flow info to a structured database
- **IPFIX** — Defines traffic flows based on shared packet characteristics
- **Zeek** — Passively monitors a network and logs data of potential interest
- **MRTG** — Creates graphs showing traffic flows through network interfaces using SNMP

---

## 🖥️ Single Pane of Glass (OBJ 4.4)

- A central access point for all info, tools, and systems
- Provides security teams with a unified view for informed decision-making

---

## 🔎 Investigating with Data (OBJ 4.9)

| Tool/Source | Description |
|---|---|
| **SIEM** | Real-time analysis combining multiple data sources |
| **Log Files** | Records events in an OS or messages between users |
| **Syslog/Rsyslog/Syslog-ng** | Logging of data from different systems to a central repository |
| **Journalctl** | Linux command for querying and displaying logs from journald |
| **NXLog** | Multi-platform log management tool |
| **NetFlow** | Collects active IP network traffic as it flows in or out of an interface |
| **SFlow** | Provides means for exporting truncated packets for network monitoring |
| **IPFIX** | Universal standard for exporting IP flow info |
| **Metadata** | Data that describes other data |

- **MD5/SHA256** — Serves as unique digital fingerprint for file identification, including potential malware
