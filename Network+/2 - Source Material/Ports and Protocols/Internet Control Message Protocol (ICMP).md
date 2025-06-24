2025-03-31 14:47

Status:

Tags: [[Ports and Protocols Intro]], [[Layer 3 - Network Layer]]

# Internet Control Message Protocol (ICMP)

**Internet Control Message Protocol (ICMP)** is an integral part of the Internet Protocol suite — a set of networking protocols used on the internet.  
It is used for **diagnostics and error reporting**, not for delivering application data.

---

## ICMP Header

- **Type** – 1 byte indicating the type of message being transmitted  
- **Code** – 1 byte providing additional context  
- **Checksum** – 2 bytes used for error checking of the header and data

---

## ICMP Attacks

- **ICMP Flood Attack** – Overwhelms a target machine with a large number of ICMP Echo Request packets, leading to a **Denial of Service (DoS)**

- **Distributed Denial of Service (DDoS)** – An attack where a **botnet** (network of compromised devices) floods the target with traffic

- **Ping of Death** – Sends **malformed or oversized ICMP packets** to crash or destabilize older, unpatched systems  
  - *Note: The maximum IP packet size is 65,535 bytes*  
  - ⚠️ This number **does not relate to the number of ports** (which also range 0–65535) — it's **coincidental**, not connected

---

## Notes

- Many administrators **block ICMP traffic** to prevent abuse, but this can make **network troubleshooting more difficult**
- ICMP is a **network tool**, not a **transport protocol**
  - Enables tools like `ping` and `tracert` (traceroute)

---

# References
