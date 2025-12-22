# Database Overview (Basics)

A **database** is a structured system used to **store, manage, and retrieve data efficiently**.

In system design:
> **APIs interact with databases to persist application data**

---

## Why Databases are Needed?

- Persistent data storage
- Fast data retrieval
- Data consistency and integrity
- Support concurrent users

---

## Types of Databases (High Level)

### 1. Relational Databases (SQL)

Relational databases store data in **tables with rows and columns**.

#### Characteristics
- Fixed schema
- Strong consistency
- Uses SQL for queries
- Supports ACID properties

#### Examples
- MySQL
- PostgreSQL
- Oracle
- SQL Server

---

### 2. NoSQL Databases

NoSQL databases are designed for **scalability and flexibility**.

#### Characteristics
- Schema-less or flexible schema
- Horizontally scalable
- Handles large volumes of data

#### Types of NoSQL Databases

##### a) Key–Value Store
- Data stored as key–value pairs
- Example: Redis, DynamoDB

##### b) Document Store
- Stores JSON-like documents
- Example: MongoDB, CouchDB

##### c) Column Store
- Stores data in columns
- Example: Cassandra, HBase

##### d) Graph Database
- Stores relationships as graphs
- Example: Neo4j

---

## SQL vs NoSQL

| Aspect | SQL | NoSQL |
|-----|-----|------|
| Schema | Fixed | Flexible |
| Scalability | Vertical | Horizontal |
| Consistency | Strong | Eventual |
| Use Case | Transactions | Big data, scale |

---

