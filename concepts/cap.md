# CAP Theorem (Basics)

The **CAP Theorem** states that a **distributed system** can guarantee **only two out of the following three properties** at the same time:

- **Consistency (C)**
- **Availability (A)**
- **Partition Tolerance (P)**

You **cannot have all three together**.

---

## 1. Consistency (C)

Consistency means:
> Every read receives the **most recent write** or an error.

- All nodes see the same data at the same time
- No stale reads

### Example
If a user updates their email, every subsequent read should return the updated email.

---

## 2. Availability (A)

Availability means:
> Every request receives a **response**, even if it may not be the latest data.

- System is always responsive
- No request should fail

### Example
A social media feed loads even if some data is slightly outdated.

---

## 3. Partition Tolerance (P)

Partition tolerance means:
> The system continues to operate **despite network failures**.

- Network splits (partitions) are handled
- Some nodes may not be able to communicate

👉 In distributed systems, **partition tolerance is mandatory**.

---

## Why CAP Theorem Exists?

In real-world distributed systems:
- Network failures **will happen**
- You must choose between:
  - **Consistency**
  - **Availability**

---

## CAP Combinations

### 1. CP (Consistency + Partition Tolerance)

- System prioritizes consistency
- May reject requests during partition

#### Use Cases
- Banking systems
- Payment systems

#### Examples
- HBase
- MongoDB (CP by default)

---

### 2. AP (Availability + Partition Tolerance)

- System always responds
- Data may be temporarily inconsistent

#### Use Cases
- Social networks
- Recommendation systems

#### Examples
- Cassandra
- DynamoDB

---

### 3. CA (Consistency + Availability)

- Works only **when no partition occurs**
- Not realistic for distributed systems

👉 CA systems exist mainly in **single-node or non-distributed setups**.

---

## CAP Theorem Summary Table

| Model | Guarantees | Trade-off |
|----|------------|-----------|
| CP | C + P | Availability |
| AP | A + P | Consistency |
| CA | C + A | No partition tolerance |

---

## Real-World Example

### Example: Online Shopping App

You have two servers:

- Server A

- Server B

They suddenly lose network connection.

#### Option 1️⃣: Choose Consistency (CP)

App says:
❌ “Sorry, please try again later”

Why?

It wants to make sure data is 100% correct

No wrong orders allowed

📌 Used in:

- Bank transfers

- Payments


#### Option 2️⃣: Choose Availability (AP)

App still works

Shows data (may be slightly old)

Why?

User experience is more important

Temporary mismatch is acceptable

📌 Used in:

- Instagram likes

- Facebook feed


#### One-Line Memory Trick 🧠

When the network breaks, you must choose:

- ❌ Correct data

OR

- ✅ App always working

You can’t have both.

---

## Key Takeaways

- Partition tolerance is **non-negotiable**
- Choice is between **Consistency vs Availability**
- CAP applies only to **distributed systems**

---


