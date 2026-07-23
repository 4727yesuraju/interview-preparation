# 📚 What is Optional Chaining (`?.`)?

## 📖 Simple English Explanation

**Optional Chaining (`?.`)** is an ES2020 feature that allows you to **safely access nested object properties or methods**.

If a property is `null` or `undefined`, JavaScript **stops the evaluation** and returns `undefined` instead of throwing an error.

---

## 🤔 Why is it Needed?

- Prevents runtime errors.
- Safely accesses nested object properties.
- Makes the code shorter and cleaner.
- Eliminates multiple `if` checks.

---

## 🌊 Flow

```text
Access Property
       │
       ▼
Does it exist?
       │
  ┌────┴────┐
  │         │
 Yes        No
  │         │
  ▼         ▼
Return     Return
Value      undefined
(No Error)
```

---

## ✍️ Syntax

```javascript
object?.property;

object?.method();

array?.[index];
```

---

## 💻 Example

### Example 1: Without Optional Chaining

```javascript
const user = null;

// ❌ Error
console.log(user.address.city);
```

---

### Example 2: With Optional Chaining

```javascript
const user = null;

console.log(user?.address?.city);
```

**Output**

```text
undefined
```

---

### Example 3: Method Call

```javascript
const user = {
  greet() {
    return "Hello";
  },
};

console.log(user?.greet());
```

**Output**

```text
Hello
```

---

## 🎤 Interview Answer (30 Seconds)

Optional Chaining (`?.`) is an ES2020 feature that safely accesses nested object properties or methods. If a property is `null` or `undefined`, JavaScript returns `undefined` instead of throwing an error. It helps write cleaner and safer code.

---

## 🧠 Memory Trick

```text
?.
 │
 ▼
Check First ✅

Exists?
 │
 ├── Yes → Return Value
 └── No  → undefined
```

Easy Rule:

> **`?.` = Check Before Access**

---

## ⭐ Keywords

- Optional Chaining
- `?.`
- ES2020
- Nested Objects
- `undefined`
- Safe Property Access
- Runtime Error
