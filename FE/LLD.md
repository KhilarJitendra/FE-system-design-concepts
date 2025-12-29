This is based on **real FE interviews** and expectations for **Senior Frontend Engineers**.

---

# PayPal Frontend Machine Coding – Practice Questions

> **Time:** 60–90 mins
> **Focus:** UI logic, clean code, LLD thinking, edge cases

---

## ⭐ Tier 1: VERY COMMON (Must Practice)

These are **most likely**.

### 1️⃣ Autocomplete / Search Bar (Flipkart-style)

**Requirements**

* Input box
* API call on typing
* Debounce input
* Show suggestions
* Keyboard navigation
* Loading & error states

**What they evaluate**

* useDebounce hook
* Cancel in-flight requests
* Component separation
* Performance

---

### 2️⃣ Infinite Scroll List

**Requirements**

* Load items page by page
* Fetch next page on scroll end
* Show loader
* Handle end-of-list

**Evaluated**

* Scroll detection
* Memory leaks
* State updates
* Cleanup logic

---

### 3️⃣ Todo App (CRUD)

**Requirements**

* Add / edit / delete todos
* Mark complete
* Persist state (localStorage)

**Evaluated**

* State immutability
* Controlled inputs
* Clean component split

---

### 4️⃣ Comment Widget (FB / IG Style)

**Requirements**

* Add comments
* Nested replies
* Delete comment
* Recursive rendering

**Evaluated**

* Recursive components
* Data normalization
* Performance

---

### 5️⃣ Star Rating Component

**Requirements**

* Hover preview
* Click to select
* Controlled / uncontrolled support

**Evaluated**

* Component API design
* Accessibility
* Reusability

---

## ⭐ Tier 2: COMMON (Good to Practice)

### 6️⃣ Pagination Component

* Page numbers
* Next / prev
* Page size change

---

### 7️⃣ Image Gallery

* Grid layout
* Lazy loading
* Pagination / infinite scroll
* Search

---

### 8️⃣ Progress Bar

* Start / pause / reset
* Async simulation

---

### 9️⃣ Accordion / Tabs Component

* Controlled vs uncontrolled
* Keyboard navigation

---

### 🔟 Event Emitter

* Subscribe
* Unsubscribe
* Emit events

---

## ⭐ Tier 3: Less Frequent (But Strong Signals)

### 11️⃣ Basic Chat UI

* Message list
* Send message
* Auto-scroll

---

### 12️⃣ Kanban Board

* Columns
* Tasks
* Drag & drop

---

### 13️⃣ Calculator

* Chained operations
* Clear / reset

---

### 14️⃣ VS Code–Like Folder Explorer

* JSON → Tree UI
* Expand / collapse
* Recursive render

---

## 🔥 PayPal “Hidden” Follow-up Questions

After coding, expect these:

* Why did you keep state here?
* How would you scale this?
* How would you make this reusable?
* How would you test this?
* What are the edge cases?

---

## 🧠 How to Practice (IMPORTANT)

For **each question**, practice in this order:

1. **Explain LLD (2–3 mins)**

   * Component structure
   * State placement

2. **Code cleanly**

   * No god components
   * Custom hooks

3. **Mention trade-offs**

   * Debounce vs throttle
   * Local vs global state

---


