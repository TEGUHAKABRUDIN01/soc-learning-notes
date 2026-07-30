# IP Address (Internet Protocol Address)

## Overview

An IP Address (Internet Protocol Address) is a unique logical address assigned to a device on a network. It enables devices such as computers, smartphones, printers, and servers to communicate with each other over a network.

---

## Types of IP Address

### 1. IPv4 (Internet Protocol Version 4)

IPv4 is the fourth version of the Internet Protocol and is the most widely used addressing system today.

**Characteristics:**

- 32-bit address length.
- Consists of **four octets** separated by periods (`.`).
- Each octet ranges from **0 to 255**.
- Supports approximately **4.3 billion unique addresses**.

**Example:**

```text
192.168.1.10
```

**IPv4 Address Range:**

```text
0.0.0.0 – 255.255.255.255
```

---

### 2. IPv6 (Internet Protocol Version 6)

IPv6 was developed to overcome the address limitations of IPv4.

**Characteristics:**

- 128-bit address length.
- Consists of **eight groups** of hexadecimal numbers separated by colons (`:`).
- Uses digits **0–9** and letters **A–F**.

**Example:**

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Shortened format:

```text
2001:db8:85a3::8a2e:370:7334
```

---

## IPv4 Address Classes

| Class | First Octet Range | Default Subnet Mask | Purpose |
|--------|-------------------|---------------------|---------|
| A | 1 – 126 | 255.0.0.0 | Large networks |
| B | 128 – 191 | 255.255.0.0 | Medium networks |
| C | 192 – 223 | 255.255.255.0 | Small networks |
| D | 224 – 239 | N/A | Multicast |
| E | 240 – 255 | N/A | Experimental |

> **Note:** The `127.x.x.x` range is reserved for **Loopback**, and `0.x.x.x` is reserved for network identification.

---

## Private IP Address

Private IP addresses are used within local networks and are **not routable on the public Internet**.

| Class | Private IP Range |
|--------|------------------|
| A | 10.0.0.0 – 10.255.255.255 |
| B | 172.16.0.0 – 172.31.255.255 |
| C | 192.168.0.0 – 192.168.255.255 |

Private IP addresses are commonly assigned automatically by a **DHCP Server**.

---

## Public IP Address

A Public IP Address is a globally unique address assigned by an Internet Service Provider (ISP).

It allows a device or network to communicate over the Internet.

---

## IPv4 vs IPv6

| Feature | IPv4 | IPv6 |
|---------|------|------|
| Address Length | 32-bit | 128-bit |
| Format | Decimal | Hexadecimal |
| Address Example | 192.168.1.10 | 2001:db8::1 |
| Number of Addresses | ~4.3 Billion | 340 Undecillion |

---

# IPv4 Subnetting

## Overview

Subnetting is the process of dividing a large network into smaller subnetworks (subnets). This improves network organization, efficiency, and management.

---

## Example

**Network Address**

```text
192.168.1.0/26
```

**Subnet Mask**

```text
255.255.255.192
```

---

## Step 1 – Number of Subnets

Formula:

```text
2^n
```

Where:

- **n** = Number of borrowed bits

Example:

```text
2² = 4 Subnets
```

---

## Step 2 – Number of Hosts per Subnet

Formula:

```text
2^h - 2
```

Where:

- **h** = Number of host bits

Example:

```text
2⁶ - 2

64 - 2

62 Hosts
```

---

## Step 3 – Block Size

Formula:

```text
256 - Last Octet of Subnet Mask
```

Example:

```text
256 - 192

64
```

Subnet increments:

```text
0
64
128
192
```

---

## Step 4 – Network, Host, and Broadcast Addresses

| Network Address | Valid Host Range | Broadcast Address |
|-----------------|------------------|-------------------|
| 192.168.1.0 | 192.168.1.1 – 192.168.1.62 | 192.168.1.63 |
| 192.168.1.64 | 192.168.1.65 – 192.168.1.126 | 192.168.1.127 |
| 192.168.1.128 | 192.168.1.129 – 192.168.1.190 | 192.168.1.191 |
| 192.168.1.192 | 192.168.1.193 – 192.168.1.254 | 192.168.1.255 |

---

## Common Networking Terms

| Term | Description |
|------|-------------|
| **IP Address** | A unique logical address assigned to a network device. |
| **Subnet Mask** | Separates the network and host portions of an IP address. |
| **Default Gateway** | The router used to communicate with other networks. |
| **Network Address** | Identifies a subnet and cannot be assigned to a host. |
| **Broadcast Address** | Used to send data to all devices within a subnet. |

---

## Summary

- **IPv4** uses a **32-bit** address and is the most widely used IP version.
- **IPv6** uses a **128-bit** address and provides a much larger address space.
- **Private IP Addresses** are used within local networks.
- **Public IP Addresses** are assigned by an ISP for Internet communication.
- **Subnetting** divides a network into smaller subnets for better organization and efficient IP address allocation.
- Every subnet has a **Network Address**, **Valid Host Range**, and **Broadcast Address**.