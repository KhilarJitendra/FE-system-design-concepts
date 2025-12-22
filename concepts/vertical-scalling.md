# Vertical Scaling (Basics)

**Vertical Scaling** means **increasing the capacity of a single machine** to handle more load.

Instead of adding more servers, you **upgrade the existing server** by increasing its resources.

---

## What is Vertical Scaling?

Vertical scaling is achieved by:
- Adding more **CPU**
- Adding more **RAM**
- Using faster **storage (SSD)**
- Upgrading network capacity

> **Same server, more power**

---

## How Vertical Scaling Works

1. Application runs on a single server
2. Traffic or data increases
3. Server becomes slow
4. Hardware resources are upgraded
5. Application performance improves

No architectural changes are required.

---

## Example

A server initially has:
- 4 GB RAM
- 2 CPU cores

After vertical scaling:
- 16 GB RAM
- 8 CPU cores

👉 The application continues to run on **the same server**.

---

## When is Vertical Scaling Used?

- Early-stage applications
- Small to medium traffic systems
- Monolithic applications
- Databases (initial phase)

---

## Advantages of Vertical Scaling

- Simple to implement
- No code changes required
- Easy to manage
- Faster performance improvement

---

## Limitations of Vertical Scaling

- Hardware has a maximum limit
- Expensive beyond a point
- Single point of failure
- Downtime may be required during upgrade

---

## Vertical Scaling vs Horizontal Scaling

| Aspect | Vertical Scaling | Horizontal Scaling |
|----|----------------|------------------|
| Approach | Upgrade one server | Add more servers |
| Complexity | Low | High |
| Scalability | Limited | High |
| Fault Tolerance | Low | High |
| Cost Growth | High | Gradual |

---

## Vertical Scaling in System Design

Vertical scaling is commonly:
- Used initially
- Combined later with horizontal scaling
- Avoided for high-availability systems

---

## Real-World Analogy

- Upgrading a computer’s RAM and CPU  
❌ Not buying multiple computers

---

## Key Takeaways

- Vertical scaling increases **power of a single machine**
- Easy but **not scalable long-term**
- Creates a **single point of failure**
- Best for **small or early-stage systems**

---

## Interview Tip

> “Vertical scaling improves system performance by upgrading a single server’s resources, but it has hardware limits and creates a single point of failure.”
