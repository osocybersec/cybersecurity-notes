# Risk, Governance & Compliance

---

## ⚖️ Risk Management (OBJ 5.2)

- **Risk Management** — Identifying, analyzing, treating, monitoring, and reporting risks
- Process: Risk Identification → Risk Analysis → Risk Treatment → Risk Monitoring → Risk Reporting

### Risk Assessment Frequency
| Type | Description |
|---|---|
| **Ad-Hoc** | Conducted as needed, often in response to a specific event |
| **Recurring** | Conducted at regular intervals (annual, quarterly, monthly) |
| **One-Time** | Conducted for a specific purpose and not repeated |
| **Continuous** | Ongoing monitoring and evaluation of risks |

---

## 🔍 Risk Identification (OBJ 5.2)

- **Business Impact Analysis (BIA)** — Evaluates potential effects of disruption to business functions

### Key Metrics
| Metric | Definition |
|---|---|
| **RTO (Recovery Time Objective)** | Maximum acceptable time before lack of a function severely impacts the org |
| **RPO (Recovery Point Objective)** | Maximum acceptable amount of data loss measured in time |
| **MTTR (Mean Time to Repair)** | Average time required to repair a failed component or system |
| **MTBF (Mean Time Between Failures)** | Average time between failures |

---

## 📋 Risk Register (OBJ 5.2)

- Document detailing identified risks: description, impact, likelihood, and mitigation strategies (also known as risk log)
- **Risk Tolerance/Acceptance** — Willingness to deal with uncertainty in pursuit of goals
- **Risk Appetite** — Org's willingness to embrace specific types and levels of risk to fulfill strategic goals
- **Key Risk Indicators (KRIs)** — Predictive metrics signaling rising risk levels

---

## 📊 Risk Analysis (OBJ 5.2)

### Qualitative Risk Analysis
- Assesses risks based on potential impact and likelihood of occurrence (descriptive, not numerical)

### Quantitative Risk Analysis
Numerical evaluation of risk:

| Term | Definition | Formula |
|---|---|---|
| **EF (Exposure Factor)** | Percentage of asset likely to be damaged (0-100%) | — |
| **SLE (Single Loss Expectancy)** | Monetary value expected to be lost in a single event | Asset Value × EF |
| **ARO (Annualized Rate of Occurrence)** | Estimated frequency a threat occurs within a year | — |
| **ALE (Annualized Loss Expectancy)** | Expected annual loss from a risk | SLE × ARO |

---

## 🛡️ Risk Management Strategies (OBJ 5.2)

| Strategy | Description |
|---|---|
| **Risk Transference** | Shifting risk to another party (insurance, contract indemnity clause) |
| **Risk Acceptance** | Recognizing a risk and choosing to address it when it arises |
| **Risk Avoidance** | Altering plans to completely eliminate a specific risk |
| **Risk Mitigation** | Implementing measures to decrease likelihood or impact of a risk |

- **Contract Indemnity Clause** — One party agrees to cover the other's harm, liability, or loss
- **Exemption** — Grants an exception from a specific rule or requirement
- **Exception** — Permits bypassing a rule in certain situations

---

## 📈 Risk Monitoring and Reporting (OBJ 5.2)

- **Risk Monitoring** — Continuously tracking risks and executing response plans
- **Residual Risk** — Likelihood and impact after implementing mitigation measures
- **Control Risk** — Assessment of how a security measure has lost effectiveness over time

---

## 🏢 Governance (OBJ 5.1)

- **Governance** — Strategic leadership, structures, and processes ensuring IT infrastructure aligns with business objectives

### Governance Structures
- **Boards** — Group of directors overseeing org management and strategic direction
- **Committees** — Subgroups of a board with specific focus areas (e.g., audit committee)
- **Government Entities** — Establish laws and regulations orgs must comply with
- **Centralized Structures** — Decision-making concentrated at top levels; consistent but slow
- **Decentralized Structures** — Decision-making distributed throughout; quicker but can lead to inconsistencies

### Key Policies
| Policy | Description |
|---|---|
| **AUP (Acceptable Use Policy)** | Outlines do's and don'ts for users interacting with IT systems |
| **Info Sec Policies** | Outlines how the org protects its info assets |
| **Business Continuity** | Focuses on continuing critical operations during a disruption |
| **Disaster Recovery** | Focuses on recovering IT systems and data after a disaster |
| **Incident Response** | A plan for handling security incidents |
| **SDLC** | Guides how software is developed within an org |
| **Change Management** | Ensures changes are implemented in a controlled manner |

### Standards
- **Password Standards** — Dictate complexity and management of passwords
- **Access Control Standards** — Determine who has access to what resources
- **Physical Security Standards** — Physical measures to protect assets
- **Encryption Standards** — Ensures intercepted data remains unreadable

### Procedures
- **Emergency Evacuation Procedure** — Steps during emergencies like fire or natural disaster
- **Data Backup Procedure** — How and when data should be backed up
- **Change Management** — Systematic approach to dealing with organizational changes
- **Playbooks** — Checklist of actions to detect and respond to specific incident types

### Governance Considerations
| Level | Example |
|---|---|
| **Regulatory** | Data protection, environmental standards |
| **Local** | City ordinances, zoning laws |
| **Regional** | California Consumer Privacy Act (CCPA) |
| **National** | Americans with Disabilities Act (ADA) |
| **Global** | General Data Protection Regulation (GDPR) |

---

## ✅ Compliance (OBJ 5.4)

- **Compliance Reporting** — Collecting and presenting data to demonstrate adherence to requirements
- **Internal Compliance Reporting** — Ensuring the org follows its own policies and procedures
- **External Compliance Reporting** — Demonstrating compliance to regulatory bodies or customers
- **Compliance Monitoring** — Regularly reviewing operations to ensure compliance
- **Attestation** — Formal declaration that the org's processes and controls are compliant
- **Automation in Compliance** — Streamlines data collection and provides real-time compliance monitoring

### Non-Compliance Consequences
- Fines, sanctions, reputational damage, loss of license, contractual impacts

---

## 🤝 Third-Party Vendor Risks (OBJ 5.3)

- **Managed Service Providers (MSPs)** — Provide a range of technology services to businesses

### Supply Chain Risks
- Supply chain attacks target a weaker link to gain access to a primary target
- **CHIPS Act** — U.S. law providing ~$280 billion to boost semiconductor research and manufacturing
- Prevention: Vendor due diligence, regular monitoring and audits, education, contractual safeguards

### Vendor Assessment
| Method | Description |
|---|---|
| **Penetration Testing** | Simulated cyberattack against supplier's system |
| **Internal Audit** | Vendor's self-assessment against industry standards |
| **Independent Assessment** | Evaluation by a neutral third-party entity |
| **Supply Chain Analysis** | Deep dive into vendor's entire supply chain |

- **Right to Audit Clause** — Grants orgs the right to evaluate vendors

### Vendor Selection and Monitoring
- **Due Diligence** — Rigorous evaluation beyond surface-level credentials
- **Conflict of Interest** — Personal/financial relationships that could cloud judgment in vendor selection
- **Vendor Questionnaires** — Documents vendors fill out about operations and compliance
- **Feedback Loops** — Two-way communication channel between org and vendor

### Contracts and Agreements

| Agreement | Description |
|---|---|
| **SLA (Service-Level Agreement)** | Standard of service a client can expect from a provider |
| **MOA (Memorandum of Agreement)** | Formal, outlines specific responsibilities and roles |
| **MOU (Memorandum of Understanding)** | Less binding declaration of mutual intent |
| **MSA (Master Service Agreement)** | Covers general terms across multiple transactions |
| **SOW (Statement of Work)** | Specifies deliverables, timelines, and milestones for a project |
| **NDA (Non-Disclosure Agreement)** | Ensures sensitive info shared during negotiations remains confidential |
| **BPA (Business Partnership Agreement)** | Document for two entities pooling resources for mutual benefit |
