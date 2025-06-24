2025-04-13 11:42

Status:

Tags: [[Ethernet Switching]]

# Network Access Control (NAC)

**NAC** is a security solution that controls how devices connect to and interact with a network. It ensures that **only authorized and compliant devices** can access network resources.

When a device attempts to connect, NAC:
- **Inspects the device**
- **Enforces policy**
- **Allows, quarantines, or denies access**

---

## 🔐 Port Security

- Restricts **physical switch ports** to specific **MAC addresses**
- Can:
  - Allow only known devices
  - Shut down port on violation
- Basic Layer 2 protection against **unauthorized access**

---

## 📛 MAC Filtering

- Filters devices based on their **unique MAC address**
- Can be implemented as:
  - **Allowlist** (more secure)
  - **Blocklist** (less secure)
- Often used on wireless routers or small networks

---

## 🔑 802.1X Authentication

- Provides **port-based network access control**
- Ensures only **authenticated users/devices** can connect

### Components:

| Term            | Role                                              |
|-----------------|---------------------------------------------------|
| **Supplicant**  | End-user device requesting access                 |
| **Authenticator** | Network device (e.g., switch or AP) acting as gatekeeper |
| **Authentication Server** | Validates user/device (often RADIUS server)        |

- Uses **EAP (Extensible Authentication Protocol)**
- Authenticator blocks all traffic **except 802.1X** until access is granted

---

## 🧳 BYOD (Bring Your Own Device)

- Uses a combination of:
  - **Port Security**
  - **MAC Filtering**
  - **802.1X**

### Agent Types:

- **Persistent Agent:** Installed on company devices permanently
- **Non-Persistent Agent:** Temporary; triggers **captive portal** to check device compliance

---

## ⏱️ Time-Based Access Control

- Grants network access **only during specific hours**
- Useful for:
  - Limiting access to business hours
  - Preventing after-hours unauthorized use

---

## 📍 Location-Based Access Control

- Uses **geolocation** to verify the device's physical location
- Enhances security by:
  - Blocking logins from unapproved regions
  - Requiring VPN or multi-factor authentication for remote access

---

## 🧑‍💼 Role-Based Access Control (RBAC)

- Access is based on the **user’s role** in the organization
- Example: HR vs. IT vs. Guest
- Enforces **least privilege** — users get only what they need

---

## 🧾 Rule-Based Access Control

- Uses **if/then logical statements**
- Can be:
  - Simple (e.g., deny guest access to file server)
  - Complex (e.g., allow access if device is compliant and time is within business hours)
- Highly customizable access policies

---

# References
