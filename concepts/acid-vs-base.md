# ACID vs BASE (Database Consistency Models)

Databases follow different **consistency models** to balance **reliability, availability, and scalability**.

Two common models are:
- **ACID** (used by SQL databases)
- **BASE** (used by many NoSQL databases)

---

## What is ACID?

**ACID** represents four properties that guarantee **reliable transactions**.

### 1. Atomicity
- Transaction is **all or nothing**
- If one step fails, entire transaction is rolled back

Example:
- Money transfer: debit + credit must both succeed

---

### 2. Consistency
- Database moves from one **valid state to another**
- Constraints, rules, and data integrity are maintained

---

### 3. Isolation
- Concurrent transactions do not interfere with each other
- Appears as if transactions run sequentially

---

### 4. Durability
- Once committed, data is **permanently stored**
- Survives crashes or power failures

---

## ACID Databases

Commonly used in:
- Banking systems
- E-commerce payments
- Inventory management

Examples:
- MySQL
- PostgreSQL
- Oracle

---

## What is BASE?

**BASE** is a model designed for **high availability and scalability**.

BASE stands for:

- **Basically Available**
- **Soft State**
- **Eventually Consistent**

---

### 1. Basically Available
- System remains available even during failures
- Some data may be stale

---

### 2. Soft State
- Data state may change over time
- No strict consistency at all times

---

### 3. Eventually Consistent
- System becomes consistent **after some time**
- Temporary inconsistencies are allowed

---

## BASE Databases

Commonly used in:
- Social media feeds
- Logging systems
- Recommendation engines

Examples:
- Cassandra
- DynamoDB
- MongoDB (eventual consistency)

---

## ACID vs BASE Comparison

| Aspect | ACID | BASE |
|----|-----|-----|
| Consistency | Strong | Eventual |
| Availability | Lower | High |
| Scalability | Limited | High |
| Transactions | Strict | Relaxed |
| Use Case | Financial systems | Large-scale systems |

---

## ACID, BASE

- ACID focuses on **Consistency**
- BASE focuses on **Availability**
- In distributed systems, trade-offs are unavoidable

---

## When to Use ACID?

- Financial transactions
- User payments
- Inventory systems
- Data integrity is critical

---

## When to Use BASE?

- Massive scale systems
- Real-time analytics
- User activity logs
- Slight inconsistency is acceptable

---

## Summary

| Model | Best For |
|----|--------|
| ACID | Strong correctness |
| BASE | High scalability |

---
