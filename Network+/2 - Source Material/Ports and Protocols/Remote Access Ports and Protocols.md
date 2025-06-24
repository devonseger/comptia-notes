2025-03-31 22:21

Status:

Tags: [[Ports and Protocols]]

# Remote Access Ports and Protocols

Remote access protocols allow users to **build, manage, and interact with systems and networks remotely**, whether across the LAN or around the world.

---

## Secure Shell (SSH)

- Provides **secure remote login** and secure access to network services over untrusted networks
- Encrypts all communications (authentication, commands, output)
- Commonly used for:
  - Remote system administration (Linux/Unix)
  - Secure file transfers (SFTP, SCP)
- Operates over **port 22**

---

## Telnet

- Allows a user to remotely log into another computer on the same or different network
- Operates over **port 23**
- **No encryption** — all data (including login credentials) is transmitted in **plaintext**
- **Not secure** and **deprecated** — rarely used in modern environments except for testing/troubleshooting in isolated networks

---

## Remote Desktop Protocol (RDP)

- Developed by **Microsoft** for remote desktop access with a graphical interface
- Operates over **port 3389**
- Features:
  - **Encrypted communication**
  - **Smart card authentication**
  - **Bandwidth reduction** techniques for low-speed connections
- Commonly used in Windows environments for helpdesk, admin access, or remote work

---

## Summary

- **SSH** – Secure remote command-line access (Port 22)
- **Telnet** – Insecure command-line remote access (Port 23) — deprecated
- **RDP** – Secure remote graphical access (Port 3389)

---

## Quick Reference Table

| Protocol | Port  | Interface Type | Secure? | Common Use                      |
|----------|-------|----------------|---------|---------------------------------|
| SSH      | 22    | Command-line   | ✅ Yes  | Remote admin, file transfer     |
| Telnet   | 23    | Command-line   | ❌ No   | Legacy systems, testing only    |
| RDP      | 3389  | GUI            | ✅ Yes  | Windows remote desktop access   |

---

# References
