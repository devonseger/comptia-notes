2025-04-24 17:29

Status:

Tags: [[Network Security Fundamentals]]

# Network Security Fundamentals

---

## Confidentiality
- Ensures that **data remains private** and is only accessible to **authorized parties**.
- Prevents unauthorized disclosure of sensitive information.

### Methods to Achieve Confidentiality:
- **Symmetric Encryption**  
  - Both sender and receiver use the **same secret key** for encryption and decryption.
  - **Fast** (approximately 1,000x faster than asymmetric encryption).
  - **Challenge:** Secure distribution of the secret key.
  - Example algorithms: AES, DES

- **Asymmetric Encryption**  
  - **Two different keys** are used: a **public key** (encrypt) and a **private key** (decrypt).
  - Allows secure communication without pre-sharing a secret key.
  - Example algorithms: RSA, ECC

- **Public Key Infrastructure (PKI)**  
  - A system for managing **digital certificates** and **key pairs**.
  - Facilitates **asymmetric key exchanges** and encryption.
  - Relies on trusted Certificate Authorities (CAs).

---

## Integrity
- Ensures that **data remains unchanged** during storage or transmission.
- Verifies that data has **not been altered** either accidentally or maliciously.

### Methods to Ensure Integrity:
- **Hashing**  
  - A process that converts data into a **fixed-length string** (hash or digest).
  - If the hashes match between sender and receiver, data integrity is confirmed.
  - Example hashing algorithms: SHA-256, SHA-3

- **Digital Signatures**  
  - Combines hashing and asymmetric encryption to verify both **integrity** and **authenticity**.

---

## Availability
- Ensures that **data and services are accessible** when needed by authorized users.
- Minimizes downtime and prevents denial of service.

### Methods to Maintain Availability:
- **Redundant Systems** (failover, RAID, clustering)
- **Backups and Disaster Recovery Plans**
- **Load Balancing**
- **DDoS Mitigation Tools**

---

# References
