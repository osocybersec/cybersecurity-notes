# Cryptography

---

## 📌 Core Concepts (OBJ 1.4)

- **Cryptography** — Practice and study of writing and solving codes to hide the true meaning of info
- A **cipher** is an algorithm that performs encryption or decryption
- **Encryption strength comes from the key, not the algorithm**
- **Key** — Essential piece of info that determines the output of a cipher
- The longer the key, the stronger the encryption
- Most encryption algorithms are open-source and publicly accessible

---

## 🔑 Symmetric vs Asymmetric (OBJ 1.4)

| Type | Keys Used | Also Known As |
|---|---|---|
| **Symmetric** | Single shared key for both encryption and decryption | Private Key Encryption |
| **Asymmetric** | Different keys for encryption and decryption | Public Key Encryption |

- **Stream Cipher** — Encrypts data bit by bit using a mathematical XOR function
- **Block Cipher** — Breaks input into fixed-length blocks and encrypts each block

---

## 🔒 Symmetric Algorithms (OBJ 1.4)

| Algorithm | Key Size | Block Size | Notes |
|---|---|---|---|
| **DES** | 56-bit effective | 64-bit | Outdated, considered weak |
| **3DES** | 3x DES keys | 64-bit | Encrypts, decrypts, then encrypts again |
| **IDEA** | 128-bit | 64-bit | Symmetric block cipher |
| **AES** | 128, 192, or 256-bit | 128, 192, or 256-bit | Current standard |
| **Blowfish** | Variable | 64-bit | Variable length key |
| **Twofish** | 128, 192, or 256-bit | 128-bit | Successor to Blowfish |
| **RC4** | 40-2048 bit | Stream cipher | Used in SSL and WEP |
| **RC5** | Up to 2048-bit | Block cipher | |
| **RC6** | — | Block cipher | Was a DES replacement candidate |

---

## 🔓 Asymmetric Algorithms (OBJ 1.4)

- Does not require a shared secret key
- The public key is freely available; the private key is kept secret
- **Digital Signature** — Hash digest of a message encrypted with the sender's private key

| Algorithm | Description |
|---|---|
| **Diffie-Hellman (DH)** | Secure key exchange over an unsecure network; used in VPN tunnels and IPSec |
| **RSA** | Based on mathematical difficulty of factoring large prime numbers; 1024-4096 bit keys |
| **ECC** | Based on algebraic structure of elliptical curves; 256-bit ECC = 2048-bit RSA in strength |

---

## #️⃣ Hashing (OBJ 1.4)

- One-way cryptographic function that produces a unique message digest
- **Hash digests are always the same length regardless of input size**
- Used to verify integrity — not for encryption

| Algorithm | Digest Size | Notes |
|---|---|---|
| **MD5** | 128-bit | Considered weak, collision-prone |
| **SHA-1** | 160-bit | Reduces collisions vs MD5, also considered weak |
| **SHA-2** | 224, 256, 384, 512-bit | Family of stronger hash functions |
| **SHA-3** | 224-512-bit | Newest family |
| **RIPEMD-160** | 160-bit | Open-source competitor to SHA family |
| **HMAC** | Varies | Used to check integrity AND authenticity of a message |

- **Digital Signature** — Created by hashing a file, then encrypting the hash digest with a private key
- **Digital Security Standard (DSS)** — Relies on a 160-bit message digest from the Digital Security Algorithm

---

## 🛡️ Increasing Hash Security (OBJ 1.4)

- **Pass the Hash Attack** — Attacker authenticates using a stolen hash instead of the actual password
- **Birthday Attack** — Finding two different inputs that produce the same hash (a collision)
- **Key Stretching** — Increases time needed to crack a weaker key
- **Salting** — Adding random data into a hash to protect against password cracking
- **Nonce** — A "number used once" added to authentication to prevent replay attacks

---

## 🏛️ Public Key Infrastructure (PKI) (OBJ 1.4)

- An entire system of hardware, software, policies, procedures, and people based on asymmetric encryption
- **Certificate Authority (CA)** — Issues digital certificates and maintains trust between CAs worldwide
- **Key Escrow** — Process where cryptographic keys are stored securely with a third party

### Digital Certificates
- Digitally signed electronic documents that bind a public key with a user's identity

| Certificate Type | Description |
|---|---|
| **Wildcard Certificate** | Allows all subdomains to use the same public key certificate |
| **SAN (Subject Alternate Name)** | Specifies additional domains and IP addresses supported |
| **Single-Sided** | Only the server is validated |
| **Dual-Sided** | Both server and user are validated |
| **Self-Signed** | Signed by the same entity whose identity it certifies |
| **Third-Party** | Issued and signed by a trusted CA |

- **Root of Trust / Chain of Trust** — Each certificate is validated back to a trusted root
- **Registration Authority (RA)** — Requests identifying info and forwards to the CA
- **Certificate Signing Request (CSR)** — Block of encoded text containing info about the entity requesting a certificate
- **Certificate Revocation List (CRL)** — Online list of digital certificates the CA has revoked
- **OCSP (Online Certificate Status Protocol)** — Determines revocation status of a certificate using its serial number
- **OCSP Stapling** — Allows certificate holder to get the OCSP record from server at regular intervals
- **Key Recovery Agent** — Software that allows restoration of lost or corrupted keys

---

## 🔧 Encryption Tools (OBJ 1.4)

| Tool | Description |
|---|---|
| **TPM (Trusted Platform Module)** | Dedicated microcontroller securing hardware through integrated cryptographic keys |
| **HSM (Hardware Security Module)** | Physical device managing digital keys, used for mission-critical situations |
| **KMS (Key Management System)** | Integrated approach for generating, distributing, and managing cryptographic keys |
| **Secure Enclave** | Co-processor within the main processor, keeps sensitive data separate even if device is compromised |

---

## 🔗 Blockchain (OBJ 1.4)

- A shared **immutable ledger** for recording transactions, tracking assets, and building trust
- **Public Ledger** — Record-keeping system maintaining participants' identities in a secure and anonymous format
- **Smart/Digital Contracts** — Self-executing contracts where terms are written directly in code
- **Permissioned Blockchain** — Used for business transactions, promotes trust and transparency
- The decentralized and transparent nature ensures smart contracts cannot be altered once deployed

---

## 🎭 Obfuscation Techniques (OBJ 1.4)

| Technique | Description |
|---|---|
| **Steganography** | Concealing a message within another file so its existence is hidden |
| **Tokenization** | Substituting sensitive data with non-sensitive tokens |
| **Data Masking** | Protecting data by making it recognizable but not including sensitive info |

---

## ⚔️ Cryptographic Attacks (OBJ 2.3 & 2.4)

| Attack | Description |
|---|---|
| **Downgrade Attack** | Forces a system to use a weaker or older cryptographic standard |
| **Collision Attack** | Finds two different inputs that produce the same hash output |
| **Pass the Hash** | Authenticates using stolen hash instead of password |
| **Birthday Attack** | Exploits the probability of finding two matching hash digests |

### Quantum Computing and Cryptography
- **Quantum Computing** — Uses quantum mechanics to generate and manipulate qubits for massive processing power
- **Quantum Communication** — Uses qubits made of photons; tamper-resistant and extremely fast
- **Qubit** — A quantum bit that can represent many combinations of ones and zeros simultaneously through superposition
- **Post-Quantum Cryptography** — New cryptographic algorithms resistant to quantum computer attacks
