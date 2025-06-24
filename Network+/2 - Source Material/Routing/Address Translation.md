2025-04-17 12:15

Status:

Tags: [[Routing]]

# Address Translation

**Network Address Translation (NAT)** is used to conserve public IPv4 addresses by allowing private IP addresses to communicate over public networks.

---

## Types of NAT

### Static NAT (SNAT)
- **Manual** one-to-one mapping
- A specific private IP is always mapped to the same public IP
- Useful for servers (e.g., web or email servers)

### Dynamic NAT (DNAT)
- Automatically selects a public IP from a **pool**
- Still a **one-to-one** mapping, but not permanently assigned
- Only works if enough public IPs are available

### Port Address Translation (PAT)
- Also known as **NAT Overload**
- Maps **multiple private IPs** to **a single public IP**
- Differentiates sessions using **port numbers**
- Most common form of NAT in home and business routers

---

## NAT Address Terms (Cisco Terminology)

| Term           | Description                                         |
|----------------|-----------------------------------------------------|
| Inside Local   | Private IP of a device **inside** the network       |
| Inside Global  | Public IP assigned to that inside device (NAT'd)    |
| Outside Local  | IP of an external device, as seen **from inside**   |
| Outside Global | Public IP of the external device on the **internet**|

> These terms describe how NAT views traffic depending on direction and scope.

---

## Network+ Key Points:
- NAT helps with **IPv4 exhaustion**
- **PAT = most common**, used in homes and small businesses
- Know the **differences between SNAT, DNAT, and PAT**
- Understand the **inside/outside local/global** address terms — these are often tested!

# References
