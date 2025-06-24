2025-04-01 14:06

Status:

Tags: [[Media and Connectors]]

# Building a Copper Cable

Creating Ethernet cables involves understanding connector types, wiring standards, and when to use specific cable types.

---

## Straight-Through Cable (Patch Cable)

- Same **pinout on both ends**
- Common for connecting:
  - **DTE → DCE** or **DCE → DTE**
- Most modern devices use this by default
- **568B** is the most commonly used standard (the one I use)

### T568B Color Order:
1. White/Orange  
2. Orange  
3. White/Green  
4. Blue  
5. White/Blue  
6. Green  
7. White/Brown  
8. Brown

### T568A Color Order (the one I don’t use):
1. White/Green  
2. Green  
3. White/Orange  
4. Blue  
5. White/Blue  
6. Orange  
7. White/Brown  
8. Brown

---

## Crossover Cable

- Used to connect similar device types (**DTE → DTE** or **DCE → DCE**)
- Swaps send/receive pairs between ends
- One end is wired as **568A**, the other as **568B**
- Example uses:
  - **Switch to switch**
  - **Computer to computer**
  - **Router to router**

⚠️ **Exam tip:**  
Assume you still need crossover cables for similar devices **unless the question mentions Auto-MDIX**.

---

## DTE vs. DCE

- **Data Terminal Equipment (DTE)**  
  - End-user devices like computers, servers  
  - “Made-up term,” but expect to see it on the exam

- **Data Communications Equipment (DCE)**  
  - Network gear like modems, switches, hubs, bridges  
  - Also a “made-up term,” but relevant for test purposes

---

## Medium Dependent Interface Crossover (MDIX)

- A feature that **automatically flips TX/RX pairs electronically**
- Allows **straight-through cables** to be used where a crossover is traditionally required
- Built into most modern switches and NICs

🧠 **For the exam:**  
> Assume the switch is **old** and does **not support Auto-MDIX** unless explicitly stated.

---

# References
