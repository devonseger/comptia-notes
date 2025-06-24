2025-04-17 12:53

Status:

Tags: [[Routing]]

# Routing Redundancy Protocols

Redundancy protocols prevent disruptions in communication by automatically rerouting data traffic in the event of a path or device failure. These protocols ensure **high availability**, especially at the **default gateway** level.

---

## First Hop Redundancy Protocol (FHRP)

FHRPs ensure reliable gateway access by assigning a **virtual IP address** to multiple routers. If the active router fails, a standby router takes over with minimal or no disruption.

---

### Core Concepts

- **Reliability:** Ensures that gateway access remains up even if one router fails
- **Load Balancing:** Some protocols allow traffic distribution across multiple routers
- **Seamless Transitions:** Fast switchover to standby routers
- **Virtual IP:** A shared IP address not tied to a single router
- **Subinterface:** Logical division of a single physical interface (commonly used with VLAN routing)

---

## Common FHRP Protocols

### HSRP (Hot Standby Router Protocol)
- **Type:** Cisco proprietary
- **Function:** Active/standby model with a virtual IP
- **Preempting:** A higher-priority router can take back the active role when it comes online
- **Default Gateway:** Clients point to the virtual IP as their default gateway

### VRRP (Virtual Router Redundancy Protocol)
- **Type:** Open standard (RFC-based)
- **Function:** Functions similarly to HSRP
- **Structure:** One master router, multiple backups
- **Election:** Automatic and simple based on priority values

### GLBP (Gateway Load Balancing Protocol)
- **Type:** Cisco proprietary
- **Function:** Adds **load balancing** to redundancy
- **Unique Feature:** Multiple routers can **actively forward traffic simultaneously**
- **How it works:** Each router is assigned a virtual MAC address to load balance traffic at the gateway level

---

## Summary Table

| Protocol | Type            | Redundancy Style       | Load Balancing | Notes                            |
|----------|------------------|------------------------|----------------|----------------------------------|
| HSRP     | Cisco proprietary | Active / Standby       | ❌             | Preempting supported             |
| VRRP     | Open standard     | Master / Backup(s)     | ❌             | Automatic election               |
| GLBP     | Cisco proprietary | Active / Active        | ✅             | Virtual MACs for traffic sharing |

---

## Network+ Key Points

- Know **HSRP vs VRRP** (Cisco vs open standard)
- GLBP = **redundancy + load balancing**
- All FHRPs use a **virtual IP** for seamless failover
- Preempting = **higher priority router reclaims active role**
- Redundancy improves **availability and uptime** at the default gateway

# References
