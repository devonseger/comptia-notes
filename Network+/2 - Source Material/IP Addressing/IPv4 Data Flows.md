2025-04-15 16:36

Status:

Tags: [[Network+/3 - Tags/IP Addressing|IP Addressing]]

# IPv4 Data Flows

IPv4 data transmission can occur in different **flow types**, depending on how many recipients are targeted and how the data is distributed.

---

## 🎯 Unicast

- **One-to-one** communication
- Data is sent from a **single source** to a **single destination**
- Most common type of data flow on modern networks

### Example:
- A regular **phone call**
- Browsing a website
- SSH into a server

---

## 📢 Broadcast

- **One-to-all** communication
- Data is sent from one host to **all devices** on the **same subnet**
- All hosts **process the frame**, even if it wasn’t meant for them

### IPv4 Broadcast Address:
- Last address in the subnet (e.g., `192.168.1.255` for `/24`)

### Example:
- **ARP requests**
- DHCP discovery
- FM radio metaphor: **everyone hears it**

---

## 📡 Multicast

- **One-to-many** communication (but not to everyone)
- Data is sent to **a group of devices** that have opted in (joined the multicast group)
- More efficient than broadcast for group-based applications

### Multicast Range:
- IPv4 Class D: `224.0.0.0 – 239.255.255.255`

### Example:
- **Streaming live video** to a specific audience
- Routing updates (OSPF, EIGRP)
- Teacher speaking to class metaphor: **only students in the room receive it**

---

## Quick Comparison Table

| Flow Type  | Scope         | Delivery               | Example Use Case                |
|------------|---------------|------------------------|---------------------------------|
| Unicast    | One-to-one    | Specific recipient     | Web browsing, file download     |
| Broadcast  | One-to-all    | Everyone in subnet     | ARP, DHCP discovery             |
| Multicast  | One-to-group  | Subscribed devices only| Video streaming, routing updates|

---

# References
