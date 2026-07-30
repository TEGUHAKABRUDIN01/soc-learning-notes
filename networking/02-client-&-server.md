# Client and Server

## Overview

A client-server model is a network architecture in which one computer (the **server**) provides services or resources, while another computer (the **client**) requests and uses those services.

This model is one of the most common communication models used in modern computer networks.

---

## Server

A **server** is a computer or system that provides services, resources, or data to other devices on a network.

Servers are designed to receive requests from clients, process those requests, and send the appropriate responses.

**Common Services Provided by a Server:**

- File storage
- Web hosting
- Email services
- Database services
- Authentication services

**Examples:**

- Web Server
- File Server
- Database Server
- Mail Server
- DNS Server

---

## Client

A **client** is a computer, smartphone, or other device that requests services or resources from a server.

The client sends requests to the server and receives the requested information or service.

**Examples:**

- Desktop computer
- Laptop
- Smartphone
- Tablet
- Web browser

---

## How Client and Server Communicate

The communication process generally follows these steps:

1. The client sends a request to the server.
2. The server receives and processes the request.
3. The server sends a response back to the client.
4. The client displays or uses the received data.

**Example:**

```text
Client
   │
   │ Request (HTTPS)
   ▼
Server
   │
   │ Response (Web Page)
   ▼
Client
```

---

## Examples of Client-Server Communication

| Client                | Server         | Protocol         |
| --------------------- | -------------- | ---------------- |
| Web Browser           | Web Server     | HTTP / HTTPS     |
| Email Client          | Mail Server    | SMTP, POP3, IMAP |
| SSH Client            | Linux Server   | SSH              |
| Remote Desktop Client | Windows Server | RDP              |
| FTP Client            | FTP Server     | FTP              |

---

## Client vs Server

| Client                                | Server                                               |
| ------------------------------------- | ---------------------------------------------------- |
| Requests services or resources.       | Provides services or resources.                      |
| Initiates communication.              | Waits for and responds to client requests.           |
| Usually used by end users.            | Usually runs continuously to serve multiple clients. |
| Examples: Browser, Laptop, Smartphone | Examples: Web Server, File Server, Database Server   |

---

## Summary

- A **server** provides services, resources, or data to other devices on a network.
- A **client** requests and uses services provided by a server.
- Communication between clients and servers occurs using network protocols such as **HTTP**, **HTTPS**, **FTP**, and **SSH**.
- Most modern applications, including websites, email, cloud storage, and remote access, use the client-server model.
