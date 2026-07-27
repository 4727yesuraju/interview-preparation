# 📚 Types of Callback Queues

## 📖 Simple English Explanation

JavaScript actually has **two main callback queues**:

1. **Microtask Queue** (High Priority)
2. **Macrotask Queue (Callback Queue)** (Normal Priority)

The **Event Loop always checks the Microtask Queue first**. Only when it becomes empty does it process the Macrotask Queue.

---

## 🤔 Why is it Needed?

- Some asynchronous tasks need to run immediately after the current code.
- Others can wait their turn.
- Separate queues help JavaScript execute tasks efficiently.

---

## 🌊 Flow

```text
Synchronous Code
        │
        ▼
Call Stack
        │
(Call Stack Empty?)
        │
        ▼
Microtask Queue
(Promise, queueMicrotask, MutationObserver)
        │
(Empty?)
        │
        ▼
Macrotask Queue
(setTimeout, setInterval, I/O, Events)
```

---

## ✍️ Syntax

### Microtask Queue

```javascript
Promise.resolve().then(() => {
  console.log("Microtask");
});
```

### Macrotask Queue

```javascript
setTimeout(() => {
  console.log("Macrotask");
}, 0);
```

---

## 💻 Example

```javascript
console.log("Start");

setTimeout(() => {
  console.log("setTimeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

**Output**

```text
Start
End
Promise
setTimeout
```

**Why?**

- `Start` and `End` are synchronous.
- `Promise.then()` goes to the **Microtask Queue**.
- `setTimeout()` goes to the **Macrotask Queue**.
- The Event Loop executes all microtasks before macrotasks.

---

## 📋 Common Examples

| Microtask Queue     | Macrotask Queue             |
| ------------------- | --------------------------- |
| `Promise.then()`    | `setTimeout()`              |
| `Promise.catch()`   | `setInterval()`             |
| `Promise.finally()` | DOM Events (click, keydown) |
| `queueMicrotask()`  | File I/O (Node.js)          |
| `MutationObserver`  | Network callbacks           |

---

## 🎤 Interview Answer (30 Seconds)

JavaScript has two callback queues: the **Microtask Queue** and the **Macrotask Queue**. Promise callbacks and `queueMicrotask()` are placed in the Microtask Queue, while `setTimeout()`, `setInterval()`, and event callbacks go into the Macrotask Queue. After the Call Stack becomes empty, the Event Loop always executes all microtasks first and then processes macrotasks.

---

## 🧠 Memory Trick

```text
Call Stack Empty
        │
        ▼
Microtask Queue ⭐
        │
        ▼
Macrotask Queue
```

Easy Rule:

> **Microtask First → Macrotask Next**

---

## ⭐ Keywords

- Microtask Queue
- Macrotask Queue
- Callback Queue
- Event Loop
- Promise
- setTimeout()
- queueMicrotask()
- Priority
