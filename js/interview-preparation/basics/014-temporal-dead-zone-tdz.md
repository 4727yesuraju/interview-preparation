# 📚 What is Temporal Dead Zone (TDZ)?

## 📖 Simple English Explanation

The **Temporal Dead Zone (TDZ)** is the period between **hoisting** and **variable declaration**, during which a `let` or `const` variable **exists but cannot be accessed**.

If you try to access it during this period, JavaScript throws a **ReferenceError**.

**Note:** TDZ applies only to **`let`** and **`const`**, **not** to `var`.

---

## 🤔 Why is it Needed?

- Prevents the use of variables before they are initialized.
- Helps avoid bugs caused by accessing variables too early.
- Makes the code safer and more predictable.

---

## 🌊 Flow

```text
JavaScript Starts
        │
        ▼
Variable is Hoisted
        │
        ▼
────── TDZ ──────
Cannot Access
        │
        ▼
Variable Declaration
(let / const)
        │
        ▼
Now You Can Access It
```

---

## ✍️ Syntax

```javascript
console.log(name);

let name = "John";
```

---

## 💻 Example

```javascript
console.log(name);

let name = "John";
```

**Output**

```text
ReferenceError:
Cannot access 'name' before initialization
```

Another Example:

```javascript
const PI = 3.14;

console.log(PI);
```

**Output**

```text
3.14
```

---

## 🎤 Interview Answer (30 Seconds)

The **Temporal Dead Zone (TDZ)** is the time between when a `let` or `const` variable is **hoisted** and when it is **declared**. During this period, the variable cannot be accessed. If we try to access it, JavaScript throws a **ReferenceError**. TDZ applies only to `let` and `const`, not to `var`.

---

## 🧠 Memory Trick

```text
Hoisted
   │
   ▼
🚫 TDZ 🚫
(No Access)
   │
   ▼
Declaration
   │
   ▼
✅ Access Allowed
```

Easy Rule:

> **TDZ = Hoisted but Not Accessible**

---

## ⭐ Keywords

- Temporal Dead Zone (TDZ)
- Hoisting
- `let`
- `const`
- ReferenceError
- Declaration
- Initialization
