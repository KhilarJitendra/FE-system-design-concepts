# IP Addresses (Basics)

An **IP Address (Internet Protocol Address)** is a **unique identifier** assigned to a device on a network.  
It helps devices **locate and communicate with each other** over the internet or a local network.

---

## Why IP Address is Needed?

- To uniquely identify a device on a network
- To send and receive data between client and server
- Acts like a **home address** for devices on the internet

Without IP addresses, data would not know **where to go**.

---

## Types of IP Addresses

There are **two main versions** of IP addresses:

---

## IPv4 (Internet Protocol Version 4)

IPv4 is the **most widely used** IP version.

### Format
- 32-bit number
- Written as **four numbers separated by dots**
- Each number ranges from `0–255`

### Example

### Total Possible Addresses
- About **4.3 billion**
- Limited → led to the creation of IPv6

---

## IPv6 (Internet Protocol Version 6)

IPv6 was introduced to **solve IPv4 exhaustion**.

### Format
- 128-bit number
- Written in **hexadecimal** and separated by colons

### Example


### Advantages
- Practically unlimited addresses
- Better security and efficiency
- Built-in support for modern networking

---

## Public IP Address

A **public IP address** is assigned by your **ISP (Internet Service Provider)** and is **visible on the internet**.

### Characteristics
- Unique across the internet
- Used to identify your network globally

### Example


---

## Private IP Address

A **private IP address** is used **inside a local network** (home, office).

### Common Private IP Ranges (IPv4)

| Range | Usage |
|-----|------|
| 10.0.0.0 – 10.255.255.255 | Large networks |
| 172.16.0.0 – 172.31.255.255 | Medium networks |
| 192.168.0.0 – 192.168.255.255 | Home networks |

### Example


👉 Private IPs **cannot be accessed directly from the internet**.

---

## Static IP Address

A **static IP** does not change over time.

### Use Cases
- Servers
- Databases
- Hosting websites

### Pros
- Easy to locate
- Stable connections

### Cons
- More expensive
- Security risk if exposed

---

## Dynamic IP Address

A **dynamic IP** changes periodically and is assigned automatically.

### Use Cases
- Home users
- Mobile devices

### Pros
- Cost-effective
- More secure

### Cons
- IP keeps changing

---

## How IP Address Works in Client–Server Model

1. Client sends a request to a **server IP**
2. Request travels through the internet
3. Server processes the request
4. Response is sent back to the **client IP**

---

## Summary

| Term | Meaning |
|----|-------|
| IP Address | Unique identifier of a device |
| IPv4 | 32-bit address format |
| IPv6 | 128-bit address format |
| Public IP | Internet-facing IP |
| Private IP | Internal network IP |
| Static IP | Fixed IP |
| Dynamic IP | Changing IP |

---



