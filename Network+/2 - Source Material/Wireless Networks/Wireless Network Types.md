2025-04-06 15:19

Status:

Tags: [[Wireless Networking]]

# Wireless Network Types

Wireless networks enable devices to communicate without physical cables and can be configured in several ways depending on the use case.

---

## Ad Hoc

- Devices connect **directly** to each other (peer-to-peer)
- No central access point or router
- Useful for:
  - Temporary setups
  - File sharing or quick device-to-device connections
- Typically does **not provide internet access**

---

## Infrastructure Mode

- Devices connect to the network through a **Wireless Access Point (WAP)**  
  - WAP bridges wireless devices to a **wired LAN**
- Most common wireless setup in homes and businesses

### Key Components:

- **SSID (Service Set Identifier):**
  - The **network name** users see and connect to
  - Can be broadcasted or hidden

- **BSSID (Basic Service Set Identifier):**
  - The **MAC address** of the wireless access point
  - Uniquely identifies the AP

- **ESS (Extended Service Set):**
  - Multiple WAPs sharing the same SSID
  - Allows **seamless roaming** across large spaces (e.g., buildings, campuses)

---

## Point-to-Point (P2P)

- Wireless connection between **two fixed locations**
- Often uses **high-gain directional antennas**
- Typically used for:
  - **Building-to-building** links
  - **Wireless bridges** (yes, you're right to associate that term here)
- Offers **dedicated bandwidth** and **long-range** capability

---

## Mesh Networks

- Each node (AP or device) can connect to **multiple other nodes**
- Offers **self-healing** and **load-balancing**
- Excellent for:
  - **Large-scale environments**
  - Areas where **cables aren’t feasible**

### Types:
1. **Infrastructure Mesh:**
   - Uses **WAPs with ESS config**
   - Managed, with a controller or shared backhaul
2. **Hybrid/Ad Hoc Mesh:**
   - Uses multiple different **wireless types working together**
   - Devices may relay data for others

---

## Lightweight Access Point (LWAP)

- Wireless access points that connect back to a **centralized controller** (WLC)
- Centralized management of:
  - SSIDs
  - Security
  - Firmware updates
  - Roaming
- Common in **enterprise networks**

---

# References
