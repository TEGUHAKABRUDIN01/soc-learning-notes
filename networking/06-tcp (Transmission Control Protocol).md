# Transmission Control Protocol (TCP)

## Overview

Transmission Control Protocol (TCP) is a communication protocol that operates at **Layer 4 (Transport Layer)** of the TCP/IP model.

TCP provides **reliable, connection-oriented communication**, ensuring that data is delivered completely, in the correct order, and with minimal data loss through retransmission and acknowledgment mechanisms.

---

## Characteristics of TCP

- **Connection-Oriented** – A connection must be established before data transmission begins.
- **Reliable** – Ensures data is delivered successfully.
- **Ordered Delivery** – Delivers packets in the same order they were sent.
- **Error Detection** – Detects transmission errors using checksums.
- **Retransmission** – Resends lost or corrupted packets.
- **Flow Control** – Prevents the receiver from being overwhelmed with data.

---

## TCP Connection Establishment (Three-Way Handshake)

Before transmitting data, TCP establishes a connection using the **Three-Way Handshake**.

### Step 1 – SYN (Synchronize)

The client sends a **SYN** packet to the server, requesting to establish a connection.

```text
Client -----------------------> Server
              SYN
```

---

### Step 2 – SYN-ACK (Synchronize Acknowledgment)

The server acknowledges the request and responds with a **SYN-ACK** packet.

```text
Client <----------------------- Server
           SYN + ACK
```

---

### Step 3 – ACK (Acknowledgment)

The client sends an **ACK** packet to confirm the connection.

```text
Client -----------------------> Server
               ACK
```

After this step, the TCP connection is successfully established and data transmission can begin.

---

## TCP Connection Termination (Four-Way Handshake)

When communication is complete, TCP closes the connection using a **Four-Way Handshake**.

### Step 1 – FIN (Finish)

The client sends a **FIN** packet to indicate that it has finished sending data.

```text
Client -----------------------> Server
               FIN
```

---

### Step 2 – ACK (Acknowledgment)

The server acknowledges the client's FIN packet.

```text
Client <----------------------- Server
               ACK
```

---

### Step 3 – FIN (Finish)

After completing its own data transmission, the server sends a **FIN** packet.

```text
Client <----------------------- Server
               FIN
```

---

### Step 4 – ACK (Acknowledgment)

The client acknowledges the server's FIN packet.

```text
Client -----------------------> Server
               ACK
```

After this step, the TCP connection is closed.

---

## Common Protocols That Use TCP

| Protocol | Port | Purpose |
|----------|-----:|---------|
| HTTP | 80 | Web browsing |
| HTTPS | 443 | Secure web browsing |
| FTP | 20/21 | File transfer |
| SSH | 22 | Secure remote login |
| SMTP | 25 | Sending email |
| POP3 | 110 | Receiving email |
| IMAP | 143 | Accessing email |
| SMB | 445 | Windows file sharing |
| RDP | 3389 | Remote Desktop |

---

## Summary

| Feature | TCP |
|---------|-----|
| Layer | Transport Layer (Layer 4) |
| Connection Type | Connection-Oriented |
| Reliable Delivery | ✅ |
| Ordered Delivery | ✅ |
| Error Detection | ✅ |
| Retransmission | ✅ |
| Flow Control | ✅ |