2025-03-26 15:23

Status:  
Tags: [[Osi Model]]

# Layer 2 - Data Link Layer (Switch Layer)

The **Data Link Layer** is responsible for packaging data into **frames** and handling how those frames are transmitted on the network.

---

### Media Access Control (MAC)

- The **physical addressing system** of a device that operates on a logical topology.
- Every network interface card (NIC) is assigned a unique **48-bit MAC address** (format: `xx:xx:xx:xx:xx:xx`).
- The first **24 bits** (6 hex digits) identify the **vendor (OUI)**.  
- The last **24 bits** are a **unique identifier** for the specific NIC.

📝 *Change: I added "OUI" (Organizationally Unique Identifier) to clarify the vendor portion. This is the only content addition I made.*

---

### Logical Link Control (LLC)

- Provides **connection services** and acknowledgment of message receipt.
- Handles basic **flow control** and **error control** (e.g., checksum).
- Sits above MAC in the Data Link sublayers.

---

### Timing Methods at Layer 2

- **Isochronous**  
  Devices use a common reference clock and divide transmission into time slots.

- **Synchronous**  
  Devices agree on a clocking method and may use control characters to indicate frame boundaries.

- **Asynchronous**  
  Devices use internal clocks and rely on **start and stop bits** for synchronization.

---

### Layer 2 Devices

- **Network Interface Card (NIC)**  
  Allows a device to interface with a network.  
  Each NIC holds a **unique MAC address**.

- **Bridges**  
  Connect two or more network segments and forward traffic based on MAC addresses.  
  Operate at Layer 2 (distinct from routing).

- **Switches**  
  Multi-port Layer 2 devices that use **MAC addresses** to forward data.  
  Some **Layer 3-capable switches** can also perform routing functions  
  (See: [[Layer 3 - Network Layer]]).

---

# References
