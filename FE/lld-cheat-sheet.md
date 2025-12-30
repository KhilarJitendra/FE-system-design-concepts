1️⃣ **Pure LLD Diagram (no code)**
2️⃣ **LLD Verbal Explanation (interview-ready script)**

You can literally **memorize + adapt** this.

---

# 1️⃣ Pure LLD – Autocomplete / Search Bar

## 🔹 High-level responsibility

> “Design a reusable, accessible, debounced autocomplete component.”

---

## 📦 Component Diagram (LLD)

```txt
Autocomplete (Container)
 ├── SearchInput (Controlled)
 ├── SuggestionsDropdown
 │     └── SuggestionItem
 ├── useDebounce (hook)
 └── SearchService (API abstraction)
```

---

## 📦 Component Responsibilities

### 🔹 Autocomplete (Container)

**Responsibilities**

* Owns state
* Orchestrates data flow
* Handles keyboard navigation
* Handles API integration

**State**

```ts
query: string
suggestions: string[]
loading: boolean
error: string | null
activeIndex: number
```

---

### 🔹 SearchInput

**Responsibilities**

* Render input field
* Capture user input
* Forward keyboard events

**Props**

```ts
value: string
onChange: (value) => void
onKeyDown: (event) => void
```

❌ No internal state
✅ Controlled component

---

### 🔹 SuggestionsDropdown

**Responsibilities**

* Render list
* Highlight active item
* Handle mouse selection

**Props**

```ts
items: string[]
activeIndex: number
onSelect: (item) => void
```

---

### 🔹 SuggestionItem

**Responsibilities**

* Display single suggestion
* Highlight based on activeIndex

**Props**

```ts
label: string
isActive: boolean
```

---

### 🔹 useDebounce (Hook)

**Responsibilities**

* Delay value changes
* Prevent excessive API calls

**Input**

```ts
value: string
delay: number
```

**Output**

```ts
debouncedValue: string
```

---

### 🔹 SearchService

**Responsibilities**

* Abstract API calls
* Handle request logic

**Methods**

```ts
fetchSuggestions(query: string): Promise<string[]>
```

---

## 🔁 Data Flow Diagram

```txt
User types
   ↓
SearchInput
   ↓
query (state)
   ↓
useDebounce
   ↓
debouncedQuery
   ↓
SearchService.fetchSuggestions
   ↓
suggestions (state)
   ↓
SuggestionsDropdown
```

---

## ⌨️ Keyboard Interaction Flow

```txt
ArrowDown → activeIndex + 1
ArrowUp   → activeIndex - 1
Enter     → select active item
Escape   → close dropdown
```

---

## ⚠️ Edge Case Handling (LLD-level)

* Empty query → clear suggestions
* Fast typing → debounced calls
* Stale API response → ignore / abort
* API error → error state
* Mouse + keyboard conflict → resolved via activeIndex

---

# 2️⃣ LLD Verbal Explanation (Interview Script)

You can say this **almost verbatim** 👇

---

## 🎤 Step 1: Start with scope

> “I’ll design an autocomplete component with debounced API calls, keyboard navigation, and proper loading and error handling.”

---

## 🎤 Step 2: Component breakdown

> “At the top, I have an `Autocomplete` container that owns all state and business logic.
> The input and suggestion list are kept as presentational components.”

Why this sounds senior:

* Mentions container vs presentational
* Shows separation of concerns

---

## 🎤 Step 3: State ownership

> “All state like query, suggestions, loading, error, and activeIndex lives in the container to maintain a single source of truth.”

🔥 This line scores big.

---

## 🎤 Step 4: Data flow

> “User input updates query → query is debounced using a custom hook → debounced value triggers an API call → results update state → UI re-renders.”

Short. Clear. Correct.

---

## 🎤 Step 5: Keyboard navigation

> “I handle keyboard navigation using an `activeIndex` state instead of DOM refs, which keeps behavior predictable and avoids imperative code.”

This shows **React maturity**.

---

## 🎤 Step 6: API abstraction

> “API logic is abstracted into a service layer so the component stays UI-focused and is easier to test or replace later.”

---

## 🎤 Step 7: Race conditions

> “To avoid race conditions from rapid typing, I either ignore stale responses or use AbortController.”

Even mentioning this = senior signal.

---

## 🎤 Step 8: Trade-offs (most important)

> “Debounce improves performance but adds slight latency; I chose it over throttle since autocomplete favors final input over intermediate keystrokes.”

🔥 Interview gold.

---

## 🎤 Step 9: Extensibility

> “This design supports caching, accessibility via ARIA roles, and virtualization if the suggestion list grows large.”

---

# 🧠 One-line LLD Summary (Memorize This)

> “LLD focuses on component boundaries, state ownership, data flow, and trade-offs — not just making the UI work.”

---

