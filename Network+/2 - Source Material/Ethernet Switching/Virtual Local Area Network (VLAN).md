2025-04-10 18:50

Status:

Tags: [[Ethernet Switching]]

# Virtual Local Area Network (VLAN)

A **VLAN** is a logical subdivision of a physical network. VLANs group devices into **separate broadcast domains** using **software configuration** rather than physical layout. This allows you to segment traffic by department (e.g., HR, IT, Admin) even if devices are connected to different physical switches.

---

## VLAN Benefits

### ✅ Enhanced Security

- Devices in different VLANs **cannot communicate by default**
- Helps isolate sensitive systems (e.g., finance or HR)

### ✅ Improved Performance

- Reduces the size of each broadcast domain
- Decreases unnecessary traffic across segments

### ✅ Easier Management

- Allows you to **logically group users or devices**
- Centralizes policy changes, access control, and troubleshooting

### ✅ Cost Efficiency

- Eliminates the need for extra hardware to create network separation
- Multiple VLANs can share the same physical switch

---

## VLAN Trunking

- Allows **multiple VLANs** to travel across a **single physical cable**
- Think of it as **one cable carrying multiple logical paths**
- Used to link switches while maintaining VLAN separation

### How it works:
- **802.1Q (dot1q)** tagging adds a **VLAN ID** to Ethernet frames
- The receiving switch uses this tag to forward the frame to the correct VLAN

---

## VLAN Tagging

- As frames move through VLAN-enabled switches, they are **tagged with a VLAN ID**
- These tags are stripped when the frame reaches an **access port** (end device)

---

## VLAN Configuration Storage

Effective VLANs maintain a **VLAN database**, which includes:

- **VLAN ID**  
- **VLAN name**
- **MTU size (Maximum Transmission Unit)**

### On Cisco devices:
- Stored in a file named: **`vlan.dat`**

---

## Switch Virtual Interface (SVI)

- An **SVI** is a **virtual interface** on a switch used for **inter-VLAN routing**
- Instead of using a separate router, a switch with Layer 3 capabilities can:
  - Route traffic **between VLANs**
  - Assign **IP addresses** to VLANs for management and routing

---

## Summary

- VLANs = **logical broadcast domains**
- Trunking = **transmit multiple VLANs over one cable**
- SVI = **virtual interface for inter-VLAN routing**
- Enhances **security**, **performance**, and **flexibility**

---

# References
