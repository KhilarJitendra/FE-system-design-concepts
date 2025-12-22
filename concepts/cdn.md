# CDN (Content Delivery Network) – Basics

A **CDN (Content Delivery Network)** is a network of **geographically distributed servers** that deliver content to users from the **nearest location**.

> **Bring content closer to users**

---

## Why CDN is Needed?

- Reduce latency
- Improve page load speed
- Reduce load on origin servers
- Handle high traffic spikes
- Improve availability and reliability

---

## How CDN Works

1. User requests a resource (image, CSS, JS, HTML)
2. Request is routed to the **nearest CDN edge server**
3. If content is cached (**cache hit**) → served immediately
4. If not cached (**cache miss**) → fetched from origin server
5. CDN stores the response for future requests

---

## CDN Architecture

User
↓
Nearest CDN Edge
↓ (on cache miss)
Origin Server

---

## What Content is Cached?

- Static assets (images, CSS, JS, fonts)
- Videos and media files
- API responses (in some cases)
- HTML pages (if allowed)

---

## CDN vs Origin Server

| Aspect | CDN | Origin Server |
|----|----|----|
| Location | Near user | Centralized |
| Latency | Low | Higher |
| Load | Reduced | Heavy |
| Scalability | High | Limited |

---

## CDN Cache Control

CDN caching is controlled using:
- `Cache-Control`
- `Expires`
- `ETag`
- `TTL`

Example:
```http
Cache-Control: public, max-age=3600
```



Interview Tip

“A CDN improves performance and scalability by serving cached content from geographically distributed edge servers, reducing latency and load on origin servers.”



