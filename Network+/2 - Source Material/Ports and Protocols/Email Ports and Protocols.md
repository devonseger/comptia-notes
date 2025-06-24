2025-03-31 15:10

Status:

Tags: [[Ports and Protocols]]

# Email Ports and Protocols

---

## Simple Mail Transfer Protocol (SMTP)

- Used for **sending** outbound emails
- Operates over **port 25** (insecure, plaintext)
- **SMTPS** is not a separate protocol — it's SMTP over SSL/TLS:
  - **Port 465** – SMTP with implicit SSL
  - **Port 587** – SMTP with STARTTLS (preferred modern method)

---

## Post Office Protocol v3 (POP3)

- Used for **retrieving** emails from a remote server to a **local client**
- Operates over **port 110** (insecure)
- POP3 is **download-and-delete**: emails are stored locally and removed from the server
- **POP3S** (secure version):
  - Operates over **port 995**
  - Uses **SSL/TLS** for encryption

---

## Internet Message Access Protocol (IMAP)

- Used to **retrieve and manage** email directly on the server
- Operates over **port 143** (insecure)
- **IMAPS** (secure version):
  - Operates over **port 993**
  - Uses **SSL/TLS**
- IMAP keeps emails **synchronized** across multiple devices

---

## Summary

- **SMTP / SMTPS** → Outbound (sending) email  
- **POP3 / POP3S** → Inbound (receiving) email, local download  
- **IMAP / IMAPS** → Inbound (receiving) email, server-managed and synced

---

## Quick Reference Table

| Protocol | Purpose     | Port | Secure Version | Secure Port |
|----------|-------------|------|----------------|-------------|
| SMTP     | Send mail   | 25   | SMTPS          | 465 / 587   |
| POP3     | Retrieve mail (download) | 110  | POP3S          | 995         |
| IMAP     | Retrieve mail (sync)     | 143  | IMAPS          | 993         |

---

## Notes

- **Port 587 with STARTTLS** is the modern, recommended method for sending email securely.
- IMAP is preferred over POP3 for users accessing their mail from **multiple devices**.
- Many mail providers (like Gmail or Outlook) block or restrict port 25 due to spam concerns.

---

# References
