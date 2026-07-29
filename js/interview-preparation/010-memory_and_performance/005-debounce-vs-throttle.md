# 📚 Debounce vs Throttle

## 📖 Simple English Explanation

Both **Debouncing** and **Throttling** are techniques used to **improve performance** by controlling how often a function executes.

- **Debouncing** → Waits until the user **stops** triggering the event.
- **Throttling** → Executes the function at a **fixed time interval** while the event continues.

---

## 🤔 Why is it Needed?

Both techniques help to:

- Improve application performance.
- Reduce unnecessary function calls.
- Prevent excessive API requests or calculations.

---

## 🌊 Flow

### Debouncing

```text
Typing...

H
 │
He
 │
Hel
 │
Hell
 │
Hello
 │
(User Stops)
 │
 ▼
Wait 500ms
 │
 ▼
Run Once ✅
```

---

### Throttling

```text
Scrolling...

↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓

Run ✅
 │
Wait 500ms
 │
Run ✅
 │
Wait 500ms
 │
Run ✅
```

---

## ✍️ Syntax

### Debounce

```javascript
const debouncedFunction = debounce(callback, 500);
```

### Throttle

```javascript
const throttledFunction = throttle(callback, 500);
```

---

## 💻 Example

### Debouncing Example (Search Box)

```javascript
const search = debounce(() => {
  console.log("Searching...");
}, 500);

document.getElementById("search").addEventListener("input", search);
```

**User Types**

```text
H
He
Hel
Hell
Hello
```

**Output**

```text
Searching...
```

> Only **one** API call is made after the user stops typing.

---

### Throttling Example (Scroll)

```javascript
const scrollHandler = throttle(() => {
  console.log("Scrolling...");
}, 500);

window.addEventListener("scroll", scrollHandler);
```

**User Scrolls**

```text
↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓
```

**Output**

```text
Scrolling...
(wait 500ms)
Scrolling...
(wait 500ms)
Scrolling...
```

> The function runs every **500 ms** while scrolling.

---

## 📋 Comparison

| Feature                  | Debouncing                     | Throttling                |
| ------------------------ | ------------------------------ | ------------------------- |
| Execution                | After the event stops          | At fixed intervals        |
| During continuous events | ❌ No                          | ✅ Yes                    |
| Function calls           | Usually one                    | Multiple (limited)        |
| Best for                 | Search input, Auto-suggestions | Scroll, Resize, Mousemove |
| Goal                     | Wait until the user finishes   | Limit execution frequency |

---

## 🌍 Real-World Examples

| Debouncing       | Throttling              |
| ---------------- | ----------------------- |
| Search box       | Scroll position updates |
| Auto-complete    | Infinite scrolling      |
| Form validation  | Window resize           |
| Search API calls | Mouse movement tracking |

---

## 🎤 Interview Answer (30 Seconds)

Debouncing and throttling are performance optimization techniques. Debouncing delays a function until the event has stopped for a specified time, making it ideal for search inputs and API calls. Throttling limits a function to run at fixed intervals while the event continues, making it ideal for scroll, resize, and mousemove events.

---

## 🧠 Memory Trick

```text
Debouncing
──────────
Typing...
Typing...
Typing...
Stop
 │
 ▼
Run Once ✅


Throttling
──────────
Scrolling...
 │
 ▼
Run ✅
(wait)
Run ✅
(wait)
Run ✅
```

Easy Rule:

> **Debounce = Wait Until Stop**

> **Throttle = Run Every Few Seconds/Milliseconds**

---

## ⭐ Keywords

- Debouncing
- Throttling
- Performance
- Event Optimization
- Search Input
- Scroll Event
- API Calls
- setTimeout()
