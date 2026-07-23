# 📚 What is an IIFE (Immediately Invoked Function Expression)?

## 📖 Simple English Explanation

An **IIFE (Immediately Invoked Function Expression)** is a function that **runs immediately after it is created**.

Instead of defining a function and calling it later, an IIFE is **created and executed at the same time**.

---

## 🤔 Why is it Needed?

- Executes code immediately.
- Creates a private scope.
- Prevents variables from polluting the global scope.
- Commonly used before ES6 modules.

---

## 🌊 Flow

```text
Create Function
       │
       ▼
Wrap in ()
       │
       ▼
Add ()
       │
       ▼
Runs Immediately
```

---

## ✍️ Syntax

```javascript
(function () {
  // Code
})();
```

Or

```javascript
(() => {
  // Code
})();
```

---

## 💻 Example

### Example 1: Basic IIFE

```javascript
(function () {
  console.log("Hello");
})();
```

**Output**

```text
Hello
```

---

### Example 2: IIFE with Parameters

```javascript
(function (name) {
  console.log(`Hello ${name}`);
})("John");
```

**Output**

```text
Hello John
```

---

### Example 3: Private Scope

```javascript
(function () {
  let message = "Private";

  console.log(message);
})();

// console.log(message); // Error
```

**Output**

```text
Private
```

---

## 🎤 Interview Answer (30 Seconds)

An **IIFE (Immediately Invoked Function Expression)** is a function that is created and executed immediately after its definition. It is commonly used to execute code once and create a private scope, preventing variables from polluting the global scope.

---

## 🧠 Memory Trick

```text
Create Function
      +
Call Immediately
      =
IIFE
```

Easy Rule:

> **IIFE = Create + Execute Immediately**

---

## ⭐ Keywords

- IIFE
- Immediately Invoked Function Expression
- Private Scope
- Global Scope
- Self-Invoking Function
- Function Expression
