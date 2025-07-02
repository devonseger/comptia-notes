
2025-07-0213:33

Status:

Tags: [[Social Engineering]]


# Impersonation

**Impersonation** is a social engineering technique in which an attacker pretends to be someone they are not—such as a trusted individual, coworker, executive, or brand representative—in order to gain **unauthorized access** or extract **sensitive information**.

> The effectiveness of impersonation attacks often depends on **pretexting**—building a believable story or identity using collected details about the target or organization.

---

### Common Types of Impersonation

#### **1. General Impersonation**

- The attacker impersonates someone the target knows or would trust (e.g., IT support, a vendor, a manager).
    
- Often performed via:
    
    - Phone (vishing)
        
    - Email (phishing)
        
    - In-person (tailgating or physical access)
        

#### **2. Brand Impersonation**

- The attacker poses as a **legitimate company or brand**, using:
    
    - Realistic logos and branding
        
    - Spoofed email domains
        
    - Lookalike websites
        
- Goal: Trick the user into providing login credentials, financial information, or downloading malware.
    

#### **3. Typosquatting (URL Hijacking)**

- Attacker registers domain names that are **visually or typographically similar** to trusted domains:
    
    - Examples: `gooogle.com`, `micros0ft.com`, `amaz0n.net`
        
- May also include **subdomain spoofing** on trusted platforms (e.g., `support.azure.com.fake-domain.com`)
    
- **Defenses:**
    
    - Register common misspellings of your domain
        
    - Implement DNS monitoring
        
    - Conduct user training on verifying URLs
        

#### **4. Watering Hole Attacks**

- A **targeted attack** where the attacker compromises a legitimate website **frequently visited** by the target organization or group.
    
- The compromised site hosts **malicious code**, which infects visitors who trust and regularly use the site.
    
- Often used to compromise **business partners**, vendors, or industry-specific forums.
    

---

### Key Characteristics of Impersonation Attacks

- Use of **social cues** and urgency
    
- Crafting **believable scenarios**
    
- Leveraging **publicly available information** (social media, company websites, data breaches)
    
- Often combined with other tactics like phishing, baiting, or tailgating
    

---

### Mitigation Strategies

- **Security Awareness Training**  
    Teach employees how to recognize impersonation attempts and verify identities.
    
- **Domain Monitoring and Registration**  
    Monitor for typosquatted domains and register likely variants of your domain.
    
- **Multi-Factor Authentication (MFA)**  
    Prevent access even if credentials are stolen through impersonation.
    
- **Technical Controls**
    
    - Use **SPF, DKIM, and DMARC** to prevent email spoofing
        
    - Enforce HTTPS and use certificate pinning to detect fraudulent websites
        
- **Incident Response Protocols**  
    Define clear escalation procedures when impersonation is suspected.

# References