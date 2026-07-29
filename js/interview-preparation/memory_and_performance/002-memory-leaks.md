# 📚 What causes Memory Leaks?

## 📖 Simple English Explanation

A **Memory Leak** happens when **memory that is no longer needed is not released**.

This usually happens because **JavaScript still has a reference to an object**, so the Garbage Collector cannot remove it.

> **Simple Definition:**
>
> **A Memory Leak occurs when unused objects remain in memory because they are still being referenced.**

---

## 🤔 Why is it Needed?

Understanding memory leaks helps you:

- Prevent high memory usage.
- Improve application performance.
- Avoid browser slowdowns and crashes.
- Build scalable applications.

---

## 🌊 Flow

```text
Create Object
      │
      ▼
Use Object
      │
      ▼
Object No Longer Needed
      │
      ▼
Reference Still Exists?
      │
  ┌───┴────┐
  ▼        ▼
 Yes       No
  │         │
  ▼         ▼
Memory    Garbage
Leak      Collector
            Removes It
```

---

## ✍️ Syntax

There is no special syntax for a memory leak.

Memory leaks happen because of **bad coding practices**.

---

## 💻 Example

### Example 1: Global Variables

```javascript
let user = {
  name: "John",
};
```

If `user` is never removed and is no longer needed, it stays in memory.

---

### Example 2: Unremoved Event Listeners

```javascript
const button = document.getElementById("btn");

button.addEventListener("click", () => {
  console.log("Clicked");
});
```

If the button is removed from the page but the event listener is never cleaned up, it may keep related objects in memory.

**Better**

```javascript
button.removeEventListener("click", handleClick);
```

---

### Example 3: Uncleared Timers

```javascript
const id = setInterval(() => {
  console.log("Running...");
}, 1000);
```

If the timer is no longer needed but isn't cleared, it continues running.

**Better**

```javascript
clearInterval(id);
```

---

### Example 4: Closures Holding References

```javascript
function createUser() {
  const largeData = new Array(1000000).fill("data");

  return function () {
    console.log(largeData.length);
  };
}

const fn = createUser();
```

The closure keeps a reference to `largeData`, so it stays in memory as long as `fn` exists.

---

### Example 5: Detached DOM Elements

```javascript
const div = document.getElementById("box");

// Remove from DOM
div.remove();
```

If another variable still references `div`, it cannot be garbage collected.

---

## 📋 Common Causes of Memory Leaks

| Cause                                      | Description                                   |
| ------------------------------------------ | --------------------------------------------- |
| Global variables                           | Stay in memory for the application's lifetime |
| Unremoved event listeners                  | Keep references to DOM elements or objects    |
| Uncleared `setInterval()` / `setTimeout()` | Continue running unnecessarily                |
| Closures                                   | May keep unused data alive                    |
| Detached DOM elements                      | Removed from the page but still referenced    |

---

## 🎤 Interview Answer (30 Seconds)

Memory leaks occur when objects that are no longer needed are still referenced, preventing the Garbage Collector from freeing their memory. Common causes include global variables, unremoved event listeners, uncleared timers, closures holding unnecessary references, and detached DOM elements. Memory leaks can increase memory usage and reduce application performance.

---

## 🧠 Memory Trick

```text
Unused Object
      │
      ▼
Reference Exists?
      │
  ┌───┴────┐
  ▼        ▼
 Yes       No
  │         │
  ▼         ▼
Memory    Garbage
Leak      Collector
```

Easy Rule:

> **Unused + Still Referenced = Memory Leak**

---

## ⭐ Keywords

- Memory Leak
- Garbage Collection
- References
- Global Variables
- Event Listeners
- Closures
- Timers
- Detached DOM
- Memory Management
