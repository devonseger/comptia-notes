2025-04-23 19:25

Status:

Tags: [[Cloud and Datacenter]]

# Software Defined Networking (SDN)

**SDN** is a networking architecture that **separates the control plane from the data plane**, allowing network traffic and policies to be managed via **software-based controllers** and APIs rather than traditional hardware configurations.

It enables:
- **Centralized control**
- **Network automation**
- **Faster deployment**
- Greater agility for cloud-scale and disaster recovery environments

---

## Key SDN Planes

### Control Plane
- Makes decisions about:
  - **Traffic routing**
  - **Security rules**
  - **Policy enforcement**
- Communicates instructions to devices in the data plane

### Data Plane (Forwarding Plane)
- Forwards **actual user traffic**
- Follows rules and decisions provided by the control plane

### Management Plane
- Handles **administrative tasks**
- Interfaces with **monitoring tools, APIs, and configurations**
- Used by network administrators to observe and manage overall network health

---

## Deployment Concepts

### Infrastructure as Code (IaC)
- SDN often works alongside **IaC** tools (e.g., Terraform, Ansible)
- Enables automated provisioning of network resources and services

### SDN Application
- The **software layer** that defines policy decisions, security rules, and traffic shaping
- These rules are then pushed to SDN controllers

---

## SDN Models

### Open SDN
- Based on **open standards and open-source software**
- Often uses the **OpenFlow** protocol

### Hybrid SDN
- Combines **traditional network infrastructure** with SDN features
- Allows for gradual migration

### SDN Overlay
- Creates **virtualized network layers** over existing physical infrastructure
- Common in **multi-tenant cloud environments**

---

## Advantages
- Centralized control and automation
- Programmability and flexibility
- Fast deployment and real-time changes

## Disadvantages
- **Single point of failure** if controller is compromised
- Complex initial setup
- Increased dependency on **software security**

---

## Network+ Key Takeaways
- SDN separates **control** from **data** plane
- Enables **centralized**, programmable network control
- **Overlay networks** = virtualization on top of physical networks
- **Open SDN** = open source; **Hybrid SDN** = mixed with legacy infrastructure
- Critical for **disaster recovery** and **high-availability designs**

# References
