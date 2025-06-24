
2025-06-2400:28

Status:

Tags: [[Security+/Tags/Fundamentals of Security|Fundamentals of Security]]


# Zero Trust

A modern security model based on the principle: **“Never trust, always verify.”**  
Zero Trust assumes no user or device—internal or external—should be inherently trusted.

---

### Core Principles

- **Verify Explicitly**  
    Every access request must be authenticated, authorized, and continuously validated using contextual data (e.g., identity, location, device health).
    
- **Use Least Privilege Access**  
    Limit users and systems to only the resources necessary for their role to reduce the attack surface.
    
- **Assume Breach**  
    Design the system with the mindset that breaches will occur and build containment, detection, and response accordingly.
    

---

### Key Components

- **Control Plane**  
    Defines and manages access policies within the Zero Trust framework.
    
    - **Adaptive Identity**  
        Uses contextual attributes (e.g., user behavior, device, location) to validate access dynamically.
        
    - **Threat Scope Reduction**  
        Minimizes the network attack surface by restricting access to only essential resources.
        
    - **Policy-Driven Access Control**  
        Access is governed by clearly defined policies aligned with user roles and responsibilities.
        
    - **Secured Zones**  
        Isolated network segments designed to protect sensitive data and critical assets.
        
- **Policy Engine**  
    Evaluates access requests by cross-referencing them against security policies.
    
- **Policy Administrator**  
    Responsible for creating, updating, and managing the access policies.
    
- **Subject/System**  
    The entity (user, device, application) requesting access to resources.
    
- **Policy Enforcement Point (PEP)**  
    The component that grants or denies access, acting as a gatekeeper at the point of entry.
    

---

### Data Plane

The **Data Plane** is responsible for the actual movement of data between systems, applications, and services after access is granted.

- Enforces access decisions made by the **Policy Engine**.
    
- Monitors live traffic for anomalous behavior (e.g., lateral movement, excessive access).
    
- Works closely with the **Policy Enforcement Point (PEP)** to restrict or allow data flows in real time.
    
- Can integrate with tools like **DLP (Data Loss Prevention)** and **NGFWs (Next-Gen Firewalls)** to protect sensitive information.
    

In Zero Trust, even data movement is closely monitored and segmented to ensure continuous protection and visibility.


# References