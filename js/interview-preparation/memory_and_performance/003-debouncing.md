# 📚 What is Debouncing?

## 📖 Simple English Explanation

**Debouncing** is a technique that **delays the execution of a function until the user stops performing an action for a specified time**.

If the user keeps triggering the event (typing, scrolling, resizing, etc.), the timer **resets**, and the function does not run until the user pauses.

> **Simple Definition:**
>
> **Debouncing delays a function call until the event stops happening for a certain amount of time.**

---

## 🤔 Why is it Needed?

- Reduces unnecessary function calls.
- Improves application performance.
- Prevents excessive API requests.
- Commonly used in search boxes and window resize events.

---

## 🌊 Flow

```text
User Types

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
(User Stops Typing)
 │
 ▼
Wait 500ms
 │
 ▼
Function Executes Once
```

---

## ✍️ Syntax

```javascript
function debounce(callback, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);

    timer = setTimeout(() => {
      callback(...args);
    }, delay);
  };
}
```

---

## 💻 Example

### Example 1: Search Box

```javascript
function search() {
  console.log("Searching...");
}

const debouncedSearch = debounce(search, 500);

document.getElementById("search").addEventListener("input", debouncedSearch);
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

> Only **one** search happens after the user stops typing for **500 ms**.

---

### Example 2: Window Resize

```javascript
window.addEventListener(
  "resize",
  debounce(() => {
    console.log("Window resized");
  }, 300),
);
```

The function runs **once**, after resizing stops.

---

## 📋 Real-World Uses

| Use Case         | Why Debouncing?                      |
| ---------------- | ------------------------------------ |
| Search box       | Avoid API calls for every keystroke  |
| Auto-suggestions | Fetch suggestions after typing stops |
| Window resize    | Avoid repeated calculations          |
| Scroll events    | Reduce unnecessary updates           |

---

## 🎤 Interview Answer (30 Seconds)

Debouncing is a technique that delays the execution of a function until an event has stopped occurring for a specified period of time. If the event keeps occurring, the timer is reset. It is commonly used in search boxes, auto-suggestions, and resize events to improve performance and reduce unnecessary function calls.

---

## 🧠 Memory Trick

```text
Typing...
   │
   ▼
Reset Timer
   │
Typing...
   │
   ▼
Reset Timer
   │
User Stops
   │
Wait
   │
   ▼
Function Runs Once
```

Easy Rule:

> **Debouncing = Wait until the user stops.**

---

## ⭐ Keywords

- Debouncing
- setTimeout()
- clearTimeout()
- Delay
- Search Box
- API Calls
- Performance
- Event Optimization
