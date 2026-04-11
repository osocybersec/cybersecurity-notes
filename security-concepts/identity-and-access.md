# Identity & Access Management (IAM)

---

## 📋 Overview (OBJ 4.6)

- **IAM** — Systems and processes used to manage access to ensure the right individuals have the right access at the right times

### IAM Main Processes
1. **Identification** — User claims an identity (username, email)
2. **Authentication** — Verifying the identity of the user
3. **Authorization** — Determines what permissions the user has
4. **Accounting** — Monitoring and recording user actions

### IAM Operations
- **Provisioning** — Creating new user accounts and assigning permissions
- **Deprovisioning** — Removing access rights when no longer required
- **Identity Proofing** — Verifying user identity before account creation
- **Interoperability** — Ability of different systems to work together and share info
- **Attestation** — Validating that user accounts and access rights are correct and up-to-date

---

## 🪪 Multi-Factor Authentication (MFA) (OBJ 4.6)

Security system that requires more than one authentication method from independent categories.

### 5 Categories of Authentication

| Factor | Description | Examples |
|---|---|---|
| **Knowledge** | Something you know | Password, PIN |
| **Possession** | Something you have | Smart card, hardware token, software token |
| **Inherence** | Something you are | Fingerprint, facial recognition, iris scan |
| **Location** | Somewhere you are | Geographic location |
| **Behavior** | Something you do | Keystroke patterns, mouse movement |

- **Passkeys** — Allow users to create and access accounts without a password

---

## 🔑 Password Security (OBJ 4.6)

- **Password Managers** — Store, generate, and autofill passwords to enhance security
- **Passwordless Authentication** — Uses biometric authentication for improved security

### Password Attacks (OBJ 2.4)

| Attack | Description |
|---|---|
| **Brute Force** | Tries every possible combination of characters |
| **Dictionary Attack** | Uses a list of commonly used passwords |
| **Password Spraying** | Tries a small number of common passwords against many accounts |
| **Hybrid Attack** | Combines brute force and dictionary techniques (adds numbers/special chars) |

---

## 🔄 Single Sign-On (SSO) (OBJ 4.6)

- Allows a user to access multiple applications by logging in only once
- SSO works based on a trusted relationship between an application and an Identity Provider

### SSO Technologies

| Technology | Description |
|---|---|
| **Identity Provider (IdP)** | System that creates, maintains, and manages identity info for authentication |
| **LDAP** | Protocol for accessing and maintaining distributed directory info services |
| **OAuth** | Open standard for token-based authentication; allows third-party service access without exposing passwords |
| **SAML** | Standard for logging users into applications based on their sessions in another context |

---

## 🌐 Federation (OBJ 4.6)

- Links electronic identities across multiple distinct identity management systems
- Works by using trust relationships that exist between different systems

### 6-Step Federation Process
1. **Login Initiation** — User accesses a service and chooses to log in
2. **Redirection to IdP** — Service provider redirects user to the IdP for authentication
3. **Authenticating the User** — IdP validates the user's identity after credentials submitted
4. **Generation of Assertion** — IdP creates an assertion with info about the user's identity
5. **Returning to Service Provider** — User is redirected back to the service provider with the assertion
6. **Verification and Access** — Service provider checks the assertion and grants access

---

## 🔐 Privileged Access Management (PAM) (OBJ 4.6)

- Restricts and monitors privileged access within an IT environment

### 3 Key Components
| Component | Description |
|---|---|
| **Just-In-Time Permissions** | Administrative access granted only when needed for a specific period |
| **Password Vaulting** | Stores and manages passwords in a secure digital vault |
| **Temporal Accounts** | Time-limited accounts automatically disabled after a set period |

---

## 🎛️ Access Control Models (OBJ 4.6)

| Model | Description |
|---|---|
| **Mandatory Access Control (MAC)** | Employs security labels to authorize user access |
| **Discretionary Access Control (DAC)** | Resource owner determines who can access each resource |
| **Role-Based Access Control (RBAC)** | Assigns users to roles and grants permissions based on roles |
| **Rule-Based Access Control** | Security policies applied to all users by admins |
| **Attribute-Based Access Control (ABAC)** | Uses object characteristics for access control decisions |
| **Time-Of-Day Restrictions** | Controls access based on the time of the request |

- **Principle of Least Privilege** — Grant users only the minimum access required for their tasks
- **Permission/Authorization Creep** — When a user gains excessive rights during their career progression
- **User Account Control (UAC)** — Ensures actions requiring admin rights are explicitly authorized
