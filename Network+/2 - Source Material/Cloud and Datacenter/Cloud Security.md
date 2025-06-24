2025-04-23 17:58

Status:

Tags: [[Cloud and Datacenter]]

# Cloud Security

---

## Virtual Private Cloud (VPC)
A **logically isolated** section of a cloud provider’s infrastructure that mimics traditional network environments, but hosted in the cloud.

VPCs allow full control over:
- Subnets
- Routing tables
- Firewall rules
- Internet access
- IP address ranges

---

## Infrastructure as Code (IaC)
- Automates the **deployment and management** of cloud infrastructure through scripts and configuration files
- Promotes **repeatability**, **version control**, and **automated provisioning**
- Tools: Terraform, AWS CloudFormation, Ansible

---

## VPC Components

### Subnet
- A **range of IP addresses** within a VPC
- Subnets can be **public** (internet-facing) or **private** (internal use only)

### Route Table
- Defines **routing rules** for subnets
- Each subnet must be associated with a route table to direct traffic appropriately

### Internet Gateway
- A horizontally scalable and highly available VPC component
- Allows **internet access** for instances in public subnets

### NAT Gateway
- Allows instances in a **private subnet** to initiate outbound traffic to the internet
- Prevents inbound connections **from** the internet

---

## VPC Security Controls

### Network ACL (Access Control List)
- Operates at the **subnet level**
- **Stateless firewall** — must explicitly allow return traffic
- Useful for broad traffic control

### Security Group
- Operates at the **instance level**
- **Stateful firewall** — return traffic is automatically allowed
- Acts like a host-based firewall within the VPC

> ✅ Use **ACLs + Security Groups** together for layered defense.  
> ⚠️ Misconfigured rules are a **common cloud vulnerability.**

---

## Private Cloud Connectivity

### VPC Peering
- Private connection between **two VPCs**
- Enables direct traffic routing without traversing the public internet

### VPC Endpoint
- Allows private access to AWS services from within the VPC
- No need for:
  - Internet gateway
  - NAT gateway
  - VPN
  - Direct Connect

### VPN Connections
- Creates **secure, encrypted tunnels** between:
  - A VPC and an on-prem network
  - Two VPCs in different regions or accounts

---

## Network+ Key Takeaways
- VPCs offer **cloud-level segmentation** and firewalling
- **NAT = outbound only** for private subnets
- **Security Groups = stateful**, **ACLs = stateless**
- Use **VPC peering** or **VPN** for private inter-VPC communication
- IaC improves **security and consistency** by automating deployments

# References
