# Caching (Basics)

**Caching** is a technique used to **store frequently accessed data in fast storage** so future requests can be served **quickly without recomputing or re-fetching** from the main source.

> **Serve data faster by storing it closer to the user**

---

## Why Caching is Needed?

- Reduce response time
- Reduce database load
- Improve scalability
- Lower infrastructure cost

---

## How Caching Works

1. Client requests data
2. System checks cache first
3. If data exists → return from cache (**cache hit**)
4. If not → fetch from database, store in cache (**cache miss**)

---

## Cache Hit vs Cache Miss

| Term | Meaning |
|----|------|
| Cache Hit | Data found in cache |
| Cache Miss | Data not found in cache |

Higher cache hit ratio = better performance.

---

## Where Caching is Used?

### 1. Client-Side Cache
- Browser cache
- Mobile app cache

---

### 2. Server-Side Cache
- In-memory caches (Redis, Memcached)
- Application-level caching

---

### 3. CDN Cache
- Caches static content close to users
- Images, CSS, JS, videos

---

## Cache Eviction Policies

- **LRU** (Least Recently Used)
- **LFU** (Least Frequently Used)
- **TTL** (Time to Live)

---

## Caching vs Database

| Aspect | Cache | Database |
|----|-----|---------|
| Speed | Very fast | Slower |
| Persistence | Usually in-memory | Persistent |
| Cost | Expensive per GB | Cheaper |

---

## Challenges of Caching

- Cache invalidation
- Stale data
- Consistency issues
- Memory limits

> “There are only two hard things in computer science: cache invalidation and naming things.”

---

## Caching in System Design

Common use cases:
- User sessions
- Product catalog
- API responses
- Configuration data

---

## Real-World Analogy

- Keeping frequently used items on your desk  
❌ Fetching from storage every time

---

## Key Takeaways

- Cache improves speed and scalability
- Reduces database load
- Needs proper eviction and invalidation strategy

---

## Interview Tip

> “Caching improves system performance by reducing latency and database load, but introduces challenges like cache invalidation and consistency.”



<img width="869" height="486" alt="Screenshot 2025-12-22 at 4 04 06 PM" src="https://github.com/user-attachments/assets/ef6fade5-f97e-49b4-a5cd-b02d3c400177" />








