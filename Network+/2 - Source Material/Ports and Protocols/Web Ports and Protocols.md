2025-03-31 15:00

Status:

Tags: [[Ports and Protocols]]

# Web Ports and Protocols

---

## Port 80 – HTTP

**Hypertext Transfer Protocol**  
An **application layer** protocol [[Layer 7 - Application Layer]] that enables plain-text communication between clients and servers.

- Not encrypted (data is readable in transit)
- Vulnerable to:
  - On-path attacks (Man-in-the-Middle)
  - Eavesdropping
  - Content tampering

---

## Port 443 – HTTPS

**Hypertext Transfer Protocol Secure**  
Adds a layer of encryption using **SSL/TLS** (Secure Sockets Layer / Transport Layer Security).

- Data is encrypted in transit
- Ensures:
  - **Confidentiality** – no one can read the data
  - **Integrity** – data hasn’t been altered
  - **Authentication** – verifies the server’s identity

---

## Key Differences

| Feature            | HTTP (Port 80)              | HTTPS (Port 443)             |
|--------------------|-----------------------------|------------------------------|
| Encryption         | ❌ None                      | ✅ SSL/TLS Encryption         |
| Security           | ❌ Vulnerable                | ✅ Secure                     |
| Use Cases          | Public content               | Sensitive data, logins       |
| SEO Ranking        | 🔽 Lower                     | 🔼 Preferred by search engines |
| Browser Indicator  | ⚠️ “Not secure”              | 🔒 Padlock in address bar     |

---

## SEO & Trust

- **Search engines** like Google prioritize **HTTPS websites** in search rankings
- Modern browsers warn users when visiting HTTP sites
- HTTPS is **essential for user trust**, especially for e-commerce or login pages

---

## Bonus Tip

- You can use tools like **SSL Labs' SSL Test** to check a website's HTTPS security configuration
- TLS 1.2 and 1.3 are current best practices for HTTPS

---

# References
