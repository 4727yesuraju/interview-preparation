# 📚 What are Truthy and Falsy Values?

## 📖 Simple English Explanation

In JavaScript, every value is treated as either **truthy** or **falsy** when used in a condition (like an `if` statement).

- **Truthy** → Behaves like `true`.
- **Falsy** → Behaves like `false`.

JavaScript automatically converts values to `true` or `false` when evaluating conditions.

---

## 🤔 Why is it Needed?

- To make decisions in `if`, `while`, and other conditional statements.
- Reduces the need to write explicit comparisons.
- Makes the code shorter and cleaner.

---

## 🌊 Flow

```text
Value
  │
  ▼
Used in a Condition
  │
  ▼
JavaScript converts it to
true or false
  │
 ┌──────┴──────┐
 │             │
 ▼             ▼
Truthy       Falsy
```

---

## ✍️ Syntax

```javascript
if (value) {
  // Executes if value is truthy
} else {
  // Executes if value is falsy
}
```

---

## 💻 Example

```javascript
let name = "John";

if (name) {
  console.log("Truthy");
}

let age = 0;

if (age) {
  console.log("Truthy");
} else {
  console.log("Falsy");
}
```

**Output:**

```text
Truthy
Falsy
```

---

## 🎤 Interview Answer (30 Seconds)

In JavaScript, every value is either **truthy** or **falsy** when used in a condition. **Truthy values** behave like `true`, while **falsy values** behave like `false`. JavaScript automatically converts values to a boolean during condition checking.

There are **only 8 falsy values**. Every other value is **truthy**.

---

## 🧠 Memory Trick

### Remember the **8 Falsy Values**

```text
false
0
-0
0n
""
null
undefined
NaN
```

**Easy Rule:**

> **Only these 8 values are Falsy. Everything else is Truthy.**

---

## ⭐ Keywords

- Truthy
- Falsy
- Boolean Conversion
- Condition
- `if`
- `false`
- `0`
- `null`
- `undefined`
- `NaN`
