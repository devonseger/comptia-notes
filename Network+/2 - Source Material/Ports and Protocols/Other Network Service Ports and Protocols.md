2025-03-31 22:46

Status:

Tags: [[Ports and Protocols]]

# Other Network Service Ports and Protocols

These protocols serve various network services such as **time synchronization**, **voice communication**, and **directory access**, each critical to smooth network operation.

---

## Network Time Protocol (NTP)

- Synchronizes clocks between computers across a network
- Crucial for:
  - Encryption (certificates, tokens, etc.)
  - Timestamps
  - Logging consistency
- Operates over **port 123** using **UDP**

---

## Session Initiation Protocol (SIP)

- Used to **initiate, maintain, and terminate** real-time communication sessions:
  - Voice
  - Video
  - Messaging
- Operates over:
  - **Port 5060** – Unencrypted (UDP/TCP)
  - **Port 5061** – Encrypted using **TLS** (TCP only)

---

## Lightweight Directory Access Protocol (LDAP)

- Used to access and maintain **directory services** over IP networks
  - Common in enterprise environments for user authentication, email directories, etc.
- Operates over:
  - **Port 389** – Insecure (TCP/UDP)
- **LDAPS**:
  - Secure version of LDAP using **SSL or TLS**
  - Operates over **port 636 (TCP)**

---

## Summary

- **NTP** – Synchronizes system clocks (Port 123, UDP)
- **SIP** – Manages real-time sessions (5060/5061, UDP/TCP)
- **LDAP/LDAPS** – Directory services and user authentication (389/636, TCP/UDP)

---

## Quick Reference Table

| Protocol | Port(s) | Transport | Secure? | Purpose                                |
|----------|---------|-----------|---------|----------------------------------------|
| NTP      | 123     | UDP       | ❌      | Time synchronization                   |
| SIP      | 5060    | UDP/TCP   | ❌      | VoIP signaling (unencrypted)           |
| SIP-TLS  | 5061    | TCP       | ✅      | VoIP signaling (encrypted with TLS)    |
| LDAP     | 389     | TCP/UDP   | ❌      | Directory services (insecure)          |
| LDAPS    | 636     | TCP       | ✅      | Encrypted LDAP (SSL/TLS)               |

---

# References
