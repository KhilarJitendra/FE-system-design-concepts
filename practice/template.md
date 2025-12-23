Here’s a **1-page Frontend System Design Cheat Sheet** you can revise **before interviews** or even mentally follow **during the interview**.

---

# 🧠 Frontend System Design – 1-Page Cheat Sheet

## 1️⃣ Start Strong: Clarify Requirements (5–10 min)

**Always ask first. Never design immediately.**

### Ask about:

* **Functional** – core features (CRUD, views, interactions)
* **Non-functional** – performance, accessibility, SEO, scalability
* **Constraints** – users, devices, regions, real-time needs
* **Out of scope** – explicitly say what you’re not designing

✅ **Repeat back**:

> “So we’re building X, focusing on Y, excluding Z. Correct?”

---

## 2️⃣ Think in Systems, Not Components

**High-level first** (zoom out):

```
Client → CDN → API → Backend Services
```

Frontend owns:
 
* Rendering
* State management
* Performance
* Accessibility
* UX reliability

🚫 Don’t jump into React components early.

---

## 3️⃣ Data Modeling (Frontend View)

Define **UI-driven entities**, not DB tables.

Ask:

* What data does UI need?
* How much data at once?
* Partial loading or pagination?

Example:

* User
* Product
* Event
* Message

---

## 4️⃣ Client ↔ Server Communication

Discuss **patterns**, not tools first.

* REST vs GraphQL vs WebSockets
* Fetching strategy
* Error handling
* Caching strategy

📌 Always say:

> “There’s no silver bullet — this is a tradeoff.”

---

## 5️⃣ State Management (Critical)

### Split clearly:

* **Server State**
  → API data, cached, synced
* **UI State**
  → Modals, filters, view modes

Why this matters:

* Fewer bugs
* Better performance
* Easier scaling

---

## 6️⃣ Performance (Almost Mandatory)

Mention at least **3–4**:

* Code splitting
* Lazy loading
* Image optimization
* CDN caching
* Virtualization
* Memoization
* SSR / CSR / SSG decision

📌 Say:

> “Performance depends on scale and usage patterns.”

---

## 7️⃣ Accessibility (Frontend Senior Signal)

Must mention:

* Keyboard navigation
* Screen readers
* ARIA roles
* Color contrast
* Responsive design

🚀 This is where frontend engineers stand out.

---

## 8️⃣ Optional but Powerful Add-Ons

If time allows:

* Localization & i18n
* Offline-first support
* Real-time sync
* Security basics (XSS, auth tokens)

---

## 9️⃣ Tradeoffs (MOST IMPORTANT)

For every major choice:

* Why this?
* What are the downsides?
* When would you change it?

❗ Interviewers listen for **tradeoff thinking** more than tools.

---

## 🔟 How to End Your Answer

End with:

> “This design balances simplicity, performance, and scalability. Depending on constraints, we could optimize further in these areas…”

---

# 🚩 Red Flags (Avoid These)

❌ Jumping into design immediately
❌ Tool-dumping (React, Redux, etc.)
❌ Only happy-path thinking
❌ Ignoring accessibility/performance
❌ No tradeoffs
❌ Staying silent — think out loud

---

# 🟢 Green Flags (Do These)

✅ Ask clarifying questions
✅ Think aloud
✅ Zoom in / zoom out
✅ Admit unknowns
✅ Collaborate with interviewer

---

## 🎯 One-Line Memory Hook

> **Requirements → Architecture → Data → APIs → State → Performance → Accessibility → Tradeoffs**

---
