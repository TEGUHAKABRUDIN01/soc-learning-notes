# MAC Address (Media Access Control Address)

## Overview

A **MAC Address (Media Access Control Address)** is a unique hardware identifier assigned to a **Network Interface Card (NIC)** by the manufacturer.

The MAC address is stored in the network adapter's firmware or ROM (Read-Only Memory) and is used to identify devices on a **Local Area Network (LAN)**.

In the **OSI Model**, the MAC Address operates at **Layer 2 (Data Link Layer)** and is commonly referred to as a **Physical Address**.

---

## MAC Address Format

A MAC address consists of:

- **48 bits (6 bytes)**
- **12 hexadecimal characters**
- Uses digits **0–9** and letters **A–F**

MAC addresses are commonly written in one of the following formats:

```text
00:1A:2B:3C:4D:5E
```

or

```text
00-1A-2B-3C-4D-5E
```

---

## MAC Address Structure

A MAC address is divided into two parts.

### 1. Organizationally Unique Identifier (OUI)

The **first 3 bytes (24 bits)** identify the manufacturer of the network interface card.

Example:

```text
00:1A:2B
```

---

### 2. Device Identifier

The **last 3 bytes (24 bits)** are assigned by the manufacturer and uniquely identify the network device.

Example:

```text
3C:4D:5E
```

---

## Example

```text
00:1A:2B:3C:4D:5E
│──────│ │──────│
  OUI      Device Identifier
```

---

## Characteristics

- Unique identifier for a network interface.
- Assigned by the hardware manufacturer.
- Operates at **OSI Layer 2 (Data Link Layer)**.
- Primarily used for communication within a Local Area Network (LAN).
- Also known as a **Physical Address** or **Hardware Address**.

---

## MAC Address vs IP Address

| Feature      | MAC Address                    | IP Address                           |
| ------------ | ------------------------------ | ------------------------------------ |
| Purpose      | Identifies a network interface | Identifies a device on a network     |
| Layer        | OSI Layer 2 (Data Link Layer)  | OSI Layer 3 (Network Layer)          |
| Assigned By  | Hardware manufacturer          | Network administrator or DHCP server |
| Address Type | Physical Address               | Logical Address                      |
| Example      | 00:1A:2B:3C:4D:5E              | 192.168.1.10                         |

---

## Summary

- A **MAC Address** is a unique hardware identifier assigned to a network interface.
- Every MAC Address consists of **48 bits (6 bytes)** represented by **12 hexadecimal characters**.
- The **first 3 bytes** identify the manufacturer (**OUI**).
- The **last 3 bytes** uniquely identify the device.
- MAC Addresses operate at the **Data Link Layer (Layer 2)** of the OSI Model and are mainly used for communication within a Local Area Network (LAN).
