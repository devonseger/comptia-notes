2025-04-10 12:24

Status:

Tags: [[Ethernet Switching]]

# Ethernet Fundamentals

Ethernet is the dominant LAN technology, using a **contention-based protocol** to manage access and communication over shared media.

---

## Legacy Ethernet Standards

### 10Base5 (Thicknet)

- Used **coaxial cable** with **vampire taps**
- Max length: **500 meters**
- Very bulky and hard to manage

### 10Base2 (Thinnet)

- Used **RG-58 coaxial cable** and **BNC connectors**
- Max length: **185 meters**
- Easier to work with than 10Base5

---

## 10Base-T Ethernet

- Allowed **10 Mbps** Ethernet over **twisted pair (Cat 3)** cabling
- Max cable length: **100 meters**
- First step toward structured cabling and modern Ethernet topologies

---

## Deterministic vs. Contention-Based

### Deterministic

- **Organized** and predictable
- Devices take turns transmitting based on scheduling
- Example: **Token Ring networks**

### Contention-Based

- Devices **compete for access**
- More efficient, but **collisions can occur**
- **Ethernet is contention-based**

> Example: In an 8-device 10 Mbps network, each device effectively averages **1.25 Mbps**. Add more devices → total capacity is shared further (1/n).

---

## CSMA/CD – Carrier Sense Multiple Access with Collision Detection

Used in **half-duplex Ethernet** environments (mostly historical today, but still testable).

### Breakdown:

- **Carrier Sense (CS):**  
  Listen before transmitting
- **Multiple Access (MA):**  
  All devices share the same medium and can attempt transmission
- **Collision Detection (CD):**  
  If a collision occurs, devices:
  - **Stop transmitting**
  - Wait for a **random backoff timer**
  - **Retry** after timer expires

> Analogy: Two people walking toward each other in a hallway, then both step side-to-side and block each other again — backoff = waiting randomly so they don’t collide again.

---

## Collision Domains

- A **collision domain** is a portion of the network where devices share a **single data path** and can collide
- Devices connected to **hubs** operate in **half-duplex** and share the same collision domain

### Key Notes:

- **Each port on a switch** is its **own collision domain**
- This means a switch significantly **reduces collisions**
- Devices on switches operate in **full-duplex**, eliminating collisions altogether

---

## Ethernet Switches

- Switches improve performance and scalability by:
  - **Segmenting collision domains** (per port)
  - Allowing **simultaneous full-duplex** communication
- Greatly reduce network congestion compared to hubs
- Operate at **Layer 2** of the OSI model (switching by MAC address)

---

# References
