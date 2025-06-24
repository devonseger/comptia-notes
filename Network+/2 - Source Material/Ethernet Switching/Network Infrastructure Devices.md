2025-04-10 18:17

Status:

Tags: [[Ethernet Switching]]

# Network Infrastructure Devices

---

## Router

- **Layer 3** device (Network Layer)
- Connects **multiple networks**
- Forwards packets based on **IP addresses**
- **Breaks up both collision and broadcast domains**
- Each interface is its own **broadcast domain**

---

## Switch

- Layer 2 device (Data Link Layer)
- Known as a **multiport bridge**
- Connects devices within the **same network**
- Maintains a **MAC address table**
- **Each port is its own collision domain**
- All ports are in the **same broadcast domain** by default (unless VLANs are used)

---

## Bridge

- Layer 2 device
- Connects **two network segments**
- Makes forwarding decisions based on **MAC addresses**
- Reduces collision domains by segmenting traffic
- Used before switches became common

---

## Hub

- Layer 1 device (Physical Layer)
- Known as a **multiport repeater**
- **Repeats** all traffic to every port
- All ports are in the **same collision and broadcast domain**
- Variants:
  - **Passive hub:** No signal boost
  - **Active hub:** Amplifies signal
  - **Smart hub:** Active hub with **SNMP** features (Ports **161**, **162** UDP)

---

## Layer 3 Switch

- Functions as a **switch + router**
- Makes **Layer 3 routing decisions**
- Used to interconnect networks with faster switching performance
- Each port is its own **collision** and **broadcast domain** (like a router)
- Not as feature-rich or flexible as dedicated routers

---

## Domain & OSI Layer Comparison Table

| Device         | OSI Layer | Collision Domains       | Broadcast Domains        |
|----------------|-----------|--------------------------|---------------------------|
| **Hub**        | Layer 1   | One shared domain        | One shared domain         |
| **Bridge**     | Layer 2   | One per interface        | One shared domain         |
| **Switch**     | Layer 2   | One per port             | One shared domain (unless VLANs) |
| **Router**     | Layer 3   | One per interface        | One per interface         |
| **Layer 3 Switch** | Layer 3 | One per port             | One per port              |

---

# References
