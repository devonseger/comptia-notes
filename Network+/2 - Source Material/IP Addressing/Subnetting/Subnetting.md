2025-04-15 17:25

Status:

Tags: [[Network+/3 - Tags/IP Addressing|IP Addressing]]

# Subnetting

**Subnetting** is the process of dividing a larger network into smaller subnetworks (subnets). It improves routing efficiency, reduces broadcast domains, and allows better control over network traffic and address allocation.

---

## Subnet Masks

Subnet masks determine which portion of an IP address is the **network** portion and which is the **host** portion.

- Example Subnets:
  - `10.0.0.0/24` = 256 IPs 
  - `10.0.1.0/24` = another 256 IPs
  - `10.0.2.0/24` = another 256 IPs

---

## Classful vs Classless

- Classful: `/8`, `/16`, `/24` (traditional defaults)
- Classless: Anything else (e.g., `/25`, `/19`) — allows more flexible subnetting using CIDR

---

## Subnetting Example – /25

- Address: `192.168.1.0/25`
- Subnet mask: `255.255.255.128`
- Breakdown:
  - Network: `192.168.1.0`
  - First usable: `192.168.1.1`
  - Last usable: `192.168.1.126`
  - Broadcast: `192.168.1.127`

---

## Calculating Subnets

**Formula:** `2^s`  
`s` = number of bits borrowed from host portion

- Example:
  - /24 → /25 (1 bit borrowed)
  - `2^1 = 2 subnets`

---

## Calculating Usable Hosts

**Formula:** `2^h - 2`  
`h` = number of host bits

- Example: /25
  - 32 total bits – 25 network bits = 7 host bits
  - `2^7 - 2 = 126 usable hosts`

The subtraction of 2 accounts for:
- Network address
- Broadcast address

---

## CIDR, VLSM, and Aggregation

### Classless Inter-Domain Routing (CIDR)

- Allows route summarization using slash notation (e.g., `/22`)
- Enables efficient use of address space

### Variable-Length Subnet Mask (VLSM)

- Allows subnetting with **different sized subnets**
- Reduces IP waste
- Requires routing protocols that support it (e.g., OSPF, EIGRP)

---

## CIDR Subnet Chart (/30 to /16)

| CIDR | Equivalent /24s      | Usable IPs (Hosts) |
|------|----------------------|--------------------|
| /30  | 1/64 of a /24        | 2                  |
| /29  | 1/32 of a /24        | 6                  |
| /28  | 1/16 of a /24        | 14                 |
| /27  | 1/8 of a /24         | 30                 |
| /26  | 1/4 of a /24         | 62                 |
| /25  | 1/2 of a /24         | 126                |
| /24  | 1 /24                | 254                |
| /23  | aggregates 2 /24s    | 510                |
| /22  | aggregates 4 /24s    | 1022               |
| /21  | aggregates 8 /24s    | 2046               |
| /20  | aggregates 16 /24s   | 4094               |
| /19  | aggregates 32 /24s   | 8190               |
| /18  | aggregates 64 /24s   | 16382              |
| /17  | aggregates 128 /24s  | 32766              |
| /16  | aggregates 256 /24s  | 65534              |

---

# References
