2025-04-07 13:42

Status:

Tags: [[Wireless Networks]]

# Wireless Security

Wireless networks require robust authentication and encryption mechanisms to prevent unauthorized access and data interception.

---

## Authentication Methods

### Pre-Shared Key (PSK)

- Same password/key used on both:
  - **Wireless Access Point (WAP)**
  - **Client device**
- Common in home and small office setups
- Easy to deploy but **less secure** than enterprise authentication

### 802.1X Authentication

- **Enterprise-grade authentication** used in business environments
- Requires individual users to authenticate using:
  - **Unique usernames and passwords**
  - Often integrates with RADIUS or Active Directory
- Provides **per-user access control** and **audit logging**

---

## Wireless Encryption Protocols

### WEP – Wired Equivalent Privacy

- **Original** 802.11 wireless security protocol
- Uses a **static 40-bit** or **104-bit key** with a **24-bit IV**
- Vulnerable to **brute-force attacks**
- **Should never be used**

### WPA – Wi-Fi Protected Access

- Temporary fix for WEP vulnerabilities
- Uses:
  - **TKIP (Temporal Key Integrity Protocol)**
  - **Message Integrity Check (MIC)** to prevent tampering
- Improved over WEP but still **vulnerable**

### WPA2

- Defined under **IEEE 802.11i**
- Became the **long-time industry standard**
- Uses:
  - **AES (Advanced Encryption Standard)** – 128/192/256-bit
  - **CCMP (Counter Mode with Cipher Block Chaining Message Authentication Code)**
- First introduced with 802.11g, and used in n/ac/ax networks

### WPA3

- Introduced in **2018**
- Enhancements over WPA2:
  - **SAE (Simultaneous Authentication of Equals)** replaces PSK handshake
  - **Stronger encryption and forward secrecy**
  - Better protection for weak passwords

---

## WPS – Wi-Fi Protected Setup

- Designed to simplify secure Wi-Fi connections for **non-technical users**
- Uses:
  - **Push-button**
  - **NFC**
  - **PIN-based authentication**
- ⚠️ Known to be vulnerable to **brute-force attacks**
- **Best practice:** **Disable WPS** on all devices

---

## Best Practices

- ❌ **Never use:** WEP, WPA (original), or WPS  
- ✅ **Use WPA2 or WPA3** whenever possible  
- ✅ In enterprise environments, use **WPA2/3-Enterprise with 802.1X**

---

## Wireless Security Protocol Comparison

| Protocol | Encryption         | Key Type      | Secure? | Notes                                |
|----------|--------------------|---------------|---------|--------------------------------------|
| WEP      | RC4 (static key)   | 40/104-bit    | ❌      | Deprecated; easily cracked           |
| WPA      | TKIP + MIC         | Dynamic PSK   | ⚠️      | Temporary fix, but still weak        |
| WPA2     | AES + CCMP         | PSK or 802.1X | ✅      | Long-term standard                   |
| WPA3     | AES + CCMP + SAE   | 802.1X / SAE  | ✅✅     | Most secure, uses forward secrecy    |
| WPS      | No encryption itself | PIN/Button  | ❌      | Convenience feature, insecure        |

---

# References
