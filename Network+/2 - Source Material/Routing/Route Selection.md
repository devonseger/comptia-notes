2025-04-16 17:57

Status:

Tags: [[Routing]]

# Route Selection

Routing decisions are made based on two main criteria:

1. **Longest Prefix Match** (most specific subnet mask)
2. **Administrative Distance** (how believable the source is)

---

## Administrative Distance (AD)

- **Administrative Distance (AD)** is a value that ranks the **trustworthiness** of a route source
- The **lower the number**, the more **preferred** the route
- Think of AD like golf scores — **lower is better**

---

## Route Selection Logic (Simplified)

1. Match destination IP to all routing entries
2. Choose the route with the **longest prefix match**
3. If multiple matches exist, choose the one with the **lowest administrative distance**
4. If still tied, choose the route with the **lowest metric** (based on the routing protocol’s internal logic)

---

## Administrative Distance Table

| Routing Source                     | Administrative Distance |
|------------------------------------|--------------------------|
| **Directly connected**             | 0                        |
| **Static route**                   | 1                        |
| **EIGRP (summary route)**          | 5                        |
| **External BGP (eBGP)**            | 20                       |
| **Internal EIGRP**                 | 90                       |
| **IGRP** (legacy)                  | 100                      |
| **OSPF**                           | 110                      |
| **IS-IS**                          | 115                      |
| **RIP**                            | 120                      |
| **External EIGRP**                 | 170                      |
| **Internal BGP (iBGP)**            | 200                      |
| **Unknown / Untrusted source**    | 255 (never used)         |

> **Note:** AD values are Cisco defaults. Other vendors may vary slightly.

---

# Key Takeaways for Network+:
- **Lower AD wins**
- Know that **directly connected = 0**, **static = 1**, **RIP = 120**, **OSPF = 110**
- **BGP** has **two different ADs**: eBGP = 20, iBGP = 200




# References
