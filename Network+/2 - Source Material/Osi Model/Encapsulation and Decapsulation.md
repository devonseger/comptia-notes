
2025-03-2623:02

Status:

Tags: [[Osi Model]]


# Encapsulation and Decapsulation

Encapsulation is the process of putting **headers (and trailers)** around data as it moves **down** the OSI layers (from Layer 7 to Layer 1).

---

As a user creates data and sends it over a network, they will enter it into a **Layer 7 application**. This data then has a **Layer 7 header** added, which contains metadata with parameters that correlate with the application.

The information is then passed down to **Layer 6 (Presentation Layer)**, where the metadata and data are encapsulated with a **Layer 6 header**. This header may include details about **data formatting, encryption, or compression**.

Next, at **Layer 5 (Session Layer)**, **session-related information** is added, such as session IDs or control mechanisms for establishing, maintaining, and terminating sessions between applications.

At **Layer 4 (Transport Layer)**, either [[TCP Headers]] or [[UDP Headers]] are added, containing information such as **source and destination port numbers, sequencing, and error-checking** (in the case of TCP). This allows the data to be reliably sent to the correct application on the receiving host.

The encapsulated data is then passed to **Layer 3 (Network Layer)**, where a [[IP Header]] with **source and destination IP addresses** is added. This enables **routing** the packet across networks.

**Layer 2 (Data Link Layer)** adds a **[[Ethernet Header]] and trailer**, which includes **MAC addresses and error detection** via a Frame Check Sequence (FCS). This prepares the data for transmission across a physical network segment.

Finally, at **Layer 1 (Physical Layer)**, the entire frame is converted into **bits** and transmitted over the physical medium (e.g., electrical signals over copper wire, light pulses over fiber, or radio waves for wireless).

This process is **reversed on the receiving end**, where each layer removes its corresponding header and processes the remaining data **up the stack** until it reaches the application.

Encapsulation Flow:

```
[DATA] → [Segment] → [Packet] → [Frame] → [Bits]
Layers:     7-5        4          3         2-1
```

### Decapsulation

The reverse of encapsulation — the process of **removing headers (and trailers)** as data moves **up** the OSI layers (from Layer 1 to Layer 7) on the receiving device.


### Protocol Data Unit (PDU)

A single unit of information transmitted at each layer of the OSI model. Often referred to as an "L# PDU" depending on the layer.

- [[Layer 1 - Physical]] = **Bits**
- [[Layer 2 - Data Link Layer (Switch Layer)]] = **Frames**
- [[Layer 3 - Network Layer]] = **Packets**
- [[Layer 4 - Transport Layer]] = **Segments** (TCP)
- [[Layer 4 - Transport Layer]] = **Datagrams** (UDP)
- [[Layer 5 - Session]], [[Layer 6 - Presentation Layer]], [[Layer 7 - Application Layer]] = **Data**

# References