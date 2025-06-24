2025-03-31 14:39

Status:

Tags: [[Ports and Protocols]], [[Layer 4 - Transport Layer]]

# User Datagram Protocol (UDP)

**User Datagram Protocol (UDP)** is a communication protocol used across the internet, especially for **time-sensitive transmissions** like streaming, gaming, and VoIP.

- **Low latency** and **reduced processing overhead**
- **No three-way handshake** or windowing overhead
- **Packets (datagrams)** are much smaller:
  - Contain only: 
    - Source port number
    - Destination port number
    - Length field
    - Checksum
  - Typically only **8 bytes** in size, compared to **20–60 bytes** for TCP

- **Stateless**:
  - UDP does **not maintain connection state**
  - Does **not track** packets
  - Does **not require acknowledgements** from the receiver
  - Results in **faster transmission** but **less reliability**

- **Ports** are used to differentiate between services or applications
- **Checksum** provides minimal protection against data corruption

---

# References
