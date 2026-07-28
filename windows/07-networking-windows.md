# Windows Networking Basics

## Overview

Windows Networking refers to the network configuration and services that allow a Windows computer to communicate with other devices and access resources on local networks or the Internet.

Understanding basic networking concepts is essential for configuring Windows systems and troubleshooting network connectivity.

---

## Common Networking Concepts

### 1. Dynamic Host Configuration Protocol (DHCP)

DHCP is a network service that automatically assigns IP configuration to devices connected to a network.

Instead of configuring an IP address manually, the DHCP server automatically provides:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

**Advantages:**

- Easy to manage.
- Reduces configuration errors.
- Automatically assigns available IP addresses.

---

### 2. Static IP Address

A Static IP Address is an IP configuration that is manually assigned by the user or administrator.

Unlike DHCP, the IP address does not change unless it is manually modified.

**Advantages:**

- Stable network address.
- Suitable for servers, printers, and network devices.
- Easier for remote access and network management.

---

### 3. Domain Name System (DNS)

The Domain Name System (DNS) translates human-readable domain names into IP addresses so computers can locate and communicate with websites and other network services.

For example:

```text
www.google.com
        │
        ▼
DNS Server
        │
        ▼
142.250.xxx.xxx
```

Without DNS, users would need to remember numerical IP addresses instead of domain names.

**Examples:**

- `www.google.com`
- `github.com`
- `openai.com`

---

## Comparison

| Feature | DHCP | Static IP |
|---------|-------|-----------|
| IP Assignment | Automatic | Manual |
| Easy to Configure | ✅ | ❌ |
| IP Address Changes | May change | Remains the same |
| Best Use Case | Client computers | Servers, printers, network devices |

---

## Summary

| Concept | Purpose |
|---------|---------|
| **DHCP** | Automatically assigns IP configuration to devices. |
| **Static IP** | Manually assigns a fixed IP address. |
| **DNS** | Translates domain names into IP addresses. |