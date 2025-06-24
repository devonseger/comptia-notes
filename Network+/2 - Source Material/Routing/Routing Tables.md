2025-04-16 17:25

Status:

Tags: [[Routing]]

# Routing Tables

A routing table is used by routers to determine the best path for forwarding packets. Among multiple entries, the one with the **longest prefix match** (most specific) is selected.

---

## Types of Routes

### Directly Connected Route
- Automatically added when a physical interface is **up and configured**
- Indicates a network that is directly reachable via one of the router's interfaces

### Static Route
- Manually configured by a network administrator
- Used for **simple or predictable routing paths**

### Default Static Route
- Syntax: `0.0.0.0/0`
- Means: “If no other route matches, send traffic here”
- Often used to route unknown destinations to a firewall, upstream ISP, or internet gateway

### Dynamic Route
- Learned automatically through **routing protocols**
- Routers exchange information to build/update routing tables

---

## Loop Prevention Mechanisms

### Split Horizon
- Prevents a route learned on one interface from being advertised **back out the same interface**
- Helps avoid routing loops
- Similar conceptually to **Spanning Tree Protocol** in switching

### Poison Reverse
- Advertises a route back out the interface it was learned on, but with an **infinite metric**
- Signals that the route is no longer valid
- Reinforces loop prevention in distance-vector protocols

---

# References
