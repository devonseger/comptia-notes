
2025-06-2222:42

Status:

Tags: [[Security+/Tags/Fundamentals of Security|Fundamentals of Security]]


# Integrity

### Definition

**Integrity** ensures that information remains **accurate**, **consistent**, and **unaltered** from its original state, unless intentionally modified by authorized users. It protects data from unauthorized changes—whether malicious or accidental.

---

### Objectives of Data Integrity

- **Ensure Data Accuracy**
    
    - Accurate data leads to correct decision-making and predictable outcomes.
        
- **Maintain Trust**
    
    - Ensures users and stakeholders can rely on data to be truthful and reliable.
        
- **Ensure System Operability**
    
    - Prevents system failures caused by corrupted or tampered data.
        

---

### Methods for Maintaining Integrity

- **Hashing**
    
    - Converts input data into a fixed-length string (hash digest).
        
    - Any change in the input produces a completely different hash, signaling a modification.
        
    - Common algorithms: SHA-256, SHA-3
        
- **Digital Signatures**
    
    - Combines hashing with public-key cryptography.
        
    - Confirms both **integrity** and **authenticity** of a message or document.
        
    - If the hash value verified with the signature doesn’t match, the data was altered.
        
- **Checksums**
    
    - A basic method to detect errors in data transmission by comparing source and destination values.
        
- **Access Controls**
    
    - Limits data modification capabilities to authorized personnel only, minimizing the risk of accidental or intentional changes.
        
    - Includes role-based permissions and change control processes.
        
- **Regular Audits**
    
    - Log and configuration reviews to identify unauthorized changes.
        
    - Helps detect data tampering and ensure that changes are documented and approved.
        

---

### Related Terms

|Term|Description|
|---|---|
|File Integrity Monitoring (FIM)|A security process that detects changes to critical system or configuration files|
|Non-Repudiation|Assurance that someone cannot deny the validity of their actions or signatures|
|Version Control|Systems like Git help track and preserve data history and integrity|




# References