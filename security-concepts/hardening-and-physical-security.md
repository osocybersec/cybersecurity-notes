# Hardening, Asset Management & Physical Security

---

## 🛡️ Hardening (OBJ 2.4, 4.1, & 4.5)

- Process of enhancing the security of a system, application, or network
- Measures: Applying security patches, configuring access controls, disabling unnecessary services, adopting best practices

### Changing Default Configurations (OBJ 2.5)
- Always change: Default passwords, unnecessary open ports, extra open ports

### Restricting Applications (OBJ 2.5)
- **Least Functionality** — Configure workstations with only essential applications and services
- **Secure Baseline Image** — Standardized workstation setup with strict policies
- **Allowlisting** — Only approved applications can run; more secure but complex to manage
- **Blocklisting** — Prevents listed applications while allowing all others; easier but less secure

---

## 🔧 Updates and Patch Management (OBJ 2.5)

| Term | Description |
|---|---|
| **Hotfix** | Solves a security issue; should be applied immediately after testing |
| **Update** | Provides additional functionality; not necessarily security-related |
| **Service Pack** | Includes all hotfixes and updates since the OS release |

### 4-Step Patch Management Process
1. **Planning** — Create policies and procedures to track and verify patch compatibility
2. **Testing** — Test patches in a lab environment before deployment
3. **Implementing** — Deploy patches to all workstations and servers
4. **Auditing** — Scan the network to verify patches were properly installed

---

## 📋 Group Policies (OBJ 2.5 & 4.5)

- Rules or policies applied to users or computer accounts within an OS
- **Access Group Policy Editor** — Open Run prompt and enter "gpedit" (Windows)
- **Security Template** — Group of policies loaded through one procedure
- **Baselining** — Measuring changes in network, hardware, or software to establish what "normal" looks like

---

## 🔐 SELinux (OBJ 2.5 & 4.5)

- **MAC (Mandatory Access Control)** — System-enforced access control based on subject clearance and object labels
- **DAC (Discretionary Access Control)** — Each object has a list of entities allowed to access it
- **SELinux** — Default context-based permission scheme in CentOS and Red Hat Enterprise Linux

### SELinux Contexts (for files and processes)
- **User** — Defines what users can access an object
- **Role** — Defines what roles can access an object
- **Type** — Groups objects with similar security requirements
- **Level (Optional)** — Describes sensitivity level of a file, directory, or process

### SELinux Modes
| Mode | Description |
|---|---|
| **Disabled** | SELinux turned off; MAC not implemented |
| **Enforcing** | All SELinux security policies are enforced |
| **Permissive** | SELinux enabled but policies are not enforced |

---

## 💿 Data Encryption Levels (OBJ 2.5)

| Level | Description |
|---|---|
| **Full-Disk** | Encrypts the entire hard drive |
| **Partition** | Applied only to a specific partition on the storage device |
| **Volume** | Encrypts a set space creating an encrypted container |
| **File** | Encrypts individual files |
| **Database** | Secures the entire database |
| **Record** | Encrypts individual records or rows within a database |

---

## 🏢 Asset Management (OBJ 4.2)

- **Asset Management** — Systematic approach to governing and maximizing the value of items throughout their lifecycle

### Mobile Asset Deployments (OBJ 4.1)
| Model | Description |
|---|---|
| **BYOD (Bring Your Own Device)** | Employees use personal devices; they control their own security |
| **COPE (Corporate-Owned, Personally Enabled)** | Company provides device for both work and personal use |
| **CYOD (Choose Your Own Device)** | Employees choose from a company-approved list |

### Asset Tracking
- **Assignment/Accounting** — Designate individuals as owners for each asset
- **Classification** — Categorize assets based on function, value, or other relevant parameters
- **Monitoring/Tracking** — Ensure proper accountability and optimal use of each asset
- **Enumeration** — Identifying and counting assets, especially during procurement or retirement
- **MDM (Mobile Device Management)** — Securely oversee employee devices and enforce policies

---

## 🗑️ Asset Disposal and Decommissioning (OBJ 4.2)

- **Sanitization** — Making data inaccessible and irretrievable from a storage medium

| Method | Description |
|---|---|
| **Overwriting** | Replacing existing data with random bits of info |
| **Degaussing** | Using a strong magnetic field to disrupt magnetic domains on storage devices; destroys ability to store data |
| **Secure Erase** | Completely deletes data by activating the storage device's built-in erasure routine |
| **Cryptographic Erase** | Destroys the encryption keys, rendering data unreadable |
| **Destruction** | Physical destruction — shredding, pulverizing, melting, incinerating |

- **Certification** — Proof that data or hardware has been securely disposed of

---

## 🔄 Change Management (OBJ 1.3)

- Structured approach to transitioning from the current state to a desired future state
- **Change Advisory Board (CAB)** — Representatives from various parts of the org responsible for evaluating proposed changes
- **Change Owner** — Individual or team that initiates the change request
- **Stakeholder** — Person who has a vested interest in the proposed change
- **Impact Analysis** — Understanding a change's potential fallout

### Change Management Process
1. **Preparation** — Assessing the current state and recognizing the need for transition
2. **Vision for Change** — Clear description of the desired future state
3. **Implementation** — Putting the plan into action
4. **Verification** — Measuring the change's effectiveness against initial objectives
5. **Documentation** — Creating a thorough record of the entire change process

- **Backout Plan** — Predetermined strategy for restoring systems if a change does not go as expected
- **SOP (Standard Operating Procedure)** — Step-by-step instruction guiding a specific task

### Technical Implications of Changes
- **Allow List** — Permitted entities
- **Deny List** — Prevented entities
- **Legacy Application** — Older software that can malfunction from minor updates elsewhere
- Dependencies must be mapped out before implementing any proposed changes

---

## 🏗️ Physical Security (OBJ 1.2 & 2.4)

### Barriers
- **Fence** — Provides visual deterrent, establishes physical barrier, delays intruders — prevents people
- **Bollards** — Short vertical posts to manage vehicular traffic — prevents vehicles
- **Fences = Prevent people | Bollards = Prevent vehicles**

### Brute Force Attacks on Physical Security (OBJ 2.4)
- **Forcible Entry** — Gaining access by physically breaking barriers
- **Tampering with Security Devices** — Manipulating devices to create vulnerabilities
- **Confronting Security Personnel** — Direct confrontation or attack of guards
- **Ramming a Barrier with a Vehicle** — Using a vehicle to breach physical security barriers

### Surveillance Systems (OBJ 1.2)
- Categories: Video surveillance, security guards, lighting, and sensors
- **PTZ (Pan-Tilt-Zoom)** — Can move the camera to better detect issues during an intrusion
- Sensor types: Infrared, pressure, microwave, and ultrasonic

### Bypassing Surveillance (OBJ 2.4)
- **Visual Obstruction** — Blocking the camera's line of sight (e.g., paint on camera)
- **Blind Sensors and Cameras** — Overwhelming sensors with a sudden burst of light
- **Acoustic Interference** — Jamming or playing loud music to disrupt microphones
- **Electromagnetic Interference (EMI)** — Jamming signals surveillance relies on
- **Physical Environment Attack** — Exploiting the environment around surveillance equipment

### Access Control Vestibules (OBJ 1.2)
- Double-door system where only one door can be open at a time
- **Piggybacking** — Person with access intentionally allows unauthorized person to enter with them
- **Tailgating** — Unauthorized person follows an authorized person without their knowledge

### Door Locks (OBJ 1.2)
- **FAR (False Acceptance Rate)** — System authenticates a user who should not have been granted access
- **FRR (False Rejection Rate)** — System denies a user who should have been granted access
- **EER/CER (Equal/Crossover Error Rate)** — Balances FAR and FRR in a biometrics system
- **Cipher Lock** — Mechanical locking mechanism using push buttons and a combination

### Access Badge Cloning (OBJ 2.4)
- **RFID and NFC** — Popular technologies used for contactless authentication
- 3 Steps to Badge Cloning: Scanning → Data Extraction → Writing to a new card
- Prevention: Advanced encryption, MFA, regular protocol updates, user education, shielded wallets, access log monitoring

---

## 👁️ Audits and Assessments (OBJ 5.5)

- **Audits** — Systematic evaluations of info systems, applications, and security controls
- **Assessments** — Detailed analysis to identify vulnerabilities and risks
- **Penetration Testing** — Simulated cyber attack against a system, network, or web application

### Penetration Testing Types
| Type | Description |
|---|---|
| **Offensive / Red Teaming** | Uses attack techniques to find and exploit vulnerabilities |
| **Defensive / Blue Teaming** | Reactive; fortifies systems and improves incident response |
| **Integrated / Purple Teaming** | Combines offensive and defensive testing |
| **Physical Pentesting** | Tests locks, access cards, cameras, and physical protective measures |

### Reconnaissance in Pentesting
| Method | Description |
|---|---|
| **Active Reconnaissance** | Direct engagement with the target — more info, higher detection risk |
| **Passive Reconnaissance** | No direct engagement — lower detection risk, less data |
| **Known Environment (White Box)** | Tester receives detailed infrastructure info from the org |
| **Partially Known (Grey Box)** | Tester receives limited info; partial knowledge of the system |
| **Unknown Environment (Black Box)** | Tester receives minimal to no info — mimics an external attacker |

### Attestation of Findings (OBJ 5.5)
- **Attestation** — Formal validation confirming the accuracy and authenticity of findings
- Proves the penetration test actually occurred and findings are valid
- **Software Attestation** — Validates software hasn't been tampered with
- **Hardware Attestation** — Validates integrity of hardware components
- **System Attestation** — Validates the security posture of a system

---

## 🔏 Vulnerability Management (OBJ 4.3)

- Systematic and ongoing process of identifying, evaluating, prioritizing, and mitigating vulnerabilities

### Identifying Vulnerabilities
- **Vulnerability Scanning** — Automated probing of networks and systems to discover potential vulnerabilities
- **Static Analysis** — Analyzes source code without executing it
- **Dynamic Analysis** — Evaluates an application while it's running
- **Package Monitoring** — Ensures libraries and components are secure and up-to-date

### Threat Intelligence
- **Threat Intelligence Feeds** — Continuous stream of data related to potential or current threats
- **OSINT** — Intelligence collected from publicly available sources
- **Proprietary Feeds** — Commercial vendor threat intelligence under a subscription
- **Dark Web** — Intentionally hidden part of the internet inaccessible through standard browsers
- **Bug Bounty Program** — Encourages researchers to find and report vulnerabilities responsibly

### Analyzing Vulnerabilities
- **CVE (Common Vulnerabilities and Exposures)** — Standardized way to identify known vulnerabilities
- **Exposure Factor (EF)** — Percentage of an asset likely to be damaged if a vulnerability is exploited
- **Risk Tolerance** — Level of risk an org is willing to accept before action is needed

### Vulnerability Remediation
- Patching, purchasing cybersecurity insurance, network segmentation
- Implementing compensating controls
- **Exception** — Temporarily relaxes security controls for operational needs
- **Exemption** — Permanently waives controls for specific reasons (e.g., legacy systems)

### Validating Remediation
- **Rescanning** — Schedule automatic rescans replicating initial scan conditions
- **Auditing** — Maintain detailed records of vulnerabilities, patches, and changes
- **Verification** — Conducting penetration tests and establishing feedback loops

---

## 🌐 Application Security (OBJ 4.1)

- **SAST (Static Code Analysis)** — Reviews source code before the program runs
- **Dynamic Code Analysis** — Tests an application while it's running
- **Fuzzing** — Finds software flaws by bombarding it with random data
- **Code Signing** — Confirms the identity of the software author and guarantees code integrity
- **Sandboxing** — Isolates running programs by limiting the resources they can access

### Network Access Control (NAC) (OBJ 4.5)
- Scans devices for security status before granting network access
- **Persistent Agent** — Software installed on the device requesting access
- **Non-Persistent Agent** — User connects to Wi-Fi and accesses a web portal to authenticate

---

## 🔒 Security Awareness (OBJ 5.6)

- **Situational Awareness** — Being mindful of surroundings, tasks, and potential consequences
- **OPSEC (Operational Security)** — Protects data about routines, project details, and internal procedures against social engineers
- **Don't fall for bait** — Chargers, charging cables, and USB drives left in public areas
- **Policy** — System of rules covering specific topics; must be read AND understood
- **Handbook** — Concise guidance on org-specific procedures; covers broader areas
- Policies and handbooks must adapt to evolving cybersecurity — annual reviews recommended

### Insider Threat Indicators
- Consistently emotionally distressed employees
- Living way above their means (e.g., $80k salary with a $500k car)

### Remote and Hybrid Work Security
- Use secure VPN connections for data access
- Use MFA for an extra layer of security
- Educate employees and promote a security culture
- Use company-issued devices with up-to-date security software
- Implement automated backups
- Use secure collaboration tools with end-to-end encryption
- Maintain clear communication between cybersecurity teams and remote employees
