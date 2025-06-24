2025-04-10 19:02

Status:

Tags: [[Ethernet Switching]]

# VLAN Config

---

## 802.1Q (VLAN Tagging)

- IEEE standard for tagging Ethernet frames with **VLAN IDs**
- Enables the transmission of **multiple VLANs over a single trunk link**
- Adds a **VLAN tag** into the Ethernet frame
- Used to **logically separate traffic** while sharing the same physical infrastructure

### Trunking

- Trunk ports carry traffic from **multiple VLANs**
- Used to interconnect **switches** or **routers with switches**
- 802.1Q tagging ensures that VLAN information is preserved

> 📌 *Tagging helps maintain VLAN isolation and supports multi-department setups over shared links*

---

## Native VLAN

- The **one VLAN** on a trunk port that does **not get tagged**
- If a frame enters the trunk **without a tag**, it is assigned to the **native VLAN**
- By default, **VLAN 1** is the native VLAN on most switches (e.g., Cisco)

> ⚠️ Always **match the native VLAN** configuration across all interconnected switches to avoid misrouted or dropped traffic

---

## Voice VLAN

- A VLAN **dedicated to VoIP (voice) traffic**
- Prioritizes **low-latency, low-jitter** transmission
- Enables:
  - **Quality of Service (QoS)** policies
  - **Traffic separation** between voice and data

> 🎙️ Use separate VLANs for phones and computers, even if they share a physical port (via switchport voice vlan)

---

## Link Aggregation

Also known as:

- **Port channeling**
- **EtherChannel (Cisco)**
- **Bonding**

Combines multiple physical links into **one logical interface** to:

- Increase **bandwidth** (e.g., 4x1Gbps = 4 Gbps)
- Improve **resiliency** — if one link fails, traffic still flows
- Often used for **trunk links between switches**

> Must be configured identically on both sides of the link

---

## Speed and Duplex Configurations

### Speed

- Measured in **Mbps** or **Gbps**
- Common values: 10 Mbps, 100 Mbps, 1 Gbps, 10 Gbps

### Duplex

- **Half-Duplex**:
  - Send OR receive (not at the same time)
  - Like a **walkie-talkie**
- **Full-Duplex**:
  - Send AND receive simultaneously
  - Like a **phone call**

> ✅ Full-duplex is used almost universally in modern networks

---

## Auto-Negotiation

- Devices automatically detect and use the **highest common speed and duplex setting**
- Typically enabled by default on modern switches and NICs
- However, **mismatched speed/duplex** (e.g., auto vs manual) can cause:
  - One-way communication
  - High latency
  - Excessive collisions or CRC errors

> 🔧 Manual config may be preferred for **critical links** or when troubleshooting

---


## 🔌 Access vs Trunk Port Cheat Sheet

| Feature               | **Access Port**                            | **Trunk Port**                              |
|----------------------|---------------------------------------------|---------------------------------------------|
| Purpose              | Connects to **end devices** (PCs, printers) | Connects to **other switches/routers**      |
| VLAN Traffic         | Carries **traffic for a single VLAN**       | Carries **traffic for multiple VLANs**      |
| VLAN Tagging         | ❌ No VLAN tag (untagged)                   | ✅ Uses **802.1Q tagging**                   |
| Default Behavior     | Assigned to **one VLAN**                    | Can carry **all VLANs** (or specific ones)  |
| Example Use          | Workstation port                            | Switch-to-switch link                       |
| Native VLAN Usage    | Not relevant                                | Used for **untagged traffic**               |
| Config Command (Cisco) | `switchport mode access`<br>`switchport access vlan <#>` | `switchport mode trunk`<br>`switchport trunk allowed vlan <list>` |

---

### 🧠 Tips for the Exam

- **Access Port** = one VLAN, no tags  
- **Trunk Port** = multiple VLANs, uses tags  
- **Native VLAN** = traffic on trunk without a tag goes here  
- Use trunks between switches, use access ports for clients

---

### 🎯 Real-World Scenario

If a PC is connected to a port, make it an **access port**.  
If two switches are connected, make that link a **trunk port** with **802.1Q tagging** enabled.


# References
