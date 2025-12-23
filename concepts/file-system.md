# File Systems (NTFS, EXT, HDFS)

A **file system** defines **how data is stored, organized, accessed, and managed** on a storage device.

Different file systems are designed for **different use cases** such as local machines or distributed systems.

---

## Why File Systems are Needed?

- Organize data into files and directories
- Manage storage space efficiently
- Ensure data reliability and recovery
- Control access and permissions

---

## Types of File Systems (High Level)

- **Local File Systems** → Single machine
- **Distributed File Systems** → Multiple machines

---

## NTFS (New Technology File System)

**NTFS** is a **proprietary file system** developed by Microsoft and used in **Windows operating systems**.

---

### Key Features of NTFS

- Supports large files and disks
- File permissions and access control
- Journaling (crash recovery)
- Encryption and compression support

---

### Use Cases

- Windows desktops and servers
- Enterprise systems on Windows
- Local storage

---

### Limitations

- Not optimized for distributed systems
- Limited native support on Linux

---

## EXT File System (EXT4)

**EXT (Extended File System)** is the **most commonly used file system in Linux**.

EXT4 is the latest and most widely used version.

---

### Key Features of EXT4

- High performance
- Journaling support
- Handles large files and volumes
- Stable and reliable

---

### Use Cases

- Linux servers
- Cloud VMs
- Backend application servers

---

### Limitations

- Designed for single-machine usage
- Not suitable for massive distributed data

---

## HDFS (Hadoop Distributed File System)

**HDFS** is a **distributed file system** designed to store **very large datasets across multiple machines**.

> **Built for big data and fault tolerance**

---

### Key Features of HDFS

- Data is split into blocks
- Blocks are distributed across multiple nodes
- Data is replicated for fault tolerance
- Optimized for high-throughput access

---

### HDFS Architecture

- **NameNode**
  - Stores metadata
  - Knows where data blocks are stored

- **DataNodes**
  - Store actual data blocks

---

### How HDFS Works

1. Large file is split into blocks
2. Blocks are stored on multiple DataNodes
3. Each block is replicated
4. If a node fails, data is still available

---

### Use Cases

- Big data analytics
- Batch processing
- Data lakes
- Hadoop ecosystem

---

### Limitations

- Not suitable for low-latency reads
- Not ideal for small files
- Write-once, read-many model

---

## NTFS vs EXT vs HDFS

| Aspect | NTFS | EXT4 | HDFS |
|----|-----|-----|-----|
| System Type | Local | Local | Distributed |
| OS | Windows | Linux | Platform-independent |
| Scalability | Low | Low | Very High |
| Fault Tolerance | Medium | Medium | High |
| Best For | Desktop / Server | Linux servers | Big data systems |

---

## File Systems in System Design

- NTFS / EXT → Application servers, databases
- HDFS → Analytics, logs, batch jobs
- Often combined with:
  - Databases
  - Data warehouses
  - Processing engines

---

## Real-World Analogy

- **NTFS / EXT** → Files in one office cabinet  
- **HDFS** → Files spread across many offices with copies

---

## Key Takeaways

- File systems manage how data is stored
- NTFS and EXT are local file systems
- HDFS is designed for distributed, large-scale data
- Choose based on scale and access pattern

---

## Interview Tip

> “NTFS and EXT are local file systems optimized for single-machine storage, while HDFS is a distributed file system designed for fault-tolerant storage of massive datasets.”
