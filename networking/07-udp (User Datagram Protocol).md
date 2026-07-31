# User Datagram Protocol (UDP)

## Overview

User Datagram Protocol (UDP) is a communication protocol that operates at **Layer 4 (Transport Layer)** of the TCP/IP model.

Unlike TCP, UDP is a **connectionless protocol**, meaning it does not establish a connection before transmitting data. UDP prioritizes speed over reliability, making it suitable for applications that require low latency.

Because UDP is connectionless, it:

- Does not guarantee packet delivery.
- Does not guarantee packet order.
- Does not retransmit lost packets.
- Does not use acknowledgments (ACK).

---

# UDP Characteristics

- **Connectionless** communication.
- Fast data transmission with low overhead.
- No packet retransmission.
- No acknowledgment (ACK).
- No packet ordering.
- Suitable for real-time communication.

---

# UDP Header

The UDP header has a fixed size of **8 bytes**.

Each port field is **16 bits**, allowing port numbers from **0 to 65535**.

| Field | Size | Description |
|--------|-----:|-------------|
| Source Port | 16 bits | Identifies the sender's port number. |
| Destination Port | 16 bits | Identifies the receiver's port number. |
| Length | 16 bits | Indicates the total length of the UDP header and data. |
| Checksum | 16 bits | Used for error detection. Optional in IPv4 and mandatory in IPv6. |

---

# UDP Header Structure

```text
0                15 16               31
+----------------+--------------------+
| Source Port    | Destination Port   |
+----------------+--------------------+
| Length         | Checksum           |
+----------------+--------------------+
|                Data                 |
+-------------------------------------+
```

---

# Common Protocols That Use UDP

| Protocol | Default Port | Purpose |
|----------|-------------:|---------|
| DHCP | 67/68 | Automatic IP address assignment |
| DNS | 53 | Domain name resolution |
| NTP | 123 | Time synchronization |
| RIP | 520 | Routing information exchange |
| VoIP | Varies | Voice communication over IP |

---

# Advantages

- Very fast communication.
- Low protocol overhead.
- Suitable for real-time applications.
- Efficient for broadcasting and multicasting.

---

# Disadvantages

- No guarantee that packets will arrive.
- No retransmission of lost packets.
- No guarantee of packet order.
- No built-in flow control or congestion control.

---

# TCP vs UDP

| Feature | TCP | UDP |
|---------|-----|-----|
| Connection Type | Connection-Oriented | Connectionless |
| Reliability | Reliable | Unreliable |
| Handshake | Three-Way Handshake | No Handshake |
| Acknowledgment (ACK) | Yes | No |
| Packet Ordering | Guaranteed | Not Guaranteed |
| Retransmission | Yes | No |
| Speed | Slower | Faster |
| Header Size | 20–60 Bytes | 8 Bytes |
| Error Recovery | Yes | No |
| Typical Applications | HTTP, HTTPS, SSH, FTP, SMTP | DNS, DHCP, VoIP, NTP, Streaming |

---

# Summary

- UDP operates at the **Transport Layer (Layer 4)**.
- UDP is **connectionless**, so it does not establish a connection before sending data.
- UDP prioritizes **speed** over **reliability**.
- The UDP header is only **8 bytes**, making it lightweight and efficient.
- UDP is commonly used by protocols such as **DNS**, **DHCP**, **NTP**, **RIP**, and **VoIP**.
- Applications that require low latency, such as voice calls, video streaming, and online gaming, commonly use UDP.