

2025-03-2623:24

Status:

Tags: [[Encapsulation and Decapsulation]]


# TCP Headers

### TCP Header Fields

- **Source Port (16 bits)**  
  Identifies the sending port.

- **Destination Port (16 bits)**  
  Identifies the receiving port.

- **Sequence Number (32 bits)**  
  Used to ensure data arrives in order.

- **Acknowledgment Number (32 bits)**  
  Indicates the next expected byte from the sender.

- **Data Offset (4 bits)**  
  Specifies the size of the TCP header.

- **Reserved (3 bits)**  
  Reserved for future use (usually set to 0).

- **Flags (9 bits)**  [[TCP Header Flags]]
  Control flags: URG, ACK, PSH, RST, SYN, FIN, ECE, CWR, NS.

- **Window Size (16 bits)**  
  Specifies the size of the sender’s receive window (flow control).

- **Checksum (16 bits)**  
  Used for error-checking the header and data.

- **Urgent Pointer (16 bits)**  
  Points to urgent data in the packet (used with URG flag).

- **Options (variable)**  
  Used for features like MSS, window scaling, etc.

- **Padding (variable)**  
  Ensures the header ends on a 32-bit boundary.



# References