# 📚 What is the Callback Queue?

## 📖 Simple English Explanation

The **Callback Queue** is a queue that **stores callbacks of completed asynchronous operations**.

When an asynchronous task (like `setTimeout()`, API call, or file read) finishes:

- Its callback is placed in the **Callback Queue**.
- It **does not execute immediately**.
- The **Event Loop** waits until the **Call Stack is empty**, then moves the callback from the Callback Queue to the Call Stack for execution.

---

## 🤔 Why is it Needed?

- Stores completed asynchronous callbacks.
- Prevents asynchronous tasks from interrupting synchronous code.
- Ensures callbacks execute in the correct order.

---

## 🌊 Flow

```text
JavaScript Code
       │
       ▼
Call Stack
       │
       ▼
Async Task
(setTimeout, API, File Read)
       │
       ▼
Browser APIs / Web APIs
or
libuv (Node.js)
       │
(Task Completes)
       ▼
Callback Queue
       │
       ▼
Event Loop
       │
(Call Stack Empty?)
       │
      Yes
       │
       ▼
Move Callback to Call Stack
       │
       ▼
Execute Callback
```

---

## ✍️ Syntax

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Hello");
}, 1000);

console.log("End");
```

---

## 💻 Example

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Callback");
}, 1000);

console.log("End");
```

**Output**

```text
Start
End
Callback
```

### Execution Flow

```text
1. "Start" prints.
2. setTimeout() starts in Browser APIs (or libuv).
3. "End" prints.
4. Timer finishes.
5. Callback enters the Callback Queue.
6. Event Loop waits for the Call Stack to become empty.
7. Callback moves to the Call Stack.
8. "Callback" prints.
```

---

## 🎤 Interview Answer (30 Seconds)

The Callback Queue is a queue that stores callbacks of completed asynchronous operations. When an asynchronous task finishes, its callback is added to the Callback Queue. The Event Loop continuously checks whether the Call Stack is empty. Once it is empty, the Event Loop moves the callback from the Callback Queue to the Call Stack, where it gets executed.

---

## 🧠 Memory Trick

```text
Async Task Finished
        │
        ▼
Callback Queue
        │
        ▼
Event Loop
        │
(Call Stack Empty?)
        │
        ▼
Execute Callback
```

Easy Rule:

> **Callback Queue = Waiting room for completed asynchronous callbacks.**

---

## ⭐ Keywords

- Callback Queue
- Event Loop
- Call Stack
- Callback
- Asynchronous
- Web APIs
- libuv
- FIFO (First In, First Out)
