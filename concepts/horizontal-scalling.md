# Horizontal Scaling

**Horizontal Scaling** means **adding more machines (servers)** to handle increased load instead of upgrading a single machine.

> **More servers, not a bigger server**

---

## What is Horizontal Scaling?

Horizontal scaling is achieved by:
- Adding multiple servers
- Distributing traffic across them
- Running the same application on each server

All servers work **together as a system**.

---

## How Horizontal Scaling Works

1. Application starts with one server
2. Traffic increases
3. New servers are added
4. Load balancer distributes traffic
5. System handles more users

No single server handles all requests.

---

## Example

Initial setup:
- 1 server handling all requests

After horizontal scaling:
- Server 1
- Server 2
- Server 3

Traffic is distributed evenly across servers.

---

## When is Horizontal Scaling Used?

- High traffic applications
- Distributed systems
- Cloud-native systems
- Microservices architectures

---

## Advantages of Horizontal Scaling

- Almost unlimited scalability
- High availability
- Fault tolerance
- Better performance under heavy load

---

## Limitations of Horizontal Scaling

- More complex architecture
- Requires load balancers
- Data consistency challenges
- Needs distributed system design

---

## Horizontal Scaling vs Vertical Scaling

| Aspect | Horizontal Scaling | Vertical Scaling |
|----|------------------|----------------|
| Approach | Add more servers | Upgrade one server |
| Scalability | High | Limited |
| Complexity | High | Low |
| Fault Tolerance | High | Low |
| Downtime | Minimal | Possible |

---

## Horizontal Scaling in System Design

Horizontal scaling requires:
- Load balancer
- Stateless application design
- Distributed database or cache
- Monitoring and auto-scaling

---

## Real-World Analogy

- Hiring more people to do the same job  
❌ Not giving more work to one person

---

## Key Takeaways

- Horizontal scaling adds **more machines**
- Essential for large-scale systems
- Improves availability and reliability
- Core concept of distributed systems

---

## Interview Tip

> “Horizontal scaling improves scalability and availability by adding more servers, but it introduces complexity in load balancing and data consistency.”
