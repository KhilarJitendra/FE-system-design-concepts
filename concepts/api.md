# APIs (Application Programming Interfaces)

An **API (Application Programming Interface)** is a **contract** that allows different software systems to **communicate with each other**.

In web systems:
> **Client ↔ API ↔ Server**

---

## Why APIs are Needed?

- Decouple frontend and backend
- Enable communication between services
- Reusability of business logic
- Support multiple clients (Web, Mobile, Third-party)

---

## API in Client–Server Architecture

1. Client sends request to API
2. API processes business logic
3. API interacts with database or other services
4. API sends response back to client

---

## Types of APIs (High Level)

### 1. Public APIs
- Open to external users
- Example: Google Maps API

---

### 2. Private APIs
- Used internally within an organization
- Example: Internal microservices APIs

---

### 3. Partner APIs
- Shared with selected partners
- Requires authentication

---

## API Communication Styles

### 1. REST API (Most Common)

REST stands for **Representational State Transfer**.

#### Key Principles
- Uses HTTP methods
- Stateless
- Resource-based URLs

#### Example
```http
GET /api/users/123
POST /api/users
```

### 2. GraphQL API

GraphQL allows clients to request exactly the data they need.

#### Example
```txt
query {
  user(id: 123) {
    name
    email
  }
}
```

### 3. gRPC

- High-performance binary protocol

- Uses HTTP/2

- Common in microservices


### REST API Design Basics

- Use nouns, not verbs

```txt
/api/users
/api/orders
```

- API Versioning
Avoid breaking existing clients

```txt
/api/v1/users
/api/v2/users
```

### API Security Best Practices

- Always use HTTPS

- Validate inputs

- Rate limiting

- Authentication & authorization

- Avoid exposing sensitive data

### API Performance Considerations

- Pagination for large data

- Caching responses

- Avoid over-fetching

- Use compression (gzip)
