2025-04-10 20:55

Status:

Tags: [[Ethernet Switching]]

# Spanning Tree Protocol (802.1D)

**Spanning Tree Protocol (STP)** prevents **layer 2 loops** in Ethernet networks by selectively blocking redundant links. Without STP, redundant paths could cause **broadcast storms**, MAC address table instability, and degraded network performance.

---

## 🔄 Why Use STP?

- **Redundant links** are necessary for fault tolerance
- STP ensures there's **only one logical path** between switches
- Prevents:
  - **Broadcast storms**
  - **Multiple frame copies**
  - **MAC flapping**

---

## 📡 Broadcast Storm

Occurs when multiple switches forward the **same frame repeatedly** in a loop. This consumes bandwidth and crashes networks quickly.

---

## 🏛️ STP Roles

### Root Bridge

- **The central switch** in the STP topology
- Chosen based on **lowest Bridge ID (BID)**
- **BID = Priority + MAC address**
- All ports on the Root Bridge are in **designated** mode

> Lower BID = More likely to be elected as Root Bridge  
> (Lower MAC address wins in a tie)

---

### Non-Root Bridges

- Every other switch in the topology
- Must find the **shortest path to the Root Bridge**

---

## 🔌 Port Roles

### Root Port (RP)

- **One per non-root switch**
- Port with the **lowest total path cost** to the Root Bridge
- Used to forward traffic **toward** the Root Bridge

> 🔍 **Cost = based on link speed**, not physical cable type  
> (e.g., 100 Mbps copper = cost 19, 1 Gbps copper = cost 4)

### Designated Port (DP)

- **One per segment**
- Port on a switch that has the **best path** (lowest cost) to the Root Bridge **for that segment**
- Always **forwarding**

### Non-Designated Port (Blocked)

- **Blocked** to avoid loops
- Receives BPDUs but does not forward frames

---

## 🔄 STP Port States

1. **Blocking**  
   - Listens for BPDUs, does **not forward frames**

2. **Listening**  
   - Receives and sends BPDUs  
   - **Does not forward traffic or learn MACs**

3. **Learning**  
   - Begins learning MAC addresses  
   - Still not forwarding frames

4. **Forwarding**  
   - Fully operational  
   - **Forwards frames** and **learns MACs**

> Each state helps STP **prevent loops** while converging safely

---

## 📊 Link Speed vs STP Cost Table

| Link Speed         | STP Cost (Default) |
|--------------------|--------------------|
| 10 Mbps            | 100                |
| 100 Mbps           | 19                 |
| 1 Gbps             | 4                  |
| 10 Gbps            | 2                  |
| 100 Gbps           | 1                  |

> Lower cost = preferred path  
> Faster links = lower cost

---

## 🧠 Key Notes

- All ports on **Root Bridge** = Designated
- **Each segment** must have one Designated Port
- **Only one Root Port** per non-root switch
- STP **converges slowly** (~30–50 seconds), unless Rapid STP (802.1w) is used

---

# References
