# Domain Name System (DNS)

**Purpose:**  
DNS translates human-readable hostnames (such as [www.example.com](http://www.example.com/)) into numerical IP addresses, enabling network clients to locate websites and services easily.

---

## Key Concepts:

### Fully Qualified Domain Name (FQDN)

- Represents the complete hierarchical name of a host or service in DNS.
    
- Format: `service.subdomain.domain.top-level-domain`
    
    - **Top-Level Domain (TLD):** `.com`, `.net`, `.org`, `.edu`, etc.
        
    - **Second-Level Domain (SLD):** Main domain, e.g., `example` in `example.com`
        
    - **Subdomain:** Prefixes added for organizational or functional separation, e.g., `mail`, `support`, `panel`
        

**Example:** `support.example.com`

### Host

- Refers specifically to a single machine or server within a domain.
    

---

## Uniform Resource Locator (URL)

- Combines the FQDN with a protocol specifying the method of access.
    
- Common URL formats:
    
    - HTTP: `http://www.example.com`
        
    - HTTPS: `https://www.example.com`
        
    - FTP: `ftp://files.example.com`
        

---

## Hosts File

- A simple local text file used to map hostnames to IP addresses.
    
- Serves as the first lookup point when a device initiates communication.
    
- If an IP address is found in the hosts file, DNS lookup is skipped.
    
- Relationship with DNS:
    
    - **Precedence:** Hosts file entries are prioritized over DNS lookups.
        
    - **Proximity:** Stored locally on each machine, enabling faster resolution.
        

**Typical File Location:**

- Windows: `C:\Windows\System32\drivers\etc\hosts`
    
- Linux/MacOS: `/etc/hosts`
    

**Example Entry:**

```
192.168.1.10   myserver.local
```

---

## DNS Operation (Simplified Steps):

1. Client initiates request for domain name.
    
2. Client checks local cache and hosts file.
    
3. If unresolved, client queries DNS resolver.
    
4. Resolver queries authoritative DNS servers.
    
5. Resolver returns IP address to client.
    

---

## DNS Record Types (Common):

- **A Record:** Maps domain names to IPv4 addresses.
    
- **AAAA Record:** Maps domain names to IPv6 addresses.
    
- **CNAME Record:** Alias pointing to another domain.
    
- **MX Record:** Specifies mail server for domain.
    
- **NS Record:** Lists authoritative DNS servers for a domain.
    

---

## Summary:

DNS is essential for user-friendly internet navigation, translating readable domain names to IP addresses, significantly improving network usability and accessibility.