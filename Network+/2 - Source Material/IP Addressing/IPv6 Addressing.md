2025-04-15 21:25

Status:

Tags: [[Network+/2 - Source Material/IP Addressing/IP Addressing]], [[IPv6]]

# IPv6 Addressing

## IPv4 Address Exhaustion

IPv4 uses 32-bit addresses, which allows for approximately 4.3 billion unique addresses. Due to global internet growth and connected devices, **IPv4 address space is depleted**, leading to the adoption of IPv6.

## IPv6 Basics

- 128-bit addressing system
    
- Written in **hexadecimal**, divided into **8 blocks (hextets)** of **4 hex digits** each
    
- Total of **32 hexadecimal digits**
    
- Each hex digit represents 4 bits
    

### Hexadecimal Values:

- 0–9 = Decimal 0–9
    
- A–F = Decimal 10–15
    

## IPv6 Address Example

```
2018:0000:0000:0000:0000:0000:4815:54ae
```

### Shorthand Rules:

1. **Leading zeroes in any block can be omitted**
    
    ```
    2018:0:0:0:0:0:4815:54ae
    ```
    
2. **Double colon (::) can replace a single consecutive string of zero blocks**
    
    - Only **one** `::` can be used per address
        
    
    ```
    2018::4815:54ae
    ```
    

## Address Types

### Unicast

Used to identify a **single interface**.

- **Global Unicast**
    
    - Routable on the internet
        
    - Begins with `2000::/3` (range: `2000` to `3FFF`)
        
    - Similar to public IPv4 addresses
        
- **Link-Local**
    
    - Used for communication within a local segment only
        
    - Begins with `FE80::/10`
        
    - Required for most IPv6 communication, including routing neighbor discovery
        

### SLAAC – Stateless Address Autoconfiguration

Allows a device to configure its own IPv6 address without DHCP:

- Uses router advertisements
    
- Often combined with **EUI-64**
    

#### EUI-64 (Extended Unique Identifier)

- Device creates its own 64-bit interface ID using:
    
    - The device's MAC address
        
    - Inserts `FFFE` in the middle of the MAC address
        

### DHCPv6

- Like DHCP in IPv4
    
- Provides centralized configuration for IPv6 clients
    

### Multicast

- Sent to **multiple specific devices**
    
- Begins with `FF00::/8`
    

### Anycast

- One address shared by **multiple devices**, but data is delivered to the **nearest** one
    
- Useful for services like DNS
    

## Neighbor Discovery Protocol (NDP)

- IPv6 equivalent of ARP
    
- Uses ICMPv6 messages
    
- Resolves layer 3 (IPv6) to layer 2 (MAC) addresses
    
- Also used for:
    
    - Router discovery
        
    - Prefix discovery
        
    - Address resolution
        

# References