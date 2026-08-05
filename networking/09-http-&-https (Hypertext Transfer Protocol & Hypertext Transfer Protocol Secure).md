# HTTP & HTTPS

## Overview

HTTP (Hypertext Transfer Protocol) and HTTPS (Hypertext Transfer Protocol Secure) are application layer protocols used to transfer data between a web browser and a web server.

The main difference is that HTTPS encrypts communication using SSL/TLS, making data transmission more secure.

---

# HTTP (Hypertext Transfer Protocol)

## Definition

HTTP (Hypertext Transfer Protocol) is a communication protocol used to exchange data between a web browser and a web server over the World Wide Web (WWW).

By default, HTTP uses **Port 80**.

---

## How HTTP Works

### Step 1 – User Enters a URL

The user opens a web browser and enters a website address.

Example:

```text
http://example.com
```

---

### Step 2 – DNS Resolution

The browser requests the IP address of the domain from a DNS server.

---

### Step 3 – HTTP Request

After obtaining the IP address, the browser sends an HTTP Request to the web server.

The request may ask for:

- HTML
- CSS
- JavaScript
- Images
- Videos
- Other web resources

---

### Step 4 – HTTP Response

The web server processes the request and returns an HTTP Response containing the requested resources.

---

### Step 5 – Display the Website

The browser renders the received content and displays the web page.

---

## HTTP Message

HTTP communication consists of two messages:

### HTTP Request

Sent from the client to the server.

Contains:

- URL
- HTTP Method
- Request Header
- Request Body (optional)

---

### HTTP Response

Sent from the server to the client.

Contains:

- HTTP Status Code
- Response Header
- Response Body

---

## HTTP Methods

| Method | Description                          |
| ------ | ------------------------------------ |
| GET    | Retrieve data from the server.       |
| POST   | Send new data to the server.         |
| PUT    | Replace an existing resource.        |
| PATCH  | Update part of an existing resource. |
| DELETE | Remove a resource.                   |

---

## HTTP Status Codes

### 1xx – Informational

The request has been received.

### 2xx – Success

| Code | Meaning    |
| ---- | ---------- |
| 200  | OK         |
| 201  | Created    |
| 204  | No Content |

### 3xx – Redirection

| Code | Meaning                    |
| ---- | -------------------------- |
| 301  | Moved Permanently          |
| 302  | Found (Temporary Redirect) |
| 307  | Temporary Redirect         |

### 4xx – Client Errors

| Code | Meaning      |
| ---- | ------------ |
| 400  | Bad Request  |
| 401  | Unauthorized |
| 403  | Forbidden    |
| 404  | Not Found    |

### 5xx – Server Errors

| Code | Meaning               |
| ---- | --------------------- |
| 500  | Internal Server Error |

---

## HTTP Headers

### Request Headers

Common request headers include:

- Authorization
- Content-Type
- Accept
- User-Agent

### Response Headers

Common response headers include:

- Content-Type
- Cache-Control
- Set-Cookie
- Access-Control-Allow-Origin (CORS)

---

# HTTPS (Hypertext Transfer Protocol Secure)

## Definition

HTTPS (Hypertext Transfer Protocol Secure) is the secure version of HTTP.

It encrypts communication between the client and the web server using **SSL/TLS**, protecting data from interception and modification during transmission.

By default, HTTPS uses **Port 443**.

---

## How HTTPS Works

### Step 1 – User Enters a Secure URL

The user opens a web browser and enters a secure website.

Example:

```text
https://example.com
```

---

### Step 2 – DNS Resolution

The browser obtains the server's IP address using DNS.

---

### Step 3 – TLS Handshake

Before any HTTP data is exchanged, the browser and the web server perform a **TLS Handshake**.

During this process:

- The server presents its SSL/TLS certificate.
- The browser verifies the certificate.
- A secure encrypted session is established.

---

### Step 4 – Secure HTTP Request

The browser sends an HTTP Request through the encrypted TLS connection.

---

### Step 5 – Secure HTTP Response

The server returns an encrypted HTTP Response.

---

### Step 6 – Display the Website

The browser decrypts the response and displays the web page.

---

## Why HTTPS Is More Secure

HTTPS provides three important security features:

### Encryption

Protects data from being read by unauthorized parties during transmission.

### Authentication

Verifies that the client is communicating with the legitimate server using a digital certificate.

### Integrity

Ensures that transmitted data has not been modified during communication.

---

## HTTP vs HTTPS

| Feature        | HTTP    | HTTPS    |
| -------------- | ------- | -------- |
| Default Port   | 80      | 443      |
| Encryption     | ❌      | ✅       |
| SSL/TLS        | ❌      | ✅       |
| Authentication | ❌      | ✅       |
| Data Integrity | ❌      | ✅       |
| Security       | Low     | High     |
| URL Prefix     | http:// | https:// |

---

## Key Takeaways

- HTTP transfers data without encryption.
- HTTPS uses SSL/TLS to encrypt communication.
- HTTPS protects against eavesdropping and data tampering.
- Modern websites should always use HTTPS to ensure secure communication.
