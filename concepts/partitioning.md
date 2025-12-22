# Partitioning (Basics)

**Partitioning** is the process of **dividing data into smaller logical parts** within the **same database or system** to improve **performance and manageability**.

> **Divide data logically, not physically across servers**

---

## Why Partitioning is Needed?

- Faster query performance
- Easier data management
- Efficient indexing
- Better maintenance (archiving, cleanup)

Partitioning helps even when you are using **a single database**.

---

## Partitioning vs Sharding (Important)

| Aspect | Partitioning | Sharding |
|----|------------|---------|
| Scope | Same database | Multiple databases |
| Data location | Same server | Different servers |
| Complexity | Low | High |
| Scaling | Vertical | Horizontal |

👉 **Sharding = Partitioning + Distribution**

---

## How Partitioning Works

1. Table is split into **partitions**
2. Each partition holds a subset of rows
3. Database decides which partition to query
4. Queries scan only relevant partitions

---

## Types of Partitioning

### 1. Range Partitioning

- Data split by value ranges

#### Example
- Orders before 2023 → Partition 1
- Orders after 2023 → Partition 2

---

### 2. List Partitioning

- Data split by specific values

#### Example
- Country = India → Partition A
- Country = USA → Partition B

---

### 3. Hash Partitioning

- Hash function decides partition
- Uniform distribution

#### Example
- `hash(user_id) % N`

---

### 4. Composite Partitioning

- Combination of multiple strategies
- Example: Range + Hash

---

## Partitioning in Databases

Commonly supported by:
- MySQL
- PostgreSQL
- Oracle
- SQL Server

---

## Real-World Analogy

- Files arranged into folders on the same computer  
❌ Not stored on multiple computers

---

## Benefits of Partitioning

- Improved query performance
- Reduced index size
- Faster data deletion
- Easier backups

---

## Limitations

- No horizontal scaling
- Still limited by single machine capacity
- Poor partition key causes imbalance

---

## Partitioning in System Design

Use partitioning when:
- Dataset is large
- Queries target specific ranges
- Sharding is not yet required

---

## Key Takeaways

- Partitioning splits data logically
- Happens within one database
- Improves performance and manageability
- Often used before sharding

---

## Interview Tip

> “Partitioning improves database performance by dividing data into logical segments within the same system, while sharding distributes data across multiple systems.”
