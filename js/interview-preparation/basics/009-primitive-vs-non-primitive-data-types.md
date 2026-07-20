# 📚 Primitive vs Non-Primitive Data Types

## 📖 Simple English Explanation

JavaScript data types are divided into **two categories**:

1. **Primitive Data Types** → Store a **single value** and are **immutable** (cannot be changed).
2. **Non-Primitive Data Types** → Store **multiple values or complex data** and are **mutable** (can be changed).

There are **7 Primitive** data types and **1 Non-Primitive** data type (**Object**). Arrays and functions are also objects in JavaScript.

---

## 🤔 Why is it Needed?

- To store different kinds of data.
- Primitive types are used for simple values.
- Non-Primitive types are used for complex data like objects, arrays, and functions.

---

## 🌊 Flow

```text
JavaScript Data Types
          │
     ┌────┴────┐
     │         │
     ▼         ▼
Primitive   Non-Primitive
 (7 Types)    (Object)
     │           │
     ▼           ▼
Single Value  Collection of Values
Immutable     Mutable
```

---

## ✍️ Syntax

```javascript
// Primitive
let name = "John";
let age = 25;

// Non-Primitive
let user = {
  name: "John",
  age: 25,
};
```

---

## 💻 Example

```javascript
// Primitive
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20

// Non-Primitive
let obj1 = { name: "John" };
let obj2 = obj1;

obj2.name = "David";

console.log(obj1.name); // David
console.log(obj2.name); // David
```

---

## 🎤 Interview Answer (30 Seconds)

JavaScript data types are divided into **Primitive** and **Non-Primitive** types.

Primitive data types store **single values** and are **immutable**. They include **String, Number, Boolean, Undefined, Null, BigInt, and Symbol**.

The only Non-Primitive data type is **Object**, which includes **objects, arrays, and functions**. Non-Primitive data types are **mutable** and are stored by **reference**.

---

## 🧠 Memory Trick

```text
Primitive
↓
Single Value
Immutable

Non-Primitive
↓
Object
Collection of Values
Mutable
```

Easy Rule:

> **Primitive → Value**
>
> **Non-Primitive → Reference**

---

## ⭐ Keywords

- Primitive
- Non-Primitive
- Object
- Immutable
- Mutable
- Value
- Reference
- String
- Number
- Boolean
- Undefined
- Null
- BigInt
- Symbol
