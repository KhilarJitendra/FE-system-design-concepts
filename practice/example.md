Perfect 👍
I’ll give you **ONE complete frontend system design example**, **step by step**, **exactly following your cheat sheet**, so you can **reuse this structure in interviews**.

---

# 🧠 Example: Frontend System Design

## **Design a Real-Time Order Tracking Page (E-commerce)**

(Think Amazon / Flipkart order status screen)

---

## 1️⃣ Clarify Requirements (START HERE)

### Ask the interviewer 👇

**Functional**

* Show order details
* Show live order status (Placed → Shipped → Delivered)
* Show delivery ETA
* Support multiple orders

**Non-functional**

* Fast load
* Works on mobile
* Accessible
* Near real-time updates

**Constraints**

* Users: millions
* Regions: India + global
* Devices: mobile-heavy
* Real-time needed: yes (order updates)

**Out of scope**

* Payment flow
* Admin dashboard

✅ **Repeat back**

> “We’re designing a customer-facing order tracking page with near real-time updates, optimized for performance and accessibility, excluding payments and admin features.”

---

## 2️⃣ High-Level Architecture (Zoom Out)

```
Browser
 ↓
CDN (HTML, JS, images)
 ↓
Frontend App
 ↓
API Gateway
 ↓
Order Service
```

Optional:

```
WebSocket / SSE → Live updates
```

📌 Frontend responsibilities:

* Rendering order timeline
* Handling loading & errors
* Updating UI in real time
* Performance & accessibility

---

## 3️⃣ Data Modeling (Frontend View)

UI-driven models:

```ts
Order {
  id
  status
  eta
  items[]
}

OrderEvent {
  status
  timestamp
}
```

Questions answered:

* One order at a time
* Small payload
* Status updates frequently

---

## 4️⃣ Client ↔ Server Communication

### Initial Load

* **REST API**

```http
GET /api/orders/{orderId}
```

Reason:

* Simple
* Cacheable
* SEO friendly

---

### Real-Time Updates

Options discussed:

* Polling ❌ (wasteful)
* Long polling ⚠️
* **WebSocket / SSE ✅**

Chosen:

> **WebSocket for live status updates**

Tradeoff:

* Stateful
* Needs scaling strategy

---

## 5️⃣ State Management (Very Important)

### Split state clearly

**Server State**

* Order details
* Order status
* Cached with TTL

**UI State**

* Loading
* Error
* Expanded view
* Retry state

📌 Why interviewer likes this:

* Clean separation
* Fewer bugs
* Scales well

---

## 6️⃣ Performance Strategy (Mention 4+)

* CDN for static assets
* Code splitting (order page lazy-loaded)
* Image optimization (product thumbnails)
* API caching
* Skeleton loaders
* Memoized status timeline

📌 Say:

> “Performance decisions depend on traffic patterns and device constraints.”

---

## 7️⃣ Accessibility (Senior Signal 🚀)

Mention clearly:

* Status updates announced via screen reader
* Keyboard navigation
* ARIA live regions for real-time status
* Color contrast for timeline
* Responsive layout

📌 This alone can separate you from 80% candidates.

---

## 8️⃣ Optional Add-ons (If Time Allows)

* Localization for ETA/time zones
* Offline fallback (last known status)
* Security: auth token, no sensitive data in client

---

## 9️⃣ Tradeoffs (MOST IMPORTANT)

### Example tradeoffs you must say 👇

* WebSocket gives real-time UX but is harder to scale
* REST is simpler but not real-time
* More caching = faster but risk of stale data
* Accessibility adds effort but improves reach

📌 Interviewers listen here very carefully.

---

## 🔟 How to End (Strong Finish)

> “This design balances real-time updates, performance, and accessibility. If scale increases significantly, we could optimize further by switching to SSE or introducing event-driven updates via a message broker.”

---

## 🎯 One-Line Summary (Say This)

> “I started by clarifying requirements, designed a CDN-backed frontend architecture, chose REST for initial load, WebSockets for real-time updates, clearly separated server and UI state, optimized for performance and accessibility, and discussed tradeoffs.”

---

## 🧠 How to Reuse This in Any Interview

Just replace **Order Tracking** with:

* Chat App
* Live Dashboard
* Feed Page
* Search Results
* Notifications Panel

**Same structure. Always works.**

---
