
2025-06-2418:40

Status:

Tags: [[Threat Actors]]


# Outsmarting Threat Actors
### Honeypots

Decoy systems or services intentionally designed to attract attackers. Often used to detect and analyze intrusion attempts.

- **Use case:** Detect insider threats (e.g., fraud, snooping)
    
- **Placement:** Within a screened subnet or isolated VLAN
    

### Honeynets

A full network of honeypots simulating real infrastructure (servers, routers, switches).

- **Benefit:** Rich data on attacker behaviors
    
- **Risk:** Could unintentionally inform attackers of real system configurations
    

### Honeyfiles

Fake files (e.g., `.docx`, `.xls`, `.db`, `.exe`) placed to lure attackers.

- **Goal:** Trigger alerts upon access
    

### Honeytokens

Useless but monitored data entries (e.g., bogus credentials, database entries, fake AWS keys).

- **Use case:** Detect unauthorized access, especially insider threats
    

---

## Additional Deception Methods

- **Bogus DNS Entries** – Fake subdomains or hosts monitored for DNS resolution attempts
    
- **Decoy Directories** – Monitored folders designed to catch unauthorized browsing
    
- **Dynamic Pages** – Auto-generated fake admin pages or dashboards
    
- **Port Triggering** – Keep sensitive ports closed until specific traffic triggers them open
    
- **Fake Telemetry Data** – Misleading system info (e.g., OS version, open ports) sent to attackers
    

---

## TTPs – Tactics, Techniques, and Procedures

Patterns of behavior and methodologies used by threat actors.

- Used in threat intelligence to attribute attacks and prepare defenses
    

---

## Deceptive & Disruption Technologies

Security tools designed to mislead, confuse, and deter attackers while detecting threats early.

# References