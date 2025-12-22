# Replication

**Replication** is the process of **copying data from one database/server to one or more other servers** to improve **availability, reliability, and performance**.

> **Same data stored in multiple places**

---

## Why Replication is Needed?

- High availability
- Fault tolerance
- Improved read performance
- Disaster recovery

If one server fails, others can still serve requests.

---

## How Replication Works

1. **Primary (Leader) Server**
   - Handles write operations

2. **Replica (Follower) Servers**
   - Receive copied data from primary
   - Handle read operations

Writes → Primary  
Reads → Replicas

---

## Types of Replication

### 1. Master–Slave (Primary–Replica)

- One primary server handles writes
- Multiple replicas handle reads

#### Use Cases
- Read-heavy systems
- E-commerce product listing

---

### 2. Master–Master (Multi-Primary)

- Multiple servers can handle writes
- Data is synced between them

#### Challenges
- Conflict resolution
- Higher complexity

---

## Synchronous vs Asynchronous Replication

### Synchronous Replication
- Write is confirmed only after replicas update
- Strong consistency
- Higher latency

---

### Asynchronous Replication
- Primary confirms write immediately
- Replicas update later
- Eventual consistency

---

## Replication vs Sharding

| Aspect | Replication | Sharding |
|----|-----------|---------|
| Purpose | Availability | Scalability |
| Data | Same data | Split data |
| Reads | Faster | Distributed |
| Writes | Centralized | Distributed |

---

## Replication in System Design

Replication is commonly used with:
- Load balancers
- Read replicas
- High availability setups
- Disaster recovery strategies

---

## Real-World Analogy

- Keeping multiple copies of important files  
❌ Not splitting the file

---

## Key Takeaways

- Replication copies data
- Improves availability and fault tolerance
- Helps read scalability
- Can introduce consistency challenges

---

## Interview Tip

> “Replication improves availability and read performance by maintaining multiple copies of data, but requires trade-offs between consistency and latency.”
