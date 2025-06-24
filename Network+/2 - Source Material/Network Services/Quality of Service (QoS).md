2025-04-20 20:19

Status:

Tags: [[Network Services]]

# Quality of Service (QoS)

**QoS (Quality of Service)** allows a network to **optimize performance** by identifying and prioritizing different types of traffic — especially useful for time-sensitive data like voice and video.

---

## QoS Metrics

- **Delay:**  
  The time it takes for a packet to travel from source to destination

- **Jitter:**  
  Variability in packet arrival times. Especially disruptive to **VoIP** because it uses **UDP**, which lacks reordering.

- **Drop:**  
  Packet loss due to network congestion — often occurs when a router's queue overflows

---

## Purpose of QoS

QoS is implemented to:
1. **Classify traffic**
2. **Apply policy rules**
3. **Prioritize data flow**

---

## QoS Models

### Best Effort (No QoS)
- No prioritization
- Packets are sent **first in, first out**
- Default behavior in most networks

### Integrated Services (IntServ)
- **Hard QoS**
- Provides **strict bandwidth reservations** for specific applications
- Requires **resource reservation** on every router along the path (e.g., RSVP)

### Differentiated Services (DiffServ)
- **Soft QoS**
- Packets are **marked** and treated differently depending on their class
- Routers/switches **make decisions locally** based on marking
- More scalable than IntServ

---

## QoS Components

### Classification
- Identifies and separates traffic into different classes (e.g., voice, video, data)
- **Does not modify** packet/frame

### Marking
- **Modifies** bits in packet/frame (e.g., IP header DSCP, Ethernet CoS)
- Informs downstream devices how to treat the traffic

### Congestion Management
- Prioritizes how packets are queued and forwarded during congestion
- Examples include **Weighted Fair Queuing (WFQ)** or **Priority Queuing**

---

## Network+ Key Points

- Know the difference between **IntServ (strict)** and **DiffServ (flexible)**
- **Classification = identify**, **Marking = modify**
- QoS is critical for **VoIP**, **video conferencing**, and **streaming**
- **Best effort = no QoS**, **IntServ = hard QoS**, **DiffServ = soft QoS**

# References
