2025-04-15 16:44

Status:

Tags: [[Network+/3 - Tags/IP Addressing|IP Addressing]]

# Assigning IPv4 Addresses

IPv4 addresses can be assigned using either **static** or **dynamic** methods, depending on network size, administration preferences, and device roles.

---

## Static Assignment

- Manually configured on each host or device
- Requires manual entry of:
  - IP address
  - Subnet mask
  - Default gateway
  - DNS server(s)
- Commonly used for:
  - Servers
  - Printers
  - Network infrastructure devices
- Not practical for large networks due to time and error risk

---

## Dynamic Assignment (DHCP)

- Automatically assigns IP configuration using a **DHCP server**
- Default setup in most home and small office routers
- Provides:
  - IP address
  - Subnet mask
  - Default gateway
  - DNS/WINS servers
- IP addresses are **leased** for a set period and released when expired or disconnected

---

## Related Protocols and Addressing Systems

### DNS (Domain Name System)

- Resolves domain names (like `example.com`) to IP addresses
- Allows users to navigate using names instead of numeric addresses

### WINS (Windows Internet Name Service)

- Legacy name resolution protocol
- Resolves **NetBIOS names** to IP addresses
- Only used in Microsoft Windows domain environments

### BOOTP (Bootstrap Protocol)

- Early version of dynamic IP assignment
- Also used for booting devices over the network
- Largely obsolete; replaced by DHCP

---

## Fallback Addressing

### APIPA (Automatic Private IP Addressing)

- Used when a device fails to get an IP via DHCP and no static IP is assigned
- Assigns an IP in the **169.254.0.0/16** range
- Communication is limited to other APIPA-configured devices on the same LAN
- Cannot route traffic outside of the local network

### Zeroconf (Zero Configuration Networking)

- Based on APIPA
- Includes additional capabilities like:
  - Name resolution
  - Service discovery
- Common in Apple environments (Bonjour)

---

## Summary Table

| Method      | Type      | Scope        | Use Cases                                 |
|-------------|-----------|--------------|-------------------------------------------|
| Static      | Manual    | Local/global | Servers, infrastructure, printers         |
| DHCP        | Dynamic   | LAN          | PCs, mobile devices, DHCP-managed clients |
| BOOTP       | Dynamic   | Legacy LAN   | Old thin clients, network booting         |
| APIPA       | Automatic | Local only   | DHCP fallback, limited LAN comms          |
| Zeroconf    | Automatic | Local only   | Apple devices, peer-to-peer networking    |
| DNS         | Name to IP| Global       | Resolves web/domain names to IPs          |
| WINS        | Name to IP| Local (MS)   | NetBIOS name resolution                   |

---

# References
