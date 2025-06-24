2025-04-21 21:07

Status:

Tags: [[Wide Area Network]]

# Access Technologies

Access technologies define the various methods by which end users connect to service provider networks for internet and communication services.

---

## Fiber Optic Access

### Fiber to the Home (FTTH)
- Fiber connection runs directly into the residence
- **Highest speed and reliability** for end users

### Fiber to the Curb (FTTC)
- Fiber runs to a nearby cabinet or curb
- Last leg to the user is typically copper

### Fiber to the Node/Neighborhood (FTTN)
- Fiber extends to a centralized point in a neighborhood
- Leverages **existing copper** infrastructure from the node onward

### Fiber to the Building (FTTB)
- Fiber terminates at the building’s **main communication room**
- Often used in apartments or commercial buildings

---

## Cable Internet (DOCSIS)

### Hybrid Fiber-Coaxial (HFC)
- Combines **fiber backbone** with **coaxial cable** to deliver data

### DOCSIS (Data Over Cable Service Interface Specification)
- Governs how data is transmitted over HFC networks
- **Asymmetric speeds** (faster download than upload)
- Used in **cable modem internet service**

---

## DSL – Digital Subscriber Line

### DSL
- Transmits data over **copper telephone lines**
- Requires a DSLAM (DSL Access Multiplexer) at the provider side

### ADSL (Asymmetric DSL)
- Different download and upload speeds
- Most common DSL type for residential use

### SDSL (Symmetric DSL)
- Equal upload and download speeds
- Used in small business applications

### VDSL (Very-high-bit-rate DSL)
- Downloads > 50 Mbps, Uploads ~10 Mbps
- High speed DSL variant, effective over short distances

---

## Satellite Connections

### Satellite Internet Access
- Connects to the internet via geostationary satellites
- Higher latency due to long transmission distance
- Useful for **rural or remote locations**

---

## Cellular Connections

### WCDMA
- Used by UMTS networks
- Speeds up to **2 Mbps**

### HSPA / HSPA+ (3.5G / 3.75G)
- HSPA: up to **14.4 Mbps**
- HSPA+: up to **50 Mbps**

### 4G LTE / LTE-A
- LTE = Long Term Evolution
- LTE-A = Advanced version with improved performance

### GSM (Global System for Mobile Communications)
- Converts voice to digital data for transmission

### CDMA (Code Division Multiple Access)
- Uses spread-spectrum technology to share bandwidth

---

## Microwave Connections

- Uses **line-of-sight radio waves** in the microwave frequency range
- High-speed, point-to-point connection between fixed locations
- Often used for **building-to-building backhaul**

---

## Leased Line Connections

### Dedicated Leased Line
- Fixed-bandwidth, **symmetric** data connection
- **Exclusive use** by one subscriber
- Always-on, **point-to-point** connectivity (e.g., T1, T3 lines)

---

# Network+ Tips
- FTTH is the **fastest** and most future-proof
- DSL and Cable often use **existing infrastructure**
- Satellite = **high latency**, good for remote access
- LTE = most common mobile access technology today
- Leased lines = best for **consistent, guaranteed bandwidth**

## MPLS – Multiprotocol Label Switching

MPLS is a **high-performance WAN protocol** used by service providers to route data efficiently through their backbone networks.

### Key Features:

- **Label-based forwarding**:  
  Packets are forwarded based on **labels**, not IP addresses. This makes routing faster and more predictable.

- **Layer 2.5 technology**:  
  Operates between Layer 2 (Data Link) and Layer 3 (Network) in the OSI model.

- **Supports multiple protocols**:  
  Works with IP, Ethernet, ATM, and Frame Relay — hence the name *Multiprotocol*.

- **Path control**:  
  Traffic follows predetermined **Label Switched Paths (LSPs)** rather than dynamic IP routing decisions.

- **QoS integration**:  
  Supports **Quality of Service** by prioritizing different types of traffic (voice, video, etc.)

- **Redundancy and failover**:  
  Rapid rerouting in case of failure, leading to **high availability**

### MPLS Use Cases:
- **Enterprise WANs** connecting remote offices through a service provider’s backbone
- **Voice over IP (VoIP)** and real-time traffic prioritization
- **Cloud service access** via provider edge

---

## Network+ Key Points:
- MPLS improves performance by using **labels** instead of routing lookups
- Considered a **private WAN** solution — **not a public internet connection**
- Commonly used for **enterprise-grade connectivity** with QoS guarantees


# References
