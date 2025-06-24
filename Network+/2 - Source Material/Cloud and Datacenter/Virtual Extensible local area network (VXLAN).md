2025-04-23 19:41

Status:

Tags: [[Cloud and Datacenter]]

# Virtual Extensible LAN (VXLAN)

**VXLAN** is a **network virtualization technology** used to extend Layer 2 networks over a Layer 3 (IP-based) infrastructure. It's commonly used in **cloud environments** and **data centers** to enable scalable multi-tenant deployments and virtual network overlays.

---

## Key Characteristics

- Encapsulates **Layer 2 Ethernet frames** into **Layer 3 UDP packets**
- Allows for **overlay networks** to span multiple Layer 3 domains
- Increases scalability over traditional VLANs

---

## Why VXLAN?

Traditional VLANs support up to **4096** IDs (12-bit limit).  
**VXLAN increases this to over 16 million segments** using a **24-bit VXLAN Network Identifier (VNI)**.

This makes VXLAN ideal for:
- **Large-scale virtualization**
- **Cloud multi-tenancy**
- **Network overlays in SDN environments**

---

## VXLAN Components

### VXLAN Tunnel Endpoints (VTEPs)
- Devices that **encapsulate and decapsulate** VXLAN packets
- Usually located at:
  - Physical servers with hypervisors
  - Network switches or routers
- Responsible for translating Ethernet frames into VXLAN packets and vice versa

### VXLAN Segment
- A **Layer 2 virtual network** (like a VLAN)
- Identified by a **VXLAN Network Identifier (VNI)**
- Allows devices to appear as if they are on the **same broadcast domain**, even if separated by Layer 3 networks

---

## Network+ Key Takeaways
- **VXLAN = Layer 2 over Layer 3**
- Uses **UDP** for transport
- **4096 VLANs → 16 million+ VXLANs**
- VTEPs handle encapsulation/de-encapsulation
- VXLAN segments use a unique **24-bit VNI**

# References
