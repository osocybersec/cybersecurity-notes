# Security Concepts

Personal reference sheet of core cybersecurity concepts and terminology.

---

## ⚠️ Risk, Threat & Vulnerability

These three terms are closely related but mean different things:

| Term | Definition | Example |
|---|---|---|
| **Risk** | The potential for damage or loss | A server going offline and losing data |
| **Threat** | What can cause the damage | A hacker attempting to breach the server |
| **Vulnerability** | The weakness that allows the threat in | An unpatched software flaw on the server |

> A risk represents the potential for damage, a threat is what can cause that damage, and a vulnerability is the weakness that allows the threat to cause damage.

### How They Connect
```
Threat exploits a Vulnerability which creates a Risk
```

---

## 🔴 Red Team vs 🔵 Blue Team

### Red Team
A specialized group of cybersecurity professionals who simulate real-world attacks on an organization's systems, networks, and people. Their goal is to test the organization's defenses comprehensively.

- They think and act like real attackers
- They use the same tools and techniques as malicious hackers
- Their findings help organizations identify weaknesses before real attackers do
- Also known as **offensive security**

### Blue Team
The defensive counterpart to the Red Team. They protect, monitor, and respond to attacks.

- Monitor systems for suspicious activity
- Respond to incidents and breaches
- Implement security controls and policies
- Also known as **defensive security**

### Purple Team
A collaboration between Red and Blue teams to improve overall security posture by sharing findings and working together.

| Team | Role | Focus |
|---|---|---|
| 🔴 Red Team | Attackers | Offense — find weaknesses |
| 🔵 Blue Team | Defenders | Defense — protect systems |
| 🟣 Purple Team | Collaborators | Combine both perspectives |

---

## 🔐 Core Security Principles

### The CIA Triad
The three pillars of information security:

| Principle | What It Means | Example |
|---|---|---|
| **Confidentiality** | Only authorized people can access data | Encrypting sensitive files |
| **Integrity** | Data is accurate and hasn't been tampered with | Checksums on downloaded files |
| **Availability** | Systems and data are accessible when needed | Backups and uptime monitoring |

---

## 🧱 Types of Attacks

| Attack Type | What It Means |
|---|---|
| **Phishing** | Tricking users into revealing credentials via fake emails or sites |
| **Brute Force** | Trying many passwords until one works |
| **SQL Injection** | Inserting malicious code into a database query |
| **Man in the Middle** | Intercepting communication between two parties |
| **DoS / DDoS** | Overwhelming a system to make it unavailable |
| **Social Engineering** | Manipulating people rather than systems |

---

## 🗒️ Key Terminology

| Term | Definition |
|---|---|
| **Exploit** | Code or technique that takes advantage of a vulnerability |
| **Payload** | The part of an attack that causes harm |
| **Firewall** | A system that filters incoming and outgoing network traffic |
| **IDS** | Intrusion Detection System — monitors for suspicious activity |
| **IPS** | Intrusion Prevention System — monitors and blocks threats |
| **SIEM** | Security Information and Event Management — collects and analyzes logs |
| **Zero Day** | A vulnerability unknown to the vendor with no patch available |
| **Patch** | A software update that fixes a vulnerability |
| **CVE** | Common Vulnerabilities and Exposures — a public list of known vulnerabilities |
