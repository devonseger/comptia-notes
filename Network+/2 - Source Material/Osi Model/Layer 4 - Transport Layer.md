2025-03-26 21:57

Status:  
Tags: [[Osi Model]]

# Layer 4 - Transport Layer

The **Transport Layer** is the dividing line between the upper (Application) and lower (Network) layers of the OSI model.  
The Protocol Data Unit (PDU) at this layer is typically referred to as a **Segment** (for TCP) or **Datagram** (for UDP).

---

### Transmission Control Protocol (TCP) — Segment Data Type

- A **connection-oriented**, reliable protocol for transporting data.
    
- Ensures delivery, packet order, and error correction.
    
- Uses the **Three-Way Handshake** to establish a session:
    
    SYN →  
    ← SYN-ACK  
    ACK →
    
- If the handshake fails, retransmission is attempted until a connection is established.
    

---

### User Datagram Protocol (UDP) — Datagram Data Type

- A **connectionless**, **unreliable** protocol.
    
- No acknowledgment, sequencing, or retransmission of lost packets.
    
- Prioritizes **speed** and low overhead over reliability.
    

---

### TCP vs UDP Comparison

```
+-----------------------------+---------------------------+
| TCP (Transmission Control) | UDP (User Datagram)       |
+-----------------------------+---------------------------+
| Connection-oriented         | Connectionless            |
| Reliable delivery           | No delivery guarantee     |
| Ordered packets             | No ordering               |
| Higher overhead             | Lower overhead            |
| Slower                      | Faster                    |
| Used for:                   | Used for:                 |
| - HTTP/HTTPS                | - DNS                     |
| - FTP, SSH                  | - Streaming, VoIP         |
| - Email                     | - Gaming, Video Calls     |
| Error checking & correction | Basic error checking only |
+-----------------------------+---------------------------+

```

---

### Windowing (TCP)

- Windowing allows endpoints to dynamically **adjust the amount of data** in transit (i.e., how much can be sent before waiting for an acknowledgment).
    
- The "window" can **open or close** to maximize bandwidth while avoiding retransmissions.
    
    - If retransmissions are occurring, the sender may be overwhelming the receiver.  
        → **Close the window** (send less at a time).
        
    - If no retransmissions occur, the sender may be able to transmit more.  
        → **Open the window** (send more at a time).
        

---

### Buffering (Router-Level)

- Occurs when a device (like a router) temporarily **stores packets in memory** due to a mismatch in transmission rates between interfaces.
    
- Example:  
    If Routers 1, 3, and 6 send a combined 210 Mbps to Router 4, but Router 4 can only forward to Router 5 at 50 Mbps,  
    Router 4 **buffers** the excess. If the buffer overflows, packets may be dropped.
    

(Note: Buffering like this is typically associated with Layer 3 devices, but it's often discussed in Transport Layer context due to its impact on flow control and retransmission.)

---

### Layer 4 Protocols & Devices

**Protocols:**

- **TCP** – connection-oriented, reliable, ordered
    
- **UDP** – connectionless, fast, low-overhead, best-effort
    

**Devices that operate at Layer 4:**

- **Firewalls** – filter traffic based on TCP/UDP ports
    
- **Load Balancers** – route traffic based on Layer 4 info (like ports/services)
    
- **WAN Accelerators** – optimize TCP traffic by managing latency, compression, etc.
    

---

# References