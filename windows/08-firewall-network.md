# Windows Firewall

## Overview

Windows Firewall is a built-in security feature that helps protect a computer by monitoring and filtering incoming and outgoing network traffic.

It prevents unauthorized access while allowing trusted network communication based on predefined firewall rules.

---

## Firewall Network Profiles

Windows Firewall uses different network profiles depending on the type of network the computer is connected to.

### 1. Domain Network

The **Domain** profile is used when the computer is connected to a corporate or organizational network managed by a Windows Active Directory domain.

**Characteristics:**

- Intended for enterprise environments.
- Managed by domain administrators.
- Uses centralized security policies.

---

### 2. Private Network

The **Private** profile is designed for trusted networks, such as home or office networks.

**Characteristics:**

- Allows trusted devices on the same network to communicate.
- Supports features such as file sharing and printer sharing.
- Provides protection while allowing more flexibility than the Public profile.

---

### 3. Public Network

The **Public** profile is intended for untrusted networks, such as public Wi-Fi in airports, hotels, coffee shops, or other public places.

**Characteristics:**

- Applies the most restrictive firewall rules.
- Blocks most unsolicited incoming connections.
- Reduces the risk of unauthorized access from other devices on the same network.

> **Recommendation:** Always keep the **Public** firewall profile enabled when connected to public Wi-Fi to help protect your computer from potential attacks.

---

## Comparison

| Network Profile | Environment | Security Level |
|-----------------|-------------|----------------|
| **Domain** | Organization or Active Directory domain | Medium (managed by administrators) |
| **Private** | Home or trusted office network | Medium |
| **Public** | Public Wi-Fi or untrusted networks | High |

---

## Summary

| Profile | Purpose |
|---------|---------|
| **Domain Network** | Protects computers connected to an Active Directory domain. |
| **Private Network** | Protects computers on trusted home or office networks. |
| **Public Network** | Provides the highest level of protection on untrusted public networks. |