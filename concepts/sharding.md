# Sharding

**Sharding** is a technique used to **split large datasets into smaller parts** and distribute them across **multiple databases or servers**.

Each part is called a **shard**.

> **Split the data, not copy it**

---

## Why Sharding is Needed?

- Handle very large datasets
- Improve write performance
- Scale databases horizontally
- Avoid single database bottlenecks

Replication alone cannot solve data size problems — sharding can.

---

## How Sharding Works

1. Data is divided based on a **shard key**
2. Each shard stores a subset of data
3. Queries are routed to the correct shard
4. All shards together form the complete dataset

---

## Example

Users table:
- Users with ID 1–1,000 → Shard 1
- Users with ID 1,001–2,000 → Shard 2

Each shard stores **different users**.

---

## Shard Key

A **shard key** determines how data is distributed.

### Good shard key characteristics:
- Even data distribution
- Frequently used in queries
- Avoids hot spots

Examples:
- User ID
- Customer ID

---

## Types of Sharding

### 1. Range-Based Sharding
- Data split by value ranges
- Example: User ID ranges

⚠️ Risk of uneven load

---

### 2. Hash-Based Sharding
- Hash function decides shard
- More uniform distribution

---

### 3. Directory-Based Sharding
- Lookup table maps data to shards
- Flexible but complex

---

## Sharding vs Replication

| Aspect | Sharding | Replication |
|----|--------|------------|
| Purpose | Scalability | Availability |
| Data | Split | Copied |
| Writes | Distributed | Centralized |
| Complexity | High | Medium |

---

## Challenges of Sharding

- Complex queries (joins across shards)
- Rebalancing shards
- Data migration
- Operational complexity

---

## Sharding in System Design

Sharding is used in:
- Large-scale databases
- Social media platforms
- E-commerce systems
- Big data applications

---

## Real-World Analogy

- Dividing books across multiple libraries  
❌ Not making copies of the same book

---

## Real-World Example

- An e-commerce app stores orders in different databases based on region (India orders in DB-India,
US orders in DB-US) to handle high traffic and scale faster.

---

## Key Takeaways

- Sharding splits data across servers
- Enables horizontal database scaling
- Requires careful shard key selection
- Adds system complexity

---

## Interview Tip

> “Sharding enables horizontal scalability by distributing data across multiple databases, but increases complexity in queries and data management.”
