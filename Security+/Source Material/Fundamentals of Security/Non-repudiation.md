
2025-06-2223:06

Status:

Tags: [[Security+/Tags/Fundamentals of Security|Fundamentals of Security]]


# Non-repudiation

### Definition

**Non-repudiation** ensures that a party in a communication **cannot deny the authenticity** of their signature, message, or transaction. It provides **proof of origin, integrity, and delivery** of data.

---

### Purpose of Non-repudiation

- Confirms the **authenticity** of digital transactions
    
- Ensures **data integrity**
    
- Provides **accountability** by linking actions to specific users or systems
    

---

### Key Mechanism: **Digital Signatures**

A **digital signature** is the primary tool for achieving non-repudiation in cybersecurity.

**How it works:**

1. The sender **hashes** the message or data.
    
2. The hash digest is then **encrypted using the sender's private key** (asymmetric encryption).
    
3. The recipient uses the sender’s **public key** to decrypt the hash and verify that:
    
    - The message hasn't been tampered with (**integrity**).
        
    - The message truly came from the sender (**authentication**).
        
    - The sender **cannot deny** having sent it (**non-repudiation**).
        

> Think: **Digital Signatures = Non-repudiation, Integrity, and Authentication**

---

### Related Concepts

|Concept|Description|
|---|---|
|Asymmetric Encryption|Uses a key pair (public/private) to enable secure communication and signing|
|Public Key Infrastructure (PKI)|Framework for managing digital certificates and key pairs|
|Audit Logs|Records of system and user activity; also support accountability and non-repudiation|
|Message Authentication Code (MAC)|Verifies both the integrity and the origin of a message|
# References