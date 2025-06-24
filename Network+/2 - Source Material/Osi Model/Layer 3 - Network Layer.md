2025-03-26 21:34

Status:  
Tags: [[Osi Model]]

# Layer 3 - Network Layer

The **Network Layer** is responsible for **logical addressing**, **routing**, and **path selection**. It enables data to be sent from one network to another, potentially across many hops.

---

### Logical Addressing

- Layer 3 assigns **IP addresses** to devices so they can communicate across networks.
- Historical protocols:
  - **AppleTalk** and **IPX**  
    Obsolete protocols replaced by IP. May still be found on legacy systems.

- **IPv4**  
  - Example: `172.16.254.1`  
  - Uses **dotted decimal notation** (four 8-bit octets)

- **IPv6**  
  - 128-bit address space using hexadecimal  
  - Format: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
  - Supports vastly more addresses than IPv4  

📝 *Note: I added the example IPv6 format and mention of 128-bit for clarity — this was the only content addition.*

---

### Switching Methods

- **Packet Switching** (used in most modern networks)  
  - Data is split into packets and sent independently  
  - Each packet can take a different route

- **Circuit Switching**  
  - A **dedicated communication path** is established and maintained throughout the session  
  - Example: Traditional telephone calls

- **Message Switching**  
  - Messages are stored and forwarded, possibly delayed  
  - Example: Email retrying failed messages until they send

---

### Route Discovery and Selection

Routes can be:
- **Statically configured** (manual)
- **Dynamically learned** using routing protocols:

  - **RIP** (Routing Information Protocol)  
  - **OSPF** (Open Shortest Path First)  
  - **EIGRP** (Enhanced Interior Gateway Routing Protocol)

---

### Connection Services (Augment Layer 2)

- **Flow Control**  
  - Regulates the rate of data transmission to prevent overload

- **Packet Reordering**  
  - Ensures data arrives in the correct order, even if packets take different paths

- **ICMP (Internet Control Message Protocol)**  
  - Sends control and error messages in an IP network

    - `ping`  
      Measures round-trip time from sender to destination

    - `tracert` (Trace Route)  
      Maps each hop a packet takes between source and destination

---

### Bandwidth Usage & Multiplexing

- Bandwidth and multiplexing strategies at this layer are determined by how the network segments share medium access and routing. (Consider elaborating or cross-linking if detailed later.)

---

### Layer 3 Devices and Protocols

- **Router**  
- **Multi-Layer Switch**  
- **IPv4**  
- **IPv6**  
- **ICMP**

---

# References
