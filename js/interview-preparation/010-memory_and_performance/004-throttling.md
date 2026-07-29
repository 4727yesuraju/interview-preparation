# 📚 What is Throttling?

## 📖 Simple English Explanation

**Throttling** is a technique that **limits how often a function can execute**.

Once the function runs, it **cannot run again until a specified time has passed**, even if the event keeps happening.

> **Simple Definition:**
>
> **Throttling allows a function to run at a fixed interval while the event is continuously occurring.**

---

## 🤔 Why is it Needed?

- Reduces unnecessary function calls.
- Improves application performance.
- Prevents excessive processing during continuous events.
- Commonly used for scrolling, resizing, and mouse movement.

---

## 🌊 Flow

```text
User Scrolls Continuously

││││││││││││││││││││
        │
        ▼
Run Function
        │
 Wait 500ms
        │
        ▼
Run Function Again
        │
 Wait 500ms
        │
        ▼
Run Function Again
```

---

## ✍️ Syntax

```javascript
function throttle(callback, delay) {
  let canRun = true;

  return function (...args) {
    if (!canRun) return;

    callback(...args);
    canRun = false;

    setTimeout(() => {
      canRun = true;
    }, delay);
  };
}
```

---

## 💻 Example

### Example 1: Scroll Event

```javascript
function onScroll() {
  console.log("Scrolling...");
}

const throttledScroll = throttle(onScroll, 500);

window.addEventListener("scroll", throttledScroll);
```

**User Scrolls Continuously**

```text
↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓
```

**Output**

```text
Scrolling...
(wait 500 ms)
Scrolling...
(wait 500 ms)
Scrolling...
```

> The function executes **once every 500 ms**, even though the user is scrolling continuously.

---

### Example 2: Mouse Move

```javascript
window.addEventListener(
  "mousemove",
  throttle(() => {
    console.log("Mouse Moving");
  }, 1000),
);
```

The function runs at most **once every second**.

---

## 📋 Real-World Uses

| Use Case       | Why Throttling?                  |
| -------------- | -------------------------------- |
| Scroll events  | Limit updates while scrolling    |
| Resize events  | Reduce repeated calculations     |
| Mouse movement | Prevent excessive event handling |
| Button clicks  | Prevent repeated rapid clicks    |

---

## 🎤 Interview Answer (30 Seconds)

Throttling is a technique that limits how often a function can execute during continuous events. Once the function runs, it waits for a specified time before allowing another execution. It is commonly used for scroll, resize, and mousemove events to improve performance and reduce unnecessary function calls.

---

## 🧠 Memory Trick

```text
Scrolling...
     │
     ▼
Run Function ✅
     │
Wait 500ms
     │
Scrolling...
     │
     ▼
Run Again ✅
```

Easy Rule:

> **Throttling = Run at Fixed Intervals**

---

## ⭐ Keywords

- Throttling
- setTimeout()
- Fixed Interval
- Scroll Event
- Resize Event
- Mousemove
- Performance
- Event Optimization
