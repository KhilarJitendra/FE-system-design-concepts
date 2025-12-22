# Proxy Servers (Forward Proxy & Reverse Proxy)

A **proxy server** acts as an **intermediary** between a client and a server.  
It sits in between and **forwards requests and responses**.

Client ↔ Proxy ↔ Server

---

## Why Proxy is Needed?

- Security (hide client or server identity)
- Caching (improve performance)
- Access control
- Logging and monitoring
- Load balancing

---

## Forward Proxy

A **forward proxy** sits **in front of the client** and forwards client requests to the internet.

### Flow
Client → Forward Proxy → Internet Server

---

### Key Characteristics

- Represents the **client**
- Server does not know the real client
- Commonly used in corporate networks

---

### Use Cases

- Restrict access to certain websites
- Monitor employee internet usage
- Bypass geo-restrictions
- Cache external content

---

### Example

- Company network using proxy to access the internet
- VPN acting as a forward proxy

---

## Reverse Proxy

A **reverse proxy** sits **in front of servers** and handles requests from clients.

### Flow
Client → Reverse Proxy → Backend Server

---

### Key Characteristics

- Represents the **server**
- Client does not know which backend server is responding
- Widely used in production systems

---

### Use Cases

- Load balancing
- SSL termination
- Caching responses
- DDoS protection
- High availability

---

### Example

- NGINX
- HAProxy
- AWS Application Load Balancer
- Cloudflare

---

## Forward Proxy vs Reverse Proxy

| Aspect | Forward Proxy | Reverse Proxy |
|-----|-------------|--------------|
| Position | Client-side | Server-side |
| Represents | Client | Server |
| Hides | Client identity | Server details |
| Common Usage | Corporate networks, VPN | Web applications |
| Load Balancing | ❌ | ✅ |

---

## Proxy vs Load Balancer

> A **load balancer is a type of reverse proxy**.

| Feature | Proxy | Load Balancer |
|------|------|---------------|
| Intermediary | Yes | Yes |
| Distributes traffic | Sometimes | Always |
| Server awareness | Not required | Required |

---

## How Proxy Works with DNS

1. DNS resolves domain → proxy IP
2. Client sends request to proxy
3. Proxy forwards request to server
4. Response flows back via proxy

---

## Proxy in System Design

Proxy servers are used with:
- CDN
- Microservices
- API gateways
- Zero-trust security models

---

## Summary

| Term | Meaning |
|----|--------|
| Proxy | Intermediary server |
| Forward Proxy | Client-side proxy |
| Reverse Proxy | Server-side proxy |
| NGINX | Popular reverse proxy |
| VPN | Example of forward proxy |

---

## Interview Tip

> In interviews, remember:
- **Forward proxy hides the client**
- **Reverse proxy hides the server**
