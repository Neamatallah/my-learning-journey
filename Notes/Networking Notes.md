#  Networking Notes

> A structured reference for the networking concepts I learn during my backend development journey.

---

## 01 — How the Internet Works

### Internet

The **Internet** is a global network that connects devices and allows them to communicate and exchange data.

It includes:

* Computers
* Smartphones
* Servers
* Routers
* Networks
* Cables and wireless connections

### Internet vs Web

* **Internet:** The infrastructure that connects devices and networks.
* **Web (World Wide Web):** A service that runs on top of the Internet and allows us to access websites and web applications.

> The Web is part of the Internet, not the Internet itself.

---

## 02 — Client & Server

### Client

A **Client** is a device or application that requests data or a service.

Examples:

* Web browser
* Mobile application
* Laptop

When I open a website, my browser acts as the Client.

### Server

A **Server** is a computer that provides data or services to Clients.

A server can store:

* Website files
* Application code
* Images
* Databases

### Client-Server Model

```text
Client
   |
   | Request
   ↓
Server
   |
   | Response
   ↓
Client
```

---

## 03 — Request & Response

### Request

A **Request** is a message sent by the Client to the Server asking for a resource or service.

Example:

```text
Client → Server

"Give me the homepage."
```

### Response

A **Response** is the Server's reply to the Client.

Example:

```text
Server → Client

"Here is the requested data."
```

Basic communication:

```text
Client
  │
  │ Request
  ▼
Server
  │
  │ Response
  ▼
Client
```

---

## 04 — IP Address

An **IP Address** is an address used to identify a device on a network and determine where data should be sent.

Example:

```text
192.168.1.10
```

Humans prefer names such as:

```text
google.com
```

while network communication ultimately uses IP addresses.

---

## 05 — Domain

A **Domain Name** is a human-readable name used to access a website.

Examples:

```text
google.com
github.com
youtube.com
```

Instead of remembering a numerical IP address, users can use an easy-to-remember domain name.

---

## 06 — DNS

**DNS (Domain Name System)** translates domain names into IP addresses.

```text
google.com
     ↓
    DNS
     ↓
IP Address
```

### Why DNS?

Without DNS, users would have to remember the IP address of every website they want to visit.

A simple analogy:

```text
Contact Name → Phone Number

Domain Name → IP Address
```

---

## 07 — Hosting

**Hosting** is a service that provides a place for a website or application to be stored and made available on the Internet.

A website generally needs:

```text
Domain
   +
Hosting
   ↓
Website available online
```

* **Domain:** The website's name.
* **Hosting:** The server/service where the website's files and application are stored.

---

## 08 — URL

**URL (Uniform Resource Locator)** is the complete address used to access a resource on the Internet.

Example:

```text
https://www.youtube.com/watch?v=123
```

### Main Components

```text
https://       → Protocol
youtube.com    → Domain
/watch         → Path
?v=123         → Parameter
```

---

## 09 — HTTP & HTTPS

**HTTP (HyperText Transfer Protocol)** is a protocol used for communication between a Client and a Web Server.

**HTTPS** is the secure version of HTTP, where communication is encrypted.

Basic flow:

```text
Client
   │
   │ HTTP/HTTPS Request
   ▼
Server
   │
   │ HTTP/HTTPS Response
   ▼
Client
```

### Common HTTP Status Codes

| Code  | Meaning                 |
| ----- | ----------------------- |
| `200` | OK / Request successful |
| `403` | Forbidden               |
| `404` | Not Found               |
| `500` | Internal Server Error   |

---



### Simplified Flow

```text
User
 ↓
Browser (Client)
 ↓
Domain
 ↓
DNS
 ↓
IP Address
 ↓
Server
 ↓
Request
 ↓
Response
 ↓
Web Page
```

---

## 📌 Key Concepts

```text
Internet  → Network connecting devices
Client    → Requests data/services
Server    → Provides data/services
Request   → Client asks for something
Response  → Server replies
IP        → Network address
Domain    → Human-readable website name
DNS       → Domain → IP
Hosting   → Where the website/application is stored
URL       → Complete resource address
HTTP      → Communication protocol for the Web
HTTPS     → Secure version of HTTP
```

---

