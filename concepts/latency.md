# Latency (Basics)

**Latency** is the **time delay** between a request being sent and the response being received.

In simple terms:
> **Latency = How long it takes for data to travel from client to server and back**

Latency is usually measured in **milliseconds (ms)**.

---

## Why Latency Matters?

- Impacts user experience
- Affects page load time
- Critical for real-time systems
- Directly affects system performance

Even small increases in latency can cause **slow applications**.

---

## Latency vs Bandwidth

| Term | Meaning |
|----|--------|
| Latency | Delay in data transfer |
| Bandwidth | Amount of data transferred |

👉 High bandwidth does **not** mean low latency.

---

## Types of Latency

### 1. Network Latency
Time taken for data to travel across the network.

Factors:
- Physical distance
- Routing hops
- Network congestion

---

### 2. Application Latency
Delay caused by:
- Backend processing
- Business logic execution
- API response time

---

### 3. Database Latency
Time taken to:
- Query database
- Fetch or update data

---

### 4. Disk Latency
Delay in reading or writing data to disk.

---

## Sources of Latency (End-to-End)

1. DNS lookup
2. TCP connection setup
3. TLS/SSL handshake
4. Server processing
5. Database queries
6. Response transfer

---

## Typical Latency Numbers (Approx)

| Operation | Latency |
|--------|---------|
| L1 Cache | ~1 ns |
| Memory access | ~100 ns |
| Disk (SSD) | ~100 µs |
| Network (same region) | ~10–50 ms |
| Network (cross region) | ~100–300 ms |

---

## How to Reduce Latency?

### Client Side
- Use CDN
- Cache assets
- Minimize JS/CSS
- Lazy loading

---

### Network Level
- Use geographically closer servers
- Reduce network hops
- HTTP/2 or HTTP/3

---

### Backend
- Optimize APIs
- Use caching (Redis)
- Async processing
- Reduce DB calls

---

### Database
- Indexing
- Query optimization
- Read replicas

---

## Latency in System Design

Latency is critical for:
- High traffic systems
- Real-time apps (chat, gaming)
- Financial systems
- Streaming platforms

---

## Latency vs Throughput

| Term | Meaning |
|----|--------|
| Latency | Time per request |
| Throughput | Requests per second |

A system can have:
- Low latency but low throughput
- High throughput but high latency

---

## Summary

| Concept | Meaning |
|------|--------|
| Latency | Request–response delay |
| Network latency | Travel time |
| Application latency | Processing delay |
| Database latency | Query delay |
| CDN | Reduces network latency |

---

## Interview Tip

> In system design interviews:
- Always discuss **latency bottlenecks**
- Mention **CDN, caching, and regional deployment**
