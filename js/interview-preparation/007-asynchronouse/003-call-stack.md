# 📚 What is the Call Stack?

## 📖 Simple English Explanation

The **Call Stack** is a data structure used by the JavaScript engine to **keep track of function execution**.

- When a function is called, it is **pushed** onto the Call Stack.
- When the function finishes, it is **popped** from the Call Stack.
- JavaScript executes **one function at a time**, so the Call Stack follows the **LIFO (Last In, First Out)** principle.

---

## 🤔 Why is it Needed?

- Keeps track of which function is currently executing.
- Manages the order of function execution.
- Helps JavaScript execute code correctly.

---

## 🌊 Flow

```text
main()

Call main()
      │
      ▼
Call Stack
────────────
|  main()  |
────────────
      │
      ▼
main() calls greet()

────────────
| greet()  |
| main()   |
────────────
      │
      ▼
greet() finishes

────────────
| main()   |
────────────
      │
      ▼
main() finishes

Empty Stack
```

---

## ✍️ Syntax

```javascript
function greet() {
  console.log("Hello");
}

function main() {
  greet();
}

main();
```

---

## 💻 Example

```javascript
function one() {
  console.log("One");
}

function two() {
  one();
  console.log("Two");
}

two();
```

**Output**

```text
One
Two
```

### Call Stack Execution

```text
Call two()
      │
      ▼
Stack:
two()

two() calls one()
      │
      ▼
Stack:
one()
two()

one() finishes
      │
      ▼
Stack:
two()

two() finishes
      │
      ▼
Stack:
Empty
```

---

## 🎤 Interview Answer (30 Seconds)

The Call Stack is a data structure that keeps track of function execution in JavaScript. Whenever a function is called, it is pushed onto the stack. When the function finishes, it is popped from the stack. Since JavaScript is single-threaded, only one function executes at a time, following the LIFO (Last In, First Out) principle.

---

## 🧠 Memory Trick

```text
Call Function
      │
      ▼
Push 📥

Function Ends
      │
      ▼
Pop 📤
```

Easy Rule:

> **Call = Push 📥**

> **Finish = Pop 📤**

---

## ⭐ Keywords

- Call Stack
- Push
- Pop
- Function Execution
- LIFO
- Single Thread
- JavaScript Engine

```

```
