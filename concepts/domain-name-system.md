# DNS (Domain Name System)

DNS stands for **Domain Name System**.  
It is responsible for **translating human-readable domain names into IP addresses**.

👉 Humans remember names like `google.com`  
👉 Computers communicate using IP addresses like `142.250.195.14`

DNS acts like the **phonebook of the internet**.

---

## Why DNS is Needed?

- Humans cannot remember IP addresses easily
- IP addresses can change, domain names remain same
- DNS provides a **layer of abstraction** between name and IP

Without DNS, we would need to type IP addresses to access websites.

---

## Basic DNS Flow (High Level)

1. User types `www.google.com` in the browser
2. Browser asks DNS for the IP address
3. DNS returns the corresponding IP
4. Browser sends HTTP/HTTPS request to that IP
5. Server responds with data

---

## DNS Resolution Process (Step by Step)

1. **Browser Cache**
   - Checks if IP is already cached

2. **OS Cache**
   - Checks operating system DNS cache

3. **Recursive Resolver (ISP DNS)**
   - If not found locally, request goes to ISP DNS

4. **Root DNS Server**
   - Directs to the correct TLD server

5. **TLD Server**
   - `.com`, `.org`, `.net`, etc.
   - Points to authoritative server

6. **Authoritative DNS Server**
   - Returns the actual IP address

---

## Types of DNS Servers

### 1. Recursive DNS Resolver
- Provided by ISP or public DNS
- Handles full DNS lookup process

Examples:
- Google DNS (`8.8.8.8`)
- Cloudflare DNS (`1.1.1.1`)

---

### 2. Root DNS Server
- Top-level DNS servers
- Know where TLD servers are located

---

### 3. TLD (Top-Level Domain) Server
- Manages domain extensions
- Examples:
  - `.com`
  - `.org`
  - `.in`

---

### 4. Authoritative DNS Server
- Stores actual DNS records
- Final source of truth for a domain

---

## Common DNS Record Types

| Record | Purpose |
|-----|--------|
| A | Maps domain → IPv4 |
| AAAA | Maps domain → IPv6 |
| CNAME | Alias to another domain |
| MX | Mail server record |
| TXT | Verification & security |
| NS | Name server info |

---

## Example DNS Records

```txt
example.com      A      93.184.216.34
www.example.com  CNAME  example.com
example.com      MX     mail.example.com

```

#### What is DNS Caching?

DNS responses are cached to reduce lookup time and load.

Where caching happens:

- Browser

- OS

- ISP Resolver

- CDN
