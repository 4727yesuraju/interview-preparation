# 📚 What is `queueMicrotask()`?

## 📖 Simple English Explanation

`queueMicrotask()` is a JavaScript method used to **add a function to the Microtask Queue**.

The function **does not execute immediately**. It waits until the **current synchronous code finishes**. Then, the **Event Loop** executes it **before any macrotasks** (such as `setTimeout()`).

---

## 🤔 Why is it Needed?

- Schedule a small task to run after the current code.
- Execute code before `setTimeout()`.
- Ensure code runs in the correct order.

---

## 🌊 Flow

```text
JavaScript Code
        │
        ▼
Call Stack
        │
(Current code finishes)
        ▼
Microtask Queue
(queueMicrotask)
        │
        ▼
Event Loop
        │
        ▼
Execute Microtask
        │
        ▼
Macrotask Queue
(setTimeout)
```

---

## ✍️ Syntax

```javascript
queueMicrotask(() => {
  // code
});
```

---

## 💻 Example

### Example 1

```javascript
console.log("Start");

queueMicrotask(() => {
  console.log("Microtask");
});

console.log("End");
```

**Output**

```text
Start
End
Microtask
```

---

### Example 2: `queueMicrotask()` vs `setTimeout()`

```javascript
console.log("Start");

setTimeout(() => {
  console.log("setTimeout");
}, 0);

queueMicrotask(() => {
  console.log("Microtask");
});

console.log("End");
```

**Output**

```text
Start
End
Microtask
setTimeout
```

**Why?**

- `queueMicrotask()` adds the callback to the **Microtask Queue**.
- `setTimeout()` adds the callback to the **Macrotask Queue**.
- The Event Loop always executes **all microtasks before macrotasks**.

---

## 🎤 Interview Answer (30 Seconds)

`queueMicrotask()` is used to schedule a function in the Microtask Queue. After the current synchronous code finishes, the Event Loop executes all microtasks before processing the Macrotask Queue. Therefore, a callback scheduled with `queueMicrotask()` runs before callbacks from `setTimeout()`.

---

## 🧠 Memory Trick

```text
Current Code
      │
      ▼
queueMicrotask()
      │
      ▼
Microtask Queue ⭐
      │
      ▼
Runs First
```

Easy Rule:

> **`queueMicrotask()` = Add work to the Microtask Queue.**

---

## ⭐ Keywords

- queueMicrotask()
- Microtask Queue
- Event Loop
- Call Stack
- Asynchronous
- High Priority
- setTimeout()
