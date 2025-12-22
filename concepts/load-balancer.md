# Load Balancer (Basics)

A **Load Balancer** is a component that **distributes incoming traffic across multiple servers** to ensure no single server is overloaded.

> **Client → Load Balancer → Multiple Servers**

---

## Why Load Balancer is Needed?

- Prevent server overload
- Improve application availability
- Enable horizontal scaling
- Increase fault tolerance

Without a load balancer, all requests would go to a single server.

---

## How Load Balancer Works

1. Client sends a request
2. Load balancer receives the request
3. Load balancer selects a healthy server
4. Request is forwarded to that server
5. Response is sent back to the client

---

## Types of Load Balancers

### 1. Layer 4 Load Balancer (L4)

Works at the **transport layer**.

- Uses IP address and port
- Does not inspect request content
- Very fast

#### Examples
- TCP load balancer
- UDP load balancer

---

### 2. Layer 7 Load Balancer (L7)

Works at the **application layer**.

- Understands HTTP/HTTPS
- Routes based on URL, headers, cookies
- Supports advanced routing

#### Examples
- NGINX
- AWS Application Load Balancer

---

## Load Balancing Algorithms

### 1. Round Robin
- Requests are distributed sequentially

---

### 2. Least Connections
- Request goes to server with fewest active connections

---

### 3. IP Hash
- Client IP determines server selection
- Useful for session persistence

---

## Health Checks

Load balancers continuously:
- Monitor server health
- Remove unhealthy servers
- Add servers back when healthy

This ensures **high availability**.

---

## Load Balancer and Sessions

### Problem
- User session stored on one server
- Request goes to another server

### Solutions
- Sticky sessions
- Centralized session store (Redis)
- Stateless applications (preferred)

---

## Load Balancer in System Design

Load balancers are used with:
- Horizontal scaling
- Microservices
- High availability systems
- Cloud infrastructure

---

## Popular Load Balancers

- NGINX
- HAProxy
- AWS ELB / ALB / NLB
- Azure Load Balancer

---

## Load Balancer vs Reverse Proxy

> A load balancer is a **specialized reverse proxy** focused on traffic distribution.

---

## Key Takeaways

- Load balancer distributes traffic
- Enables horizontal scaling
- Improves reliability
- Removes single point of failure

---

## Interview Tip

> “Load balancers distribute traffic across multiple servers using algorithms like round-robin or least-connections and are critical for scalable, highly available systems.”
