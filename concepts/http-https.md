# HTTP / HTTPS (Basics)

**HTTP** stands for **HyperText Transfer Protocol**.  
It is the **application-layer protocol** used for communication between a **client (browser)** and a **server**.

---

## What is HTTP?

HTTP is a **request–response protocol**.

### Basic Flow
1. Client sends an HTTP request
2. Server processes the request
3. Server sends an HTTP response

HTTP works **on top of TCP**.

---

## HTTP Request Structure

An HTTP request contains:

```txt
GET /api/users HTTP/1.1
Host: example.com
Authorization: Bearer token
Content-Type: application/json
```

### Components

- Method (GET, POST, PUT, DELETE)

- URL / Path

- Headers

- Body (optional)

```txt
HTTP/1.1 200 OK
Content-Type: application/json

{ "status": "success" }
```

### Common HTTP Methods

| Method | Purpose        |
| ------ | -------------- |
| GET    | Fetch data     |
| POST   | Create data    |
| PUT    | Update data    |
| PATCH  | Partial update |
| DELETE | Remove data    |


### HTTP Status Codes

1xx – Informational

- 100 Continue

- 2xx – Success

- 200 OK

- 201 Created

3xx – Redirection

- 301 Moved Permanently

- 302 Found

4xx – Client Error

- 400 Bad Request

- 401 Unauthorized

- 403 Forbidden

- 404 Not Found

5xx – Server Error

- 500 Internal Server Error

- 502 Bad Gateway

- 503 Service Unavailable


### What is HTTPS?

- HTTPS is HTTP over SSL/TLS.
- It adds a security layer to HTTP.

👉 HTTPS = HTTP + Encryption + Authentication + Integrity

### Why HTTPS is Important?

- Encrypts data in transit

- Prevents man-in-the-middle attacks

- Ensures server authenticity

- Mandatory for modern browsers


### How HTTPS Works (High Level)

- Client initiates HTTPS request

- Server sends SSL certificate

- Client verifies certificate

- Secure key exchange happens

- Encrypted communication starts

### SSL / TLS Certificate

- Issued by Certificate Authority (CA)

- Verifies server identity

- Enables encrypted communication

Examples of CAs:

- Let’s Encrypt

- DigiCert

- GlobalSign

### HTTP is Stateless

HTTP does not remember previous requests.

To maintain state, systems use:

- Cookies

- Sessions

- JWT tokens
