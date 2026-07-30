# Common Network Ports

## Overview

A network port is a logical communication endpoint used by network protocols to send and receive data between devices.

Each network service uses a specific port number so that computers know which application or service should receive incoming network traffic.

For example, when you access a website using HTTPS, your computer communicates with the web server through **port 443**.

---

## Why Are Ports Important?

Network ports allow multiple services to run on the same computer without interfering with each other.

For example:

- A web server can use **Port 80**.
- An SSH server can use **Port 22**.
- A DNS server can use **Port 53**.

Each service listens on its assigned port.

---

## Common Network Ports

### Port 20/21 – FTP (File Transfer Protocol)

**Purpose:**

Used to transfer files between computers over a network.

- Port **20** – Data transfer.
- Port **21** – Command and control connection.

---

### Port 22 – SSH (Secure Shell)

**Purpose:**

Provides secure remote access to Linux and Unix systems.

SSH encrypts communication between the client and server.

---

### Port 25 – SMTP (Simple Mail Transfer Protocol)

**Purpose:**

Used to send email between mail servers or from an email client to a mail server.

---

### Port 53 – DNS (Domain Name System)

**Purpose:**

Translates domain names into IP addresses.

**Example:**

```text
www.google.com
        │
        ▼
DNS Server
        │
        ▼
142.250.xxx.xxx
```

---

### Port 67/68 – DHCP (Dynamic Host Configuration Protocol)

**Purpose:**

Automatically assigns network configuration to devices.

- Port **67** – DHCP Server
- Port **68** – DHCP Client

DHCP provides:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

---

### Port 80 – HTTP (Hypertext Transfer Protocol)

**Purpose:**

Transfers web pages without encryption.

Because data is sent in plain text, HTTP is generally replaced by HTTPS for secure communication.

---

### Port 110 – POP3 (Post Office Protocol Version 3)

**Purpose:**

Allows an email client to download email messages from a mail server.

Downloaded messages are often removed from the server.

---

### Port 143 – IMAP (Internet Message Access Protocol)

**Purpose:**

Allows users to access and manage email directly on the mail server.

Unlike POP3, emails remain stored on the server.

---

### Port 443 – HTTPS (Hypertext Transfer Protocol Secure)

**Purpose:**

Provides encrypted communication between a web browser and a web server using TLS/SSL.

HTTPS protects:

- Confidentiality
- Data integrity
- User privacy

---

### Port 445 – SMB (Server Message Block)

**Purpose:**

Provides file and printer sharing between Windows computers.

Commonly used for:

- Shared folders
- Network printers
- Windows file sharing

---

### Port 3389 – RDP (Remote Desktop Protocol)

**Purpose:**

Allows users to remotely access and control a Windows computer through a graphical interface.

---

## Additional Common Ports

### Port 23 – Telnet

**Purpose:**

Provides remote command-line access.

> **Note:** Telnet does **not** encrypt communication and has largely been replaced by SSH.

---

### Port 123 – NTP (Network Time Protocol)

**Purpose:**

Synchronizes the system clock between computers over a network.

---

### Port 161/162 – SNMP (Simple Network Management Protocol)

**Purpose:**

Used to monitor and manage network devices such as routers, switches, and printers.

- Port **161** – SNMP Queries
- Port **162** – SNMP Traps

---

## Common Ports Summary

| Port | Protocol | Purpose |
|------:|----------|---------|
| 20/21 | FTP | File transfer |
| 22 | SSH | Secure remote login |
| 23 | Telnet | Remote login (unencrypted) |
| 25 | SMTP | Send email |
| 53 | DNS | Domain name resolution |
| 67/68 | DHCP | Automatic IP configuration |
| 80 | HTTP | Unencrypted web traffic |
| 110 | POP3 | Download email |
| 123 | NTP | Time synchronization |
| 143 | IMAP | Access email on the server |
| 161/162 | SNMP | Network device management |
| 443 | HTTPS | Encrypted web traffic |
| 445 | SMB | Windows file sharing |
| 3389 | RDP | Remote Desktop |

---

## Key Points

- Every network service communicates through a specific port number.
- A computer can run multiple network services simultaneously because each service uses a different port.
- Some protocols, such as **SSH** and **HTTPS**, encrypt communication, while others, such as **Telnet** and **HTTP**, do not.
- Understanding common port numbers is essential for networking, troubleshooting, and system administration.