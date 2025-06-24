2025-03-31 22:11

Status:

Tags: [[Ports and Protocols]]

# File Transfer Ports and Protocols

**File transfer protocols** are specialized rules and procedures used to transmit files across networks. They operate on designated ports and act as doorways for file-related data exchanges.

---

## File Transfer Protocol (FTP)

- Used for transferring files between a **client and server**
- Operates in **plaintext** (not secure)
- Uses two ports:
  - **Port 20** – Data transfer
  - **Port 21** – Control/command communication

---

## Secure File Transfer Protocol / SSH File Transfer Protocol (SFTP)

- A secure alternative to FTP
- Operates over **port 22**
- Tunnels file transfers through an **SSH (Secure Shell)** connection
- **Note:** SFTP is **not the same** as FTP over SSH; it is a **separate protocol** that uses SSH as the transport layer

---

## Trivial File Transfer Protocol (TFTP)

- Operates over **port 69**
- Very lightweight and simple protocol
- Typically used for:
  - Bootstrapping network devices
  - Transferring config files or firmware
- **No authentication or encryption**
- Intended for **trusted environments** (e.g., local networks)

---

## Server Message Block (SMB)

- Operates over **port 445**
- Primarily used in **Windows environments**
- Allows applications to:
  - Read/write files on a remote system
  - Share printers and other resources
- Meant for use **within a LAN**  
  - Not secure enough for direct internet exposure

---

## Summary

- **FTP** – Basic file transfer, insecure (Ports 20 & 21)
- **SFTP** – Secure file transfer over SSH (Port 22)
- **TFTP** – Simplified, insecure file transfer with minimal features (Port 69)
- **SMB** – File sharing within local networks, mainly for Windows (Port 445)

---

## Quick Reference Table

| Protocol | Use Case                | Port(s)  | Secure? | Notes                          |
|----------|-------------------------|----------|---------|--------------------------------|
| FTP      | Standard file transfer  | 20, 21   | ❌      | Plaintext; not recommended for sensitive data |
| SFTP     | Secure file transfer    | 22       | ✅      | Uses SSH, completely encrypted |
| TFTP     | Lightweight file transfer | 69     | ❌      | No auth/encryption; internal use only |
| SMB      | LAN file sharing (Windows) | 445   | ⚠️      | Use within LAN; vulnerable over internet |

---

# References
