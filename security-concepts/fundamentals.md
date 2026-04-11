# Security Fundamentals

Core security concepts from CompTIA Security+ (SY0-701).

---

## 🔑 Basic Definitions

- **Info Sec** — Protecting data
- **Info Systems Sec** — Protecting devices that hold data
- More complexity = Less usability

---

## 🔺 CIA Triad (OBJ 1.2)

| Principle | What It Means | Key Method |
|---|---|---|
| **Confidentiality** | Protecting info from unauthorized access and disclosure | **Encryption** |
| **Integrity** | Ensuring info remains accurate and unchanged unless modified by an authorized user | **Hashing** |
| **Availability** | Ensuring systems and resources are accessible when needed by authorized users | **Redundancy** |

### Confidentiality
- Why it matters: Protect personal privacy, maintain business advantage, achieve regulatory compliance
- Methods: Encryption, access controls, data masking, physical security, training and awareness

### Integrity
- Verifies accuracy and trustworthiness of data over its entire lifecycle
- Why it matters: Ensure data accuracy, maintain trust, ensure system operability
- Methods: Hashing, digital signatures, checksums, regular audits
- **Hash Digest = Digital Fingerprint**

### Availability
- Why it matters: Ensuring business continuity, maintaining customer trust, upholding org's reputation
- Methods: Server redundancy, data redundancy, network redundancy, power redundancy

---

## 🔐 Non-repudiation (OBJ 1.2)

- Providing undeniable proof in digital transactions
- **Non-repudiation = Digital Signatures**
- Digital Signature — Hashing a message and encrypting the hash digest with the user's private key using asymmetric encryption
- Why it matters: Confirming authenticity of digital transactions, ensuring integrity, providing accountability

---

## 🪪 AAA of Security (OBJ 1.2)

### Authentication
- Ensures individuals are who they claim to be
- 5 methods:
  - **Something you know** — Username, password
  - **Something you have** — Employee ID badge, OTP code
  - **Something you are** — Facial recognition, fingerprint
  - **Something you do** — Handshake, handwriting
  - **Somewhere you are** — Geographic location
- **2FA** — Two authentication methods
- **MFA** — Two or more authentication methods

### Authorization
- Permissions and privileges granted to users after authentication
- Set of rules and policies used to dictate what actions users can perform once verified
- Why it matters: Protect sensitive data, maintain system integrity, create streamlined user experiences

### Accounting
- Ensures all user activities are properly tracked and recorded
- Tracked actions: Logging in, accessing files, modifying configs, downloading software, unauthorized attempts
- Systems: Audit Trail, Regulatory Compliance, Forensic Analysis, Resource Optimization, User Accountability
- Tools: Syslog Servers, Network Analyzers, SIEM

---

## 🗂️ Security Control Categories (OBJ 1.1)

| Category | Description | Examples |
|---|---|---|
| **Technical** | Technologies, hardware, and software mechanisms | Antivirus, firewalls, encryption, IDS |
| **Managerial** | Strategic planning and governance | Risk assessments, security policies, training programs |
| **Operational** | Day-to-day procedures governed by human actions | Password change policies, backup procedures, account reviews |
| **Physical** | Tangible, real-world measures | Surveillance cameras, shredding documents, security guards, locked doors |

---

## 🎛️ Security Control Types (OBJ 1.1)

| Type | Description | Example |
|---|---|---|
| **Preventative** | Proactive measures to thwart threats | Firewall |
| **Deterrent** | Discourages attackers by making effort less appealing | Warning signs |
| **Detective** | Monitors and alerts to malicious activities | Security cameras, IDS |
| **Corrective** | Mitigates damage and restores systems | Antivirus quarantine and removal |
| **Compensating** | Alternative measures when primary controls aren't feasible | Different encryption if system can't support latest version |
| **Directive** | Rooted in policy or documentation | Acceptable use policy |

---

## 🚫 Zero Trust (OBJ 1.2)

- Demands verification for every device, user, and transaction regardless of origin
- **Control Plane** — Framework responsible for defining, managing, and enforcing access policies
- **Data Plane** — Ensures policies are properly executed

### Key Elements of Control Plane
- **Adaptive Identity** — Real-time validation considering user behavior, device, location
- **Threat Scope Reduction** — Limit users' access to only what they need (reduces attack surface)
- **Policy-driven Access Control** — Managing user access policies based on roles and responsibilities
- **Secured Zones** — Isolated environments housing sensitive data

### Control Plane Components
- **Policy Engine** — Cross-references access requests with predefined policies (the rulebook)
- **Policy Administrator** — Establishes and manages access policies
- **Subject/System** — The individual or entity attempting to gain access
- **Policy Enforcement Point** — The gatekeeper that actually grants or denies access

---

## 📊 Gap Analysis (OBJ 1.2)

- Process of evaluating differences between an org's current performance and desired performance
- **Technical Gap Analysis** — Evaluating current technical infrastructure against required capabilities
- **Business Gap Analysis** — Evaluating current business processes against required capabilities
- **Plan of Action and Milestones (POA&M)** — Outlines specific measures to address each vulnerability with timelines
