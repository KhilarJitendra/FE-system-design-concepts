# Client–Server Architecture (Basics)

Hi 👋  
In this file, I will explain **how client–server architecture works**, along with some **basic system design concepts** like thick client, thin client, and tier-based applications.

---

## What is Client–Server Architecture?

Client–server architecture is a model where:

- **Client** → Requests data or services  
- **Server** → Processes the request and sends back a response  

The client and server communicate over a network (usually the internet) using protocols like **HTTP/HTTPS**.

<img width="659" height="234" alt="Client Server Architecture" src="https://github.com/user-attachments/assets/b5fb4afe-8bf9-4f2c-83c6-9944150db88f" />

---

## (i) What is a Thick Client?

A **thick client** is an application where **most of the business logic and processing happens on the client side**.

### Characteristics
- Heavy client-side logic
- Less dependency on the server
- Can work partially offline
- More resource usage on the client machine

### Examples
- Microsoft Outlook (Desktop App)
- Video editing software (Premiere Pro, Final Cut)
- Desktop accounting software

---

## (ii) What is a Thin Client?

A **thin client** is an application where **most of the business logic happens on the backend (server)**, and the client mainly handles UI rendering and user interaction.

### Characteristics
- Minimal logic on client
- Highly dependent on backend APIs
- Easy to update and maintain
- Scales well for web applications

### Examples
- Netflix (Web App)
- Amazon (Web)
- Gmail (Web version)

---

## (iii) What is a Tier Application?

A **tier** represents a **logical separation of responsibilities** in an application architecture.

Common tiers:
- Presentation layer (UI)
- Business logic layer
- Data layer (Database)

---

## 2-Tier Application

In a **2-tier architecture**, the client communicates **directly with the database**.

### Structure
- Client (UI + Logic)
- Database

### Examples
- Desktop applications connected directly to a database
- Small internal tools

### Drawbacks
- Poor scalability
- Security risks
- Tight coupling

---

## 3-Tier Application

In a **3-tier architecture**, responsibilities are clearly separated.

<img width="954" height="498" alt="3 Tier Architecture" src="https://github.com/user-attachments/assets/2e112b8d-0683-4e26-8d7f-61108c79b76d" />

### Structure
1. **Presentation Layer (Client)**
   - Browser / Mobile App
   - React, Next.js, Angular

2. **Application Layer (Backend)**
   - Business logic
   - APIs (Node.js, Java, Python)

3. **Data Layer**
   - Databases (MySQL, PostgreSQL, MongoDB)

### Advantages
- Better scalability
- Improved security
- Easier maintenance
- Industry standard for modern systems

---

## Summary

| Concept | Description |
|-------|-------------|
| Thick Client | Logic mostly on client side |
| Thin Client | Logic mostly on backend |
| 2-Tier App | Client ↔ Database |
| 3-Tier App | Client ↔ Backend ↔ Database |
