# Denormalization (Basics)

**Denormalization** is the process of **intentionally adding redundant data** to a database to **improve read performance**.

> **Trade storage and write complexity for faster reads**

---

## Why Denormalization is Needed?

- Reduce expensive JOIN operations
- Improve read performance
- Optimize read-heavy systems
- Simplify query logic

Denormalization is commonly used when **reads are much more frequent than writes**.

---

## Normalization vs Denormalization

| Aspect | Normalization | Denormalization |
|----|--------------|----------------|
| Data duplication | ❌ No | ✅ Yes |
| Storage usage | Low | High |
| Read performance | Slower | Faster |
| Write complexity | Simple | Complex |
| Data consistency | Easy | Harder |

---

## How Denormalization Works

- Related data is stored together
- Duplicate fields are added
- Fewer tables or documents are queried

---

## Example

### Normalized Design
- Users table
- Orders table
- OrderItems table

Query requires multiple JOINs.

---

### Denormalized Design
- Orders contain:
  - User name
  - User email
  - Product details

Single query → faster read.

---

Think:

- “I’ll store the same information in multiple places so I don’t have to look it up again and again.”
