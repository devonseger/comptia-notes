# DHCP (Dynamic Host Configuration Protocol)

**Purpose:** Provides automatic IP address assignment to devices on a network, minimizing manual configuration and reducing errors.

---

## Key Concepts:

### Scope

- A defined range of IP addresses available for distribution by the DHCP server.
    

### DHCP Reservation

- Reserved IP addresses that are excluded from general assignment.
    
- Assigns a specific IP address to a particular device (based on MAC address), ensuring the device always receives the same static IP address automatically.
    

---

## DHCP Process (DORA)

- **Discover**: Client broadcasts a DHCP Discover message seeking a DHCP server.
    
- **Offer**: DHCP server responds with an IP address offer.
    
- **Request**: Client formally requests the offered IP address.
    
- **Acknowledge**: DHCP server confirms assignment by sending an acknowledgment message.
    

Remember: **DORA** (Discover → Offer → Request → Acknowledge)

---

## Lease Duration:

- **Home Networks:** Typically 24 hours.
    
- **Corporate Networks:** Usually set to 7 or 30 days, balancing network stability and efficient IP management.
    

---

## Information Provided by DHCP:

- IP Address
    
- Subnet Mask
    
- Default Gateway
    
- DNS Server(s)
    

---

## IP Address Assignment Types:

- **Dynamic Assignment:** DHCP server assigns addresses automatically from the scope.
    
- **Static Assignment (DHCP Reservation):** Manually specifies IP addresses for devices.
    

---

## DHCP Relay:

- Forwards DHCP messages between clients and servers that reside on different subnets or networks.
    
- Essential when the DHCP server is not located within the client's local subnet.
    

---

## IP Helper (UDP Broadcast Forwarding):

- Enables routers to forward UDP broadcasts (including DHCP messages) across network segments.
    
- Often used alongside DHCP Relay to enable DHCP functionality across different networks.
    
- Router configuration with a helper address is necessary to relay DHCP packets across segments.
    

---

## Protocol Information:

- DHCP operates using **UDP** (User Datagram Protocol).
    
- DHCP Server Port: UDP **67**
    
- DHCP Client Port: UDP **68**
    

---

## Additional Notes for Effective Study:

- Understanding the difference between DHCP Relay and IP Helper can clarify network design scenarios.
    
- Familiarize yourself with DHCP troubleshooting commands:
    
    - `ipconfig /release` and `ipconfig /renew` (Windows)
        
    - `dhclient -r` and `dhclient` (Linux)
        

---

## Summary:

Dynamic Host Configuration Protocol streamlines network administration by automating IP address allocation, simplifying network management, and minimizing configuration errors.