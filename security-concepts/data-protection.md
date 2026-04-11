# Data Protection & Resilience

---

## 🗃️ Data Classifications (OBJ 3.3)

- **Sensitive Data** — Any info that can result in a loss of security or advantage if accessed by unauthorized persons
- Overclassifying data leads to protecting all data at a high level, wasting money and resources

### Commercial Business Classifications
| Level | Description |
|---|---|
| **Public** | No impact if released; often in open-source environments |
| **Sensitive** | Minimal impact if released |
| **Private** | Should only be used within the org |
| **Confidential** | Trade secrets, IP, source code — affects business if disclosed |
| **Critical** | Contains the most valuable info |

### Government Classifications
| Level | Description |
|---|---|
| **Unclassified** | Can be released to the public or under Freedom of Info Act |
| **Sensitive but Unclassified** | Wouldn't hurt national security but could impact individuals |
| **Confidential** | Could seriously affect the gov if disclosed |
| **Secret** | Could seriously damage national security if disclosed |
| **Top Secret** | Would damage national security if disclosed |

---

## 👤 Data Ownership (OBJ 4.2 & 5.1)

| Role | Responsibility |
|---|---|
| **Data Owner** | Senior executive responsible for CIA of the info asset |
| **Data Controller** | Decides purposes and methods of data storage, collection, and usage |
| **Data Processor** | Hired by controller to collect, store, or analyze data |
| **Data Steward** | Focused on quality of data and associated metadata |
| **Data Custodian** | Handles management of the system where data is stored |
| **Privacy Officer** | Oversees privacy-related data (PII, SPI, PHI) |

---

## 💾 Data States (OBJ 3.3)

### Data at Rest
- Data stored in databases, file systems, or other storage systems
- Encryption methods: Full disk encryption (FDE), partition encryption, file encryption, volume encryption, database encryption, record encryption

### Data in Transit
- Data actively moving from one location to another
- Encryption methods: SSL/TLS, VPN, IPSec

### Data in Use
- Data in the process of being created, retrieved, updated, or deleted

---

## 📁 Data Types (OBJ 3.3 & 1.4)

| Type | Description |
|---|---|
| **Regulated Data** | Controlled by laws, regulations, or industry standards |
| **PII** | Any info that can be used to identify an individual |
| **PHI** | Any info about health status linked to a specific individual |
| **Trade Secrets** | Confidential business info providing a competitive edge |
| **Intellectual Property (IP)** | Creations of the mind — inventions, artistic works, designs |
| **Legal Info** | Data related to legal proceedings, contracts, or regulatory compliance |
| **Financial Info** | Data related to financial transactions |

- **Data Sovereignty** — Digital info is subject to the laws of the country in which it's located

---

## 🔒 Securing Data (OBJ 3.3)

| Method | Description |
|---|---|
| **Geofencing** | Setting virtual boundaries to restrict data access by location |
| **Encryption** | Transforms readable data into unreadable ciphertext |
| **Hashing** | Converts data into a fixed-size hash value |
| **Masking** | Replacing data with a placeholder like "x" to conceal original content |
| **Tokenization** | Replaces sensitive data with non-sensitive tokens |
| **Obfuscation** | Making data unclear or unintelligible |
| **Segmentation** | Dividing a network into separate segments with their own security controls |
| **Permission Restrictions** | Defining who can access data and what they can do with it |

---

## 🚧 Data Loss Prevention (DLP) (OBJ 4.4)

- Monitors data in use, in transit, or at rest to detect theft attempts

| DLP Type | Description |
|---|---|
| **Endpoint DLP** | Software on workstations monitoring data in use |
| **Network DLP** | Hardware/software at the network perimeter monitoring data in transit |
| **Storage DLP** | Software on servers inspecting data at rest |
| **Cloud-based DLP** | Offered as SaaS for cloud storage needs |

---

## 🔄 Cyber Resilience & Redundancy (OBJ 3.4)

- **Cyber Resilience** — Ability to continuously deliver intended outcomes despite adverse cyber events
- **Redundancy** — Having additional systems or processes to ensure continued functionality if primary ones fail

### High Availability
- **Uptime** — Usually expressed as a percentage
- **Load Balancing** — Distributing workloads across multiple computing resources
- **Clustering** — Multiple computers working together as a single system

### RAID (Redundant Array of Independent Disks)

| RAID Level | Description | Redundancy |
|---|---|---|
| **RAID 0** | Data striping — faster read/write speeds | None |
| **RAID 1** | Mirroring — full copy on two drives | Yes |
| **RAID 5** | Striping with parity across 3+ drives | Yes (1 drive failure) |
| **RAID 6** | Striping with two parity sets | Yes (2 drive failures) |
| **RAID 10** | Combines RAID 1 and RAID 0 | Yes |

- **Failure-resistant** — RAID 1 or RAID 10 (mirroring)
- **Fault-tolerant** — RAID 1, 5, 6, and 10 (uninterrupted operation during hardware failures)
- **Disaster-tolerant** — Protects data from catastrophic events

---

## 📦 Capacity Planning (OBJ 3.4)

Four aspects to consider:
- **People** — Analyzing current skills and forecasting future hiring or training needs
- **Technology** — Assessing current resources and future technological needs
- **Infrastructure** — Considering physical space and utilities
- **Process** — Optimizing business processes to handle demand fluctuations

---

## ⚡ Powering Data Centers (OBJ 3.4)

| Term | Description |
|---|---|
| **Surge** | Small, unexpected increase in voltage |
| **Spike** | Short transient voltage from short circuit or lightning |
| **Sag** | Small, unexpected decrease in voltage |
| **Under-voltage Event** | Voltage reduced for a longer period |
| **Power Loss Event** | Total loss of power |
| **Line Conditioner** | Overcomes minor power fluctuations automatically |
| **UPS** | Provides emergency power for 15-60 minutes during power failure |
| **Generator** | Converts mechanical energy into electrical energy for longer outages |
| **PDC (Power Distribution Center)** | Central hub distributing power to all data center systems |

---

## 💿 Data Backups (OBJ 3.4)

- **Never keep all data on a single device or server**
- **Onsite Backup** — Duplicate data at the same location on separate devices
- **Offsite Backup** — Duplicate data at a geographically separate location
- **Snapshots** — Point-in-time copies capturing a consistent state of data

### Data Recovery Process
1. Selection of the backup
2. Initiating the recovery process
3. Data validation
4. Testing and validation
5. Documentation and reporting
6. Notification to relevant stakeholders

---

## 🏢 Continuity of Operations (OBJ 3.4)

- **BCP (Business Continuity Plan)** — Addresses responses to disruptive events
- **DRP (Disaster Recovery Plan)** — Subset of BCP; focuses on resuming operations after a disaster
- **BCP = Incident | DRP = Disaster**
- Senior management takes charge of BCP/DRP development

### Redundant Sites

| Site Type | Description |
|---|---|
| **Hot Site** | Fully equipped backup facility ready to take over immediately |
| **Warm Site** | Partially equipped; can become operational within days |
| **Cold Site** | No immediate equipment; can be transformed into a facility |
| **Mobile Site** | Portable units (trailers/tents); can be hot, warm, or cold |
| **Virtual Site** | Cloud-based environment; scalable and cost-effective |

- **Platform Diversity** — Using different platforms to prevent single points of failure

### Resilience and Recovery Testing

| Test Type | Description |
|---|---|
| **Tabletop Exercise** | Simulated discussion to improve crisis readiness without deploying resources |
| **Failover Test** | Verifies seamless system transition to a backup |
| **Simulation** | Computer-generated real-world scenario in a virtualized environment |
| **Parallel Processing** | Replicates data and processes onto a secondary system running in parallel |
