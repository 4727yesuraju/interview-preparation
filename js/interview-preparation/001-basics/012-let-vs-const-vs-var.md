# 📚 Difference Between `let`, `const`, and `var`

## 📖 Simple English Explanation

`let`, `const`, and `var` are used to **declare variables** in JavaScript.

- **`var`** → Older way of declaring variables (before ES6). It can be **re-declared** and **re-assigned**.
- **`let`** → Modern way of declaring variables. It **cannot be re-declared**, but it **can be re-assigned**.
- **`const`** → Used for values that should **not change**. It **cannot be re-declared** or **re-assigned**.

**Simple Rule:**

- `var` → Re-declare ✅ Re-assign ✅
- `let` → Re-declare ❌ Re-assign ✅
- `const` → Re-declare ❌ Re-assign ❌

---

## 🤔 Why is it Needed?

- To store data in variables.
- `let` and `const` help avoid bugs caused by `var`.
- Modern JavaScript recommends using `let` and `const`.

---

## 🌊 Flow

```text
Need a Variable?
       │
       ▼
Will the value change?
       │
  ┌────┴────┐
  │         │
 No        Yes
  │         │
  ▼         ▼
const      let

Use var only in legacy code.
```

---

## ✍️ Syntax

```javascript
var name = "John";

let age = 25;

const country = "India";
```

---

## 💻 Example

```javascript
// var
var a = 10;
var a = 20; // ✅ Allowed

// let
let b = 10;
b = 20; // ✅ Allowed
// let b = 30; // ❌ Error

// const
const c = 10;
// c = 20;     // ❌ Error
```

---

## 🎤 Interview Answer (30 Seconds)

`var`, `let`, and `const` are used to declare variables in JavaScript.

`var` is the older way and allows both **re-declaration** and **re-assignment**.

`let` allows **re-assignment** but does not allow **re-declaration**.

`const` allows neither **re-declaration** nor **re-assignment**, so it is used for values that should remain constant. In modern JavaScript, `let` and `const` are preferred over `var`.

---

## 🧠 Memory Trick

```text
var
✅ Re-declare
✅ Re-assign

let
❌ Re-declare
✅ Re-assign

const
❌ Re-declare
❌ Re-assign
```

Easy Rule:

> **const → Never Change**  
> **let → Can Change**  
> **var → Old Way**

---

## ⭐ Keywords

- `var`
- `let`
- `const`
- Variable Declaration
- Re-declaration
- Re-assignment
- ES6
- Block Scope
- Function Scope
