# 📚 What is the Event Loop?

## 📖 Simple English Explanation

The **Event Loop** is a mechanism in JavaScript that **continuously checks whether the Call Stack is empty**.

- If the **Call Stack is busy**, it waits.
- If the **Call Stack is empty**, it takes the next callback from the **Callback Queue** and executes it.

This is how JavaScript handles **asynchronous operations** without blocking the main thread.

---

## 🤔 Why is it Needed?

- JavaScript is **single-threaded** (one Call Stack).
- It cannot execute multiple tasks at the same time.
- The Event Loop helps JavaScript execute asynchronous tasks after the current synchronous code finishes.

---

## 🌊 Flow

```text
JavaScript Code
       │
       ▼
Call Stack
       │
       ▼
Slow Task? (API, Timer, File, DB)
       │
       ▼
Browser APIs / Web APIs (Browser)
or
libuv (Node.js)
       │
       ▼
Task Completes
       │
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
  console.log("Timer Finished");
}, 1000);

console.log("End");
```

**Output**

```text
Start
End
Timer Finished
```

**Why?**

- `Start` executes first.
- `setTimeout()` is sent to Browser APIs (or libuv in Node.js).
- JavaScript continues and prints `End`.
- After 1 second, the callback enters the Callback Queue.
- The Event Loop waits until the Call Stack is empty, then moves the callback to the Call Stack.
- Finally, `Timer Finished` is printed.

---

## 🎤 Interview Answer (30 Seconds)

The Event Loop is a mechanism in JavaScript that continuously checks whether the Call Stack is empty. When an asynchronous operation finishes, its callback is placed in the Callback Queue. Once the Call Stack becomes empty, the Event Loop moves the callback to the Call Stack for execution. This allows JavaScript to handle asynchronous tasks without blocking the main thread.

---

## 🧠 Memory Trick

```text
Call Stack Busy?
      │
      ├── Yes → Wait ⏳
      │
      └── No
           │
           ▼
Take Callback
           │
           ▼
Execute
```

Easy Rule:

> **Event Loop = Checks the Call Stack and runs waiting callbacks when it becomes empty.**

---

## ⭐ Keywords

- Event Loop
- Call Stack
- Callback Queue
- Web APIs
- libuv
- Asynchronous
- Single Thread
- Non-Blocking
