2025-04-13 22:05

Status:

Tags: [[Ethernet Switching]]

# Maximum Transmission Unit (MTU)

**MTU** refers to the **largest size (in bytes)** of a packet or frame that can be transmitted over a network without requiring fragmentation.

---

## ⚙️ General Guidelines

- MTU size is measured in **bytes**
- Standard Ethernet MTU: **1500 bytes**
- Wireless MTU: Slightly smaller due to wireless overhead
- MTU too **high**: May cause **packet loss** if routers must fragment and fragmentation is disallowed
- MTU too **small**: Leads to **increased overhead** due to more packets for the same amount of data

---

## 🛡️ VPN and PPPoE Considerations

- VPN (IPSec, SSL) and PPPoE add **extra encapsulation headers**
- These headers increase the total packet size
- Recommended MTU in these scenarios: **~1400 bytes**
- Prevents fragmentation and ensures compatibility with tunneling protocols

---

## 🧱 Jumbo Frames

- Refers to frames **larger than 1500 bytes**
- Common jumbo frame size: **9000 bytes**
- Typically used in:
  - **Data centers**
  - **Storage networks (iSCSI, NAS)**
  - **High-performance computing (HPC)**

### Pros:
- Reduces **CPU overhead**
- Improves **throughput** on high-speed links

### Cons:
- Can cause **fragmentation** on incompatible links
- Increases difficulty in **troubleshooting** MTU mismatch issues
- Must be **supported and configured consistently** on all network devices (NICs, switches, routers)

> 🔍 *Always monitor the network before and after enabling jumbo frames to assess performance impact and ensure end-to-end support*

---

## ✏️ Quick Reference

| Network Type     | Typical MTU     |
|------------------|-----------------|
| Ethernet (standard) | 1500 bytes     |
| VPN / PPPoE      | ~1400 bytes      |
| Jumbo Frames     | 9000 bytes       |

---

# References
