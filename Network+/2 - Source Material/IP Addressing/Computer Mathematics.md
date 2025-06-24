2025-04-15 17:06

Status:

Tags: [[Network+/3 - Tags/IP Addressing|IP Addressing]]

# Computer Mathematics

Understanding how to convert between **decimal** and **binary** is critical for working with IP addresses, subnetting, and networking fundamentals.

---

## Base-10 (Decimal)

- Used by humans
- Digits range from 0–9
- Each digit increases by powers of 10 (10⁰, 10¹, 10², ...)

### Example:
523 = (5 × 100) + (2 × 10) + (3 × 1)

---

## Base-2 (Binary)

- Used by computers
- Digits are limited to 0 and 1
- Each position increases by powers of 2 (2⁰, 2¹, 2², ...)

### Example:
1101 = (1×8) + (1×4) + (0×2) + (1×1) = 13

---

## Binary Conversion Example

Converting **150** to binary:

| 128 | 64 | 32 | 16 | 8  | 4  | 2  | 1  |
|-----|----|----|----|----|----|----|----|
|  1  |  0 |  0 |  1 |  0 |  1 |  1 |  0 |

Binary: `10010110`  
Decimal: `128 + 16 + 4 + 2 = 150`

---

## Quick Binary Bit Value Table (8-bit)

| Bit Position | 2ⁿ  | Decimal Value |
|--------------|-----|----------------|
| 7            | 2⁷  | 128            |
| 6            | 2⁶  | 64             |
| 5            | 2⁵  | 32             |
| 4            | 2⁴  | 16             |
| 3            | 2³  | 8              |
| 2            | 2²  | 4              |
| 1            | 2¹  | 2              |
| 0            | 2⁰  | 1              |

---

## Common Decimal-to-Binary Reference

| Decimal | Binary    |
|---------|-----------|
| 0       | 00000000  |
| 1       | 00000001  |
| 64      | 01000000  |
| 127     | 01111111  |
| 128     | 10000000  |
| 192     | 11000000  |
| 255     | 11111111  |

---

# References
