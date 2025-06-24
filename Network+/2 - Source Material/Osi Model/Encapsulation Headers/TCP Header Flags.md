
2025-03-2623:25

Status:

Tags: [[TCP Headers]]


# TCP Header Flags

### TCP Flags (Control Bits)

- **SYN** — Synchronize  
  Initiates a connection; used in the TCP 3-way handshake, along with ACK and FIN.

- **ACK** — Acknowledgment  
  Acknowledges received data or a connection request.

- **FIN** — Finish  
  Gracefully closes a connection.

- **RST** — Reset  
  Abruptly resets or refuses a connection.

- **PSH** — Push  
  Instructs the receiver to push the data to the application immediately.

- **URG** — Urgent  
  Marks data as urgent and prioritizes it over other data, can violate FIFO rules.

- **ECE** — ECN Echo  
  Indicates network congestion; part of Explicit Congestion Notification.

- **CWR** — Congestion Window Reduced  
  Used to acknowledge the ECE flag and notify sender has reduced its send rate.



# References