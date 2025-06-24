
2025-03-2623:30

Status:

Tags: [[Encapsulation and Decapsulation]]


# Ethernet Header

### Ethernet Header (Layer 2)

- **Destination MAC Address (48 bits)**  
  The MAC address of the intended recipient.

- **Source MAC Address (48 bits)**  
  The MAC address of the sender.

- **EtherType / Length (16 bits)**  
  - Indicates the protocol of the encapsulated data (e.g., 0x0800 for IPv4, 0x86DD for IPv6).
  - In older Ethernet formats, this field could also represent the length of the payload.

- **Payload (46–1500 bytes)**  
  The actual data being carried (e.g., IP packet, ARP, etc.).

- **Frame Check Sequence (FCS) (32 bits)**  
  A CRC value used for error detection at Layer 2.




# References