# 📚 What are Pure Functions?

## 📖 Simple English Explanation

A **Pure Function** is a function that:

1. **Always returns the same output for the same input.**
2. **Does not modify or depend on anything outside the function (no side effects).**

This means the function is **predictable**.

---

## 🤔 Why is it Needed?

- Produces predictable results.
- Easier to test and debug.
- Avoids unexpected changes.
- Makes code reusable and maintainable.

---

## 🌊 Flow

```text
Same Input
     │
     ▼
Pure Function
     │
     ▼
Same Output
     │
No Side Effects
```

---

## ✍️ Syntax

```javascript
function add(a, b) {
  return a + b;
}
```

---

## 💻 Example

### Example 1: Pure Function ✅

```javascript
function add(a, b) {
  return a + b;
}

console.log(add(10, 20));
```

**Output**

```text
30
```

---

### Example 2: Same Input → Same Output ✅

```javascript
function square(num) {
  return num * num;
}

console.log(square(5));
console.log(square(5));
```

**Output**

```text
25
25
```

---

### Example 3: Not a Pure Function ❌

```javascript
let total = 0;

function add(num) {
  total += num;
  return total;
}
```

**Reason:**

The function modifies the external variable `total`, so it has a **side effect**.

---

## 🎤 Interview Answer (30 Seconds)

A **Pure Function** is a function that always returns the same output for the same input and has **no side effects**. It does not modify external variables or depend on external state, making the function predictable, easy to test, and easy to maintain.

---

## 🧠 Memory Trick

```text
Same Input
     │
     ▼
Same Output
     │
No Side Effects
```

Easy Rule:

> **Pure = Predictable**

---

## ⭐ Keywords

- Pure Function
- Same Input
- Same Output
- No Side Effects
- Predictable
- Functional Programming
