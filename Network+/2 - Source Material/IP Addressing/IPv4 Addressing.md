2025-04-14 19:30

Status:

Tags: [[Network+/3 - Tags/IP Addressing|IP Addressing]]

# IPv4 Addressing

IPv4 addresses are written in **dotted-decimal notation**, consisting of **four octets**, each with **8 bits**, totaling **32 bits** of addressable space.

---

## 📦 IPv4 Structure

|                          | Octet 1  | Octet 2  | Octet 3  | Octet 4  |
|--------------------------|----------|----------|----------|----------|
| **Dotted-decimal**       | 192      | 168      | 1        | 4        |
| **Binary**               | 11000000 | 10101000 | 00000001 | 00000100 |
| **Subnet mask (binary)** | 11111111 | 11111111 | 11111111 | 00000000 |
| **Network/Host bits**    | Network  | Network  | Network  | Host     |

---

## 🌐 IP Classes & Subnet Masks

| **Class** | **1st Octet Range** | **Default Subnet Mask** | **CIDR** | **Hosts per Network**      |
|-----------|---------------------|--------------------------|----------|-----------------------------|
| A         | 1 – 126             | 255.0.0.0                | /8       | 16,777,214                  |
| B         | 128 – 191           | 255.255.0.0              | /16      | 65,534                      |
| C         | 192 – 223           | 255.255.255.0            | /24      | 254                         |
| D         | 224 – 239           | N/A (Multicast)          | N/A      | N/A                         |
| E         | 240 – 255           | N/A (Reserved)           | N/A      | Reserved (Experimental)     |

> Class D is used for **multicast**. Class E is **reserved for future or research use**.

---

## 🔢 Key Concepts

### Subnetting

- The process of **dividing a larger network** into **smaller subnetworks (subnets)**
- Helps optimize address allocation and **reduce broadcast traffic**
- Involves adjusting the **subnet mask** to "borrow" host bits and create additional networks

### Classful Addressing

- Uses the **default subnet masks** based strictly on address class (A, B, C)
- No custom subnetting allowed
- Example:
  - Class A: 10.0.0.0 → Subnet: 255.0.0.0

### Classless Addressing (CIDR)

- **CIDR = Classless Inter-Domain Routing**
- Introduced to **extend the life of IPv4**
- Allows subnetting **outside of class boundaries**
- Uses **slash notation (/X)** to define the subnet
  - Example: `192.168.1.0/26` = 64 addresses, 62 usable hosts
- CIDR increases **flexibility** and reduces **waste of addresses**

---

## 📡 Multicast Addresses (Class D)

- Range: **224.0.0.0 – 239.255.255.255**
- Designed for **one-to-many** communications
- Used in:
  - Streaming media
  - Routing protocols (OSPF, EIGRP)
  - Conferencing apps

> Unlike broadcast (one-to-all), multicast delivers to **subscribed members only**

---

## 🧠 IPv4 Address Types (For Reference)

| Type           | Description                               |
|----------------|-------------------------------------------|
| Public         | Routable on the internet                  |
| Private        | Reserved ranges for internal networks     |
| Loopback       | 127.0.0.0/8 → Internal testing             |
| APIPA          | 169.254.0.0/16 → Auto-assigned if DHCP fails |
| Broadcast      | All bits set to 1 (e.g., 192.168.1.255)   |
| Multicast      | 224.0.0.0 – 239.255.255.255               |

---

# References
