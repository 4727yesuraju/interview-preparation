# 📚 What is Lexical Scope?

## 📖 Simple English Explanation

**Lexical Scope** means that a function can **access variables from its own scope and its parent (outer) scope**.

The word **lexical** means **where the function is written (defined)**, **not where it is called**.

---

## 🤔 Why is it Needed?

- Allows inner functions to access outer variables.
- Makes closures possible.
- Helps organize code in nested functions.

---

## 🌊 Flow

```text
Global Scope
      │
      ▼
Outer Function
      │
      ▼
Inner Function
      │
      ▼
Can Access
Own + Parent Variables
```

---

## ✍️ Syntax

```javascript
function outer() {
  let name = "John";

  function inner() {
    console.log(name);
  }

  inner();
}
```

---

## 💻 Example

### Example 1: Access Parent Variable

```javascript
function outer() {
  let name = "John";

  function inner() {
    console.log(name);
  }

  inner();
}

outer();
```

**Output**

```text
John
```

---

### Example 2: Multiple Levels

```javascript
let a = 10;

function outer() {
  let b = 20;

  function inner() {
    let c = 30;

    console.log(a, b, c);
  }

  inner();
}

outer();
```

**Output**

```text
10 20 30
```

---

### Example 3: Cannot Access Child Scope

```javascript
function outer() {
  function inner() {
    let message = "Hello";
  }

  inner();

  // console.log(message); // Error
}

outer();
```

**Reason:** Parent functions **cannot access child variables**.

---

## 🎤 Interview Answer (30 Seconds)

Lexical Scope means that a function can access variables from its own scope and its parent scope because scope is determined by **where the function is defined**, not where it is called. This concept is the foundation of **closures** in JavaScript.

---

## 🧠 Memory Trick

```text
Child
 │
 ▼
Can See Parent 👀

Parent
 │
 ▼
Cannot See Child ❌
```

Easy Rule:

> **Child → Parent ✅**

> **Parent → Child ❌**

---

## ⭐ Keywords

- Lexical Scope
- Parent Scope
- Child Scope
- Nested Functions
- Scope Chain
- Closure
