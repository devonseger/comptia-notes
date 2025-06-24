**Multicast Routing**

**Multicast** allows a sender to transmit traffic to **multiple receivers** using a **single stream**. The destination is a **Class D IP address** (`224.0.0.0 – 239.255.255.255`), known as a **multicast group**.

---

**IGMP – Internet Group Management Protocol**

Used by clients and routers to manage group membership for multicast traffic.

**IGMP Versions:**

- **IGMPv1**
    
    - Hosts request to join multicast groups
        
    - Routers query every 60 seconds to verify group membership
        
- **IGMPv2**
    
    - Clients can send a **Leave Group** message
        
    - Improves efficiency over v1 (reduces leave latency)
        
- **IGMPv3**
    
    - Supports **Source-Specific Multicast (SSM)**
        
    - Clients can request traffic only from specific sources
        
    - Useful for apps like streaming multiple video feeds over a single group
        

---

**PIM – Protocol Independent Multicast**

PIM routes multicast traffic **between routers**, forming distribution trees. It works alongside (but is not dependent on) unicast routing protocols.

**Modes of PIM:**

- **PIM Dense Mode (PIM-DM)**
    
    - Assumes all routers want multicast traffic
        
    - Uses **flood and prune** to build the tree
        
    - Best for small networks with many receivers
        
- **PIM Sparse Mode (PIM-SM)**
    
    - Assumes **few routers** need multicast
        
    - Builds a **shared tree** via a **Rendezvous Point (RP)**
        
    - Switches to **Shortest Path Tree (SPT)** for optimized paths
        

---

**Network+ Key Points:**

- Multicast uses **Class D IPs**
    
- **IGMP** = host-to-router group management
    
- **PIM** = router-to-router multicast routing
    
- Know the differences between **PIM-DM** (flood/prune) and **PIM-SM** (shared to shortest path)
    
- **IGMPv3** adds support for **SSM** (source-specific multicast)