# Database Indexing

**Indexing** is a technique used to **speed up data retrieval** from a database.

Instead of scanning the entire table, the database uses an **index** to quickly locate the required data.

> **Index = Faster reads**

---

## Why Indexing is Needed?

- Improves query performance
- Reduces database load
- Enables fast search operations
- Essential for large datasets

Without indexes, databases perform **full table scans**.

---

## How Indexing Works

- Database creates a **separate data structure**
- Index stores:
  - Column value
  - Reference to actual row

When a query runs:
1. Database checks the index
2. Finds matching row location
3. Fetches data directly

---

## Simple Example

Without index:
- Database scans every row

With index:
- Database jumps directly to matching rows

Example query:
```sql
SELECT * FROM users WHERE email = 'user@example.com';
