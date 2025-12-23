# Distributed File Systems

A **Distributed File System (DFS)** stores files **across multiple machines** but makes them appear as **one single file system** to the user or application.

> **Files are spread across many servers, but accessed like one system**

---

## Why Distributed File Systems are Needed?

- Store very large amounts of data
- Handle machine failures
- Scale storage easily
- Support multiple users and applications

Single machines have **storage and reliability limits** — DFS solves that.

---

## Big Picture First 🧠

Think of data storage like this:

- **Single file system** → One cupboard  
- **Distributed file system** → Many cupboards in different rooms, all connected  

You don’t care *where* the file is stored — the system finds it for you.

---

## How Distributed File Systems Work

1. Large files are split into **blocks**
2. Blocks are stored on **multiple machines**
3. Blocks are **replicated** for safety
4. Metadata keeps track of:
   - Where files are
   - Where blocks are stored

If one machine fails, data is still available.

---

## Key Features of Distributed File Systems

- **Scalability** → Add more machines easily
- **Fault tolerance** → Handles failures
- **High availability** → Data always accessible
- **Transparency** → Looks like one file system

---

## Common Distributed File Systems

### 1️⃣ HDFS (Hadoop Distributed File System)
- Designed for big data
- Optimized for large files
- Write once, read many

---

### 2️⃣ NFS (Network File System)
- Used in enterprise networks
- Shared file access over network

---

### 3️⃣ Ceph
- Modern distributed storage
- Used in cloud environments

---

### 4️⃣ Amazon S3 (Conceptually Similar)
- Object-based distributed storage
- Highly scalable and durable

---

## Distributed File System vs Local File System

| Aspect | Local File System | Distributed File System |
|----|-----------------|------------------------|
| Machines | One | Many |
| Scalability | Limited | High |
| Fault tolerance | Low | High |
| Data size | Small to medium | Very large |

---

## Challenges of Distributed File Systems

- Network latency
- Metadata management
- Consistency issues
- Operational complexity

---

## Distributed File Systems in System Design

Used in:
- Big data analytics
- Log storage
- Data lakes
- Cloud storage systems

Often combined with:
- Compute engines (Spark, Hadoop)
- Data processing pipelines

---

## Real-World Analogy

- **Local FS** → Files in one office cabinet  
- **Distributed FS** → Files spread across many offices with copies  

---

## Key Takeaways

- Distributed file systems store data across many machines
- Provide scalability and fault tolerance
- Hide complexity from users
- Essential for large-scale systems

---

## Interview Tip

> “A distributed file system stores data across multiple machines while presenting a single unified file system interface, enabling scalability and fault tolerance.”
