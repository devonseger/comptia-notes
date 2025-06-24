2025-03-31 22:28

Status:

Tags: [[Ports and Protocols]]

# Network Service Ports and Protocols

These protocols enable devices to **discover**, **communicate**, and **coordinate** with each other across networks. They play critical roles in automating, monitoring, and managing network infrastructure.

---

## Domain Name System (DNS)

- Translates **human-friendly domain names** (like google.com) into **IP addresses**
- Operates over **port 53**
- Uses:
  - **UDP** by default (faster, used for standard queries)
  - **TCP** for zone transfers or when response size exceeds UDP limits

---

## Dynamic Host Configuration Protocol (DHCP)

- Automatically assigns:
  - IP addresses
  - Subnet masks
  - Default gateways
  - DNS servers
- Uses **UDP**
  - **Port 67** – Server listens
  - **Port 68** – Client receives

---

## SQL Services

Used by database systems to allow remote query and management of structured data.

- **Microsoft SQL Server** – Port **1433**
- **MySQL** – Port **3306**
- Often run over **TCP**

---

## Simple Network Management Protocol (SNMP)

- Collects and configures information from devices like:
  - Routers, switches, servers, printers
- Uses **UDP**
  - **Port 161** – SNMP Managers send requests
  - **Port 162** – SNMP Agents send traps/alerts

---

## Syslog

- Standard for **logging system events** across devices
- Used by firewalls, routers, and servers to send logs to a **central logging server**
- Operates over **port 514**
  - Typically uses **UDP**, but **TCP** is supported for reliability

---

## Key Points Summary

| Service | Port(s)   | Protocol(s) | Purpose                                      |
|---------|-----------|-------------|----------------------------------------------|
| DNS     | 53        | UDP/TCP     | Domain name resolution                       |
| DHCP    | 67 (server), 68 (client) | UDP   | Dynamic IP assignment                       |
| SQL     | 1433 (MSSQL), 3306 (MySQL) | TCP   | Remote database queries                      |
| SNMP    | 161 (requests), 162 (traps) | UDP   | Network monitoring and device configuration |
| Syslog  | 514       | UDP (default), TCP | Event logging and message collection        |

---

# References
