2025-04-16 17:42

Status:

Tags: [[Routing]]

# Routing Protocols

Routing protocols are used by routers to dynamically exchange information and determine the best path for forwarding packets.

---

## Protocol Categories

### Interior Gateway Protocols (IGPs)
- Operate **within a single Autonomous System (AS)** (i.e., a single organization or network)
- Examples: RIP, OSPF, IS-IS, EIGRP

### Exterior Gateway Protocols (EGPs)
- Operate **between different Autonomous Systems**
- Example: BGP

---

## Routing Algorithm Types

### Distance Vector
- Sends the **entire routing table** to directly connected neighbors at **regular intervals**
- Metric: **Hop count**
- Slower convergence
- Example: **RIP**

### Link State
- Each router builds a map of the entire network topology by sharing **link-state advertisements (LSAs)**
- Metric: **Cost** (based on link speed or similar)
- **Faster convergence**
- Examples: **OSPF, IS-IS**

### Hybrid
- Combines features of distance vector and link state
- Example: **EIGRP (Cisco proprietary)**

---

## Key Concepts

### Convergence
- The time it takes for all routers to learn and agree on the best paths after a change in the network

### Hold-Down Timer
- A timer that suppresses route updates for a period of time after a route is believed to be down
- Helps avoid routing flaps and speeds up convergence

### Hop Count
- Number of routers a packet must pass through to reach a destination
- Used as a metric in distance vector protocols like RIP

---

## Interior Routing Protocols

### RIP (Routing Information Protocol)
- **Type:** Distance vector
- **Metric:** Hop count (Max 15 hops, 16 = unreachable)
- **Updates:** Every 30 seconds
- **Protocol:** UDP
- **Notes:** Oldest protocol; easy to configure, not scalable

### OSPF (Open Shortest Path First)
- **Type:** Link state
- **Metric:** Cost (based on bandwidth)
- **Faster convergence** than RIP
- **Open standard**, widely used

### IS-IS (Intermediate System to Intermediate System)
- **Type:** Link state
- **Metric:** Cost
- Similar to OSPF but less commonly used outside of large service provider networks

### EIGRP (Enhanced Interior Gateway Routing Protocol)
- **Type:** Hybrid (distance vector + link state)
- **Metric:** Bandwidth and delay
- **Cisco proprietary**; ideal for Cisco-only networks
- Fast convergence and flexible

---

## Exterior Routing Protocol

### BGP (Border Gateway Protocol)
- **Type:** Path vector
- **Metric:** Autonomous System (AS) hop count
- Used for **inter-AS routing** (i.e., Internet backbone)
- Extremely scalable and policy-driven
- **Slow convergence** but highly configurable

---

# Network+ Exam Notes:
- Know the **difference between distance vector and link state**
- Remember **RIP max hop is 15**
- **OSPF and IS-IS** use **cost**, not hop count
- **EIGRP** = hybrid + Cisco-only
- **BGP** is the only EGP you need to know, and it uses **AS paths**

# References
