2025-03-26 22:32

Status:  
Tags: [[Osi Model]]

# Layer 5 - Session

The **Session Layer** is responsible for managing and maintaining connections between applications. It ensures that conversations between hosts stay **separate and organized**, preventing data streams from intermingling.

---

### Key Responsibilities

- **Set Up Session**
    
    - Checks user credentials and assigns unique session identifiers.
        
    - Prepares the session for communication.
        
- **Maintain Session**
    
    - Manages ongoing data exchange between devices.
        
        - Transfers data
            
        - Reestablishes connections as needed
            
        - Acknowledges receipt of communication
            
- **Tear Down Session**
    
    - Closes the session after communication is complete or if the connection is dropped.
        
        - May be timed out or closed explicitly by one or both parties
            

---

### Layer 5 Devices & Protocols

- **H.323**  
    Used to set up, maintain, and tear down **video and voice** sessions. Often works alongside the **Real-time Transport Protocol (RTP)**.
    
- **NetBIOS**  
    Enables applications on different computers to communicate over a LAN and supports **file and printer sharing**.
    

---

# References