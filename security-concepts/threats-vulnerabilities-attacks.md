# Threats, Vulnerabilities & Attacks

---

## ⚠️ Core Definitions

- **Threat** — Anything that could cause harm, loss, damage, or compromise to IT systems (natural disasters, cyber-attacks, data integrity breaches)
- **Vulnerability** — Any weakness in system design or implementation (software bugs, misconfigured software, missing patches, lack of physical security)
- **Risk** — The potential for damage; the intersection of threats and vulnerabilities
- Threat + No Vulnerability = No Risk (and vice versa)
- **Risk Management** — Finding ways to minimize the likelihood of a harmful outcome

---

## 🎭 Threat Actors (OBJ 2.1)

Individual or entity responsible for incidents that impact security and data protection.

### Attributes
- **Internal Threat Actors** — Individuals within the org who pose a threat
- **External Threat Actors** — Individuals outside the org attempting to breach defenses
- **Resources and Funding** — Tools, skills, and personnel at the threat actor's disposal
- **Sophistication and Capability** — Technical skill and ability to evade detection

### Motivations
- Data Exfiltration, Financial Gain, Blackmail, Service Disruption
- Philosophical/Political Beliefs, Ethical Reasons, Revenge, Espionage, War, Disruption/Chaos

### Types of Threat Actors

| Actor Type | Description | Sophistication |
|---|---|---|
| **Script Kiddie** | Lacks technical knowledge, uses existing tools | Low |
| **Hacktivist** | Uses skills to promote a cause (website defacement, DDoS, doxing) | Varies |
| **Organized Crime** | Well-structured entities leveraging resources for financial gain | High |
| **Nation-State** | Government-sponsored, conduct complex coordinated operations | Very High |
| **Insider Threat** | Originates from within the org (data theft, sabotage, misuse) | Varies |

- **False Flag Attack** — Attack orchestrated to appear from a different source
- **Advanced Persistent Threat (APT)** — Prolonged targeted attack where an intruder remains undetected for extended periods
- **Shadow IT** — Use of IT systems without explicit org approval
- **Stuxnet Worm** — Sophisticated malware designed to sabotage Iran's nuclear program

---

## 📡 Threat Vectors & Attack Surfaces (OBJ 2.2)

- **Threat Vector** — Pathway by which an attacker gains unauthorized access to deliver a malicious payload
- **Attack Surface** — All points where unauthorized users can try to enter or extract data

### Threat Vectors
- **Messages** — Email, SMS, instant messaging
- **Images** — Malicious code embedded in image files
- **Files** — Malicious files delivering threats
- **Voice Calls** — Tricking victims into revealing sensitive info
- **Removable Devices** — Threats delivered via USB
- **Unsecure Networks** — Lack of appropriate security measures
- **BlueBorne** — Bluetooth vulnerabilities allowing device takeover or malware spread
- **BlueSmack** — DoS attack targeting Bluetooth-enabled devices

---

## 🎣 Social Engineering (OBJ 2.2)

- Exploits human psychology to gain unauthorized access
- Security awareness training is the primary prevention method

### Motivational Triggers (OBJ 5.6)
| Trigger | Description |
|---|---|
| **Authority** | People comply more when requests come from those in higher positions |
| **Urgency** | Compelling immediacy that drives people to bypass security procedures |
| **Social Proof** | Making victims believe "everyone is doing it" |
| **Scarcity** | Psychological pressure from limited availability |
| **Likeability** | Using friendliness to gain trust |
| **Fear** | Capitalizing on anxieties to compel action |

### Types of Social Engineering Attacks
- **Impersonation** — Assuming another person's identity to gain unauthorized access
- **Brand Impersonation** — Pretending to represent a legitimate company
- **Typosquatting** — Registering domains with common typographical errors
- **Watering Hole Attacks** — Compromising a website the target is known to use
- **Pretexting** — Tricking victims by creating a believable scenario
- **Diversion Theft** — Creating a distraction to steal items or info
- **Hoaxes** — Malicious deceptions spread through social media or email
- **Shoulder Surfing** — Looking over someone's shoulder to gather info
- **Dumpster Diving** — Searching trash for valuable info
- **Eavesdropping** — Secretly listening to private conversations
- **Baiting** — Planting a malware-infected device for a victim to find

### Phishing Types (OBJ 2.2)
| Type | Description |
|---|---|
| **Phishing** | Deceptive emails from seemingly trusted sources |
| **Spear Phishing** | Focused on a specific group or individual |
| **Whaling** | Targets high-profile individuals (CEOs, CFOs) |
| **BEC** | Uses internal email accounts to manipulate employees |
| **Vishing** | Phone-based deception |
| **Smishing** | SMS-based deception |

- **Key Phishing Indicators** — Urgency, unusual requests, mismatched URLs, strange email addresses, poor spelling/grammar

### Fraud and Scams
- **Identity Fraud** — Using another person's info without authorization (e.g., stealing credit card info)
- **Identity Theft** — Fully assuming the identity of a victim
- **Misinformation** — Inaccurate info shared unintentionally
- **Disinformation** — Intentional spread of false info

---

## 🦠 Malware (OBJ 2.4)

Any software designed to infiltrate a system without the user's knowledge.

- **Threat Vector** — Specific method used to infiltrate a victim's machine
- **Attack Vector** — Means by which an attacker gains access AND infects the system

### Types of Malware

| Type | Description |
|---|---|
| **Virus** | Malicious code that runs without user knowledge; infects when executed |
| **Worm** | Like a virus but replicates itself without user interaction |
| **Trojan** | Malicious software disguised as harmless software |
| **RAT** | Remote Access Trojan — provides attacker with remote control of victim's machine |
| **Ransomware** | Encrypts data and demands ransom for decryption |
| **Rootkit** | Gains admin-level control without being detected |
| **Keylogger** | Records every keystroke made on a device |
| **Spyware** | Gathers and sends info about a user without their knowledge |
| **Bloatware** | Pre-installed software that takes up resources (not inherently dangerous) |
| **Logic Bomb** | Executes only when certain conditions are met |
| **Backdoor** | Bypasses normal security and authentication |
| **Botnet** | Network of compromised computers controlled by an attacker |
| **Zombie** | A compromised device that's part of a botnet |

### Virus Subtypes
- **Boot Sector Virus** — Stored in first sector of hard drive, loads at boot
- **Macro Virus** — Embedded inside documents, executes when document opens
- **Program Virus** — Infects executable or application files
- **Multipartite Virus** — Combination of boot sector and program virus
- **Encrypted Virus** — Hides by encrypting its malicious code
- **Polymorphic Virus** — Changes its code each time it executes to evade detection
- **Metamorphic Virus** — Rewrites itself entirely before infecting a file
- **Stealth Virus** — Hides from antivirus software
- **Armored Virus** — Has a layer of protection to confuse analysis

### Ransomware Response
- Never pay the ransom
- Disconnect the infected system from the network
- Notify the authorities
- Restore from known good backups

### Rootkit Details
- Embeds deeply into the OS, starting at ring 3 (user-level) working down to ring 0 (kernel mode)
- Traditional antivirus often fails to detect rootkits
- **Most effective detection method** — External system scan
- **DLL Injection** — Technique to gain deeper access by running code within another process's space

### Fileless Malware
- Creates a process in system memory without relying on the local file system
- **Stage 1 (Dropper)** — Malware installed when user clicks malicious link or file
- **Stage 2 (Downloader)** — Downloads and installs a RAT for command and control
- **Concealment** — Hiding tracks by erasing log files and evidence

### Indicators of Malware Attacks
- Account lockouts, concurrent session utilization, blocked content
- Impossible travel, resource consumption, resource inaccessibility
- Out-of-cycle logging, missing logs, published or documented attacks

---

## 🔓 Hardware & Software Vulnerabilities (OBJ 2.3)

- **End-of-Life Systems** — Hardware/software that has reached the end of its lifecycle
- **Legacy Systems** — Outdated systems largely superseded by newer alternatives
- **Unsupported Systems** — Products no longer receiving security updates or patches
- **Unpatched System** — System not updated with latest security patches
- **Zero-Day Vulnerability** — Discovered or exploited before the vendor can issue a patch
- **Zero-Day Exploit** — Unknown exploit exposing a previously unknown vulnerability
- **Malicious Updates** — Attacker crafts a malicious update to a trusted program

### Bluetooth Vulnerabilities
| Attack | Description |
|---|---|
| **BlueJacking** | Sends unsolicited messages to Bluetooth devices |
| **BlueSnarfing** | Unauthorized access to steal contacts, call logs, messages |
| **BlueBugging** | Takes control of device's Bluetooth functions |
| **BlueSmack** | DoS attack that overwhelms a device with data |
| **BlueBorne** | Spreads through the air without user interaction |

---

## 💉 Injection Attacks (OBJ 2.3 & 2.4)

- **SQL Injection** — Inserting malicious SQL statements into input fields
- **XML Bomb (Billion Laughs Attack)** — XML entities that expand exponentially, consuming memory
- **XML External Entity (XXE)** — Embeds a request for a local resource
- **LDAP Injection** — Fabricates LDAP statements via user input
- **Command Injection** — Executes arbitrary shell commands via a vulnerable web app
- **Best prevention** — Input validation and sanitizing data received from users

---

## 🌐 Web Attacks (OBJ 2.3 & 2.4)

### Cross-Site Scripting (XSS)
- Injects malicious scripts into trusted sites to compromise visitors
- **Non-Persistent XSS** — Only occurs when launched, happens once
- **Persistent XSS** — Inserts code into the backend database
- **DOM XSS** — Exploits client's browser using client-side scripts
- **JavaScript = Most likely XSS attack**

### Session Management
- **Cookie** — Text file storing info about a user when they visit a website
- **Session Hijacking** — Spoofing attack where attacker replaces a host with their own machine
- **Session Prediction** — Attacker predicts the session token to hijack a session
- **Cookie Poisoning** — Modifying cookie contents to exploit application vulnerabilities
- **XSRF (Cross-Site Request Forgery)** — Malicious script exploiting a session started on another site

### Buffer Overflow
- When data exceeds allocated memory, potentially enabling unauthorized code execution
- **Smashing the Stack** — Overwriting the return address to execute malicious code
- **ASLR (Address Space Layout Randomization)** — Randomizes addresses to make buffer overflows harder

### Race Conditions
- Vulnerability where outcome depends on unintended timing of events
- **Time-of-Check (TOC)** — Attacker alters a resource after its state is checked but before operation executes
- **Time-of-Use (TOU)** — Attacker changes state between when it's checked and when it's used
- **Mutex** — Gatekeeper ensuring only one thread processes at a time
- **Deadlock** — Two or more processes unable to proceed, each waiting for the other

---

## 💣 Malicious Activity (OBJ 2.4)

### DoS and DDoS
- **DoS** — Attempts to make a server's resources unavailable
- **Flood Attack** — Sends more packets than a server can handle
- **Ping Flood** — Overwhelms server with ICMP echo (ping) packets
- **SYN Flood** — Initiates multiple TCP sessions but never completes the three-way handshake
- **PDoS (Permanent DoS)** — Permanently damages a networking device by exploiting firmware
- **Fork Bomb** — Creates so many processes it consumes all processing power
- **DDoS** — Multiple machines launch an attack simultaneously
- **DNS Amplification Attack** — Initiates DNS requests from a spoofed IP to flood a website

### DNS Attacks
- **DNS Cache Poisoning** — Corrupts DNS cache with false info
- **DNSSEC** — Adds digital signature to org's DNS data
- **DNS Tunneling** — Uses DNS protocol over port 53 to hide non-DNS traffic
- **Domain Hijacking** — Altering a domain's registration without the registrant's consent
- **DNS Zone Transfer Attack** — Attacker mimics an authorized system to obtain entire DNS zone data

### Directory Traversal
- Allows access to files and directories outside the web root
- **Attackers may hide attempts using %2e%2e%2f to represent ../**
- **Local File Inclusion** — Attacker tries to add a file that already exists
- **Remote File Inclusion** — Attacker tries to execute a script to inject a remote file
- **../ and Local File Inclusion = Directory Traversal**

### Replay and On-Path Attacks
- **Replay Attack** — Intercepts valid data and retransmits it later
- **Session Hijack** — Alters real-time data transmissions
- **On-Path Attack** — Attacker places themselves logically between two hosts
- **SSL Stripping** — Tricks the app into using HTTP instead of HTTPS
- **Downgrade Attack** — Forces a client/server to use a weaker security mode
- **To counter replay attacks** — Use session tokens for unique authentication

### Indicators of Compromise (IoC)
- Account lockouts, concurrent session usage, blocked content
- Impossible travel, unusual resource consumption, resource inaccessibility
- Out-of-cycle logging, missing logs, published articles about a breach

---

## 🕵️ Outsmarting Threat Actors (OBJ 1.2)

- **TTPs (Tactics, Techniques, and Procedures)** — Specific methods associated with a particular threat actor
- **Deceptive and Disruption Technologies** — Mislead, confuse, and divert attackers while detecting threats

| Technology | Description |
|---|---|
| **Honeypot** | Decoy system to attract potential hackers |
| **Honeynet** | Network of honeypots mimicking an entire network |
| **Honeyfiles** | Decoy files placed within a system |
| **Honeytokens** | Data with no real value that is monitored for access |
| **Bogus DNS** | Fake DNS entries in the DNS server |
| **Decoy Directories** | Fake folders and files placed in storage |
| **Port Triggering** | Ports remain closed until specific outbound traffic is detected |
| **Fake Telemetry Data** | System sends fake network data in response to an attacker |
