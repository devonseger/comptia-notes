
2025-03-2623:29

Status:

Tags: [[Encapsulation and Decapsulation]]


# IP Header

### IPv4 Header Fields

- **Version (4 bits)**  
  IP version (e.g., 4 for IPv4).

- **Header Length (IHL) (4 bits)**  
  Length of the IP header in 32-bit words.

- **Type of Service (ToS) / DSCP (8 bits)**  
  Specifies packet priority (Quality of Service).

- **Total Length (16 bits)**  
  Entire packet size (header + data), in bytes.

- **Identification (16 bits)**  
  Used to identify fragments of the original IP packet.

- **Flags (3 bits)**  
  Control flags for fragmentation (e.g., DF, MF).

- **Fragment Offset (13 bits)**  
  Indicates where in the datagram this fragment belongs.

- **Time to Live (TTL) (8 bits)**  
  Limits the packet's lifespan (hops allowed).

- **Protocol (8 bits)**  
  Indicates the protocol carried in the payload (e.g., TCP=6, UDP=17).

- **Header Checksum (16 bits)**  
  Error-checking for the IP header only.

- **Source IP Address (32 bits)**  
  IP address of the sender.

- **Destination IP Address (32 bits)**  
  IP address of the receiver.

- **Options (variable)**  
  Rarely used; for debugging, security, etc.

- **Padding (variable)**  
  Ensures the header ends on a 32-bit boundary.


# References