2025-04-23 19:15

Status:

Tags: [[Cloud and Datacenter]]

# Network Virtualization

Network virtualization allows physical network resources to be **abstracted and managed in software**, making them easier to scale, configure, and automate — especially in cloud and data center environments.

---

## Network Function Virtualization (NFV)

- A **framework** for delivering **network services through software** rather than dedicated hardware
- Introduces **flexibility, agility**, and **cost reduction** to traditional telecom and enterprise networks
- Common in **ISPs, cloud providers, and software-defined networks (SDNs)**

### Benefits:
- Rapid deployment and scaling
- Reduced reliance on specialized hardware
- Dynamic network service chaining

---

## Key NFV Components

### NFV Infrastructure (NFVI)
- The **physical and virtual hardware layer**
- Includes:
  - Compute
  - Storage
  - Network resources
  - Hypervisors and virtualization software
- Hosts and runs **VNFs**

### Virtual Network Functions (VNFs)
- **Software-based versions** of traditional hardware network appliances:
  - Routers
  - Firewalls
  - Load balancers
  - VPN concentrators
- Deployed on virtual machines or containers within the NFVI

### Management and Network Orchestration (MANO)
- Manages the **lifecycle and deployment** of VNFs
- **Orchestrates**:
  - Resource allocation
  - VNF instantiation
  - Scaling and termination
- Acts as the **“brain”** of the NFV ecosystem

---

## Network+ Key Takeaways
- **NFV** replaces hardware appliances with **software-defined services**
- **VNFs** are individual service functions (firewalls, routers, etc.)
- **NFVI** = infrastructure layer (compute + network)
- **MANO** = centralized controller for orchestration and lifecycle management

# References
