2025-03-26 15:20

Status:  
Tags: [[Osi Model]]

# Layer 1 - Physical

The **Physical Layer** is the bottom of the OSI model. It’s where the actual **transmission of bits** across a network occurs. This includes the **electrical, optical, or radio signals** used to carry data.

---

### What Happens at Layer 1

- Data is always in the form of **bits** (1s and 0s)
- This layer defines:
  - Voltage levels
  - Cable types
  - Pin layouts
  - Transmission rates
  - Connector types
  - Physical topology

---

### Examples

- **Copper Wire**: Uses voltages to represent bits  
- **Fiber Optic**: Uses light to represent bits

---

### Ethernet Standards

- **TIA/EIA 568A/B**: Defines how to wire Ethernet cables (pinout standard)

---

### Network Transmission Methods

- **Asynchronous**  
  Uses start/stop bits to indicate when data is being sent.

- **Synchronous**  
  Uses a **reference clock** to sync the sender and receiver.

---

### Baseband vs Broadband

- **Broadband**  
  Divides bandwidth into multiple channels (e.g., cable TV — one wire, many channels)

- **Baseband**  
  Uses all available bandwidth for one signal at a time.  
  - Home Ethernet is baseband  
  - Uses **digital signaling** (no modulation)  
  - Requires synchronization (clocking) to avoid collisions  
  - Supports **full-duplex** or time-managed communication (via switching)

---

### Multiplexing Techniques

- **Time-Division Multiplexing (TDM)**  
  Each user gets a **fixed timeslot**. Think one TV shared by multiple people taking turns.

- **Statistical TDM (StatTDM)**  
  Timeslots are assigned **dynamically as needed**. If a slot is open, you can use it.

- **Frequency-Division Multiplexing (FDM)**  
  Divides the medium into multiple **frequency channels**.  
  Each session uses a unique frequency (like radio stations).

---

## Examples of Layer 1 Devices

### Physical Media

- **Ethernet Cable (Twisted Pair)**  
  - Cat5e, Cat6, etc.  
  - Transmits data via **electrical signals**  

- **Fiber Optic Cable**  
  - Uses **light** to transmit data  
  - Immune to **EMI (Electromagnetic Interference)**  
  - Great for long distances and high speeds  

- **Coaxial Cable**  
  - Used in cable internet and TV  
  - Shielded copper core to protect signal integrity

These are all considered **media** because they are physical pathways for signals.  
They don’t interpret data — they just **transmit bits**.

---

### Wireless Media (Still Layer 1)

- **Wi-Fi (IEEE 802.11)**  
  - Wireless LAN  
  - Uses radio waves (2.4 GHz, 5 GHz, 6 GHz)

- **Bluetooth**  
  - Short-range communication  
  - Used for devices like keyboards, mice, headsets

- **NFC (Near Field Communication)**  
  - Very short-range (a few centimeters)  
  - Common in mobile payments and key cards

Even though wireless, these technologies are Layer 1 because they handle **physical signal transmission** via radio frequencies.

---

# References
