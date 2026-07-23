# 📚 What are the Data Types in JavaScript?

## 📖 Simple English Explanation

A **data type** defines the kind of value that a variable can store.

JavaScript has **8 data types**, divided into **2 categories**:

- **Primitive Data Types** (7)
- **Non-Primitive (Reference) Data Type** (1)

---

## 🤔 Why is it Needed?

- To store different types of data.
- To perform operations correctly.
- To help JavaScript understand how to handle different values.

---

## 🌊 Flow

```text
JavaScript Data Types
          │
          ├───────────────┐
          │               │
          ▼               ▼
 Primitive           Non-Primitive
 (7 Types)             (1 Type)
          │               │
          ▼               ▼
String              Object
Number
Boolean
Undefined
Null
BigInt
Symbol
```

---

## ✍️ Syntax

```javascript
let name = "John"; // String
let age = 25; // Number
let isStudent = true; // Boolean
let city; // Undefined
let person = null; // Null
let id = 123n; // BigInt
let unique = Symbol(); // Symbol

let user = {
  // Object
  name: "John",
};
```

---

## 💻 Example

```javascript
let name = "John"; // String
let age = 25; // Number
let isActive = true; // Boolean

console.log(typeof name); // string
console.log(typeof age); // number
console.log(typeof isActive); // boolean
```

---

## 🎤 Interview Answer (30 Seconds)

JavaScript has **8 data types**. They are divided into **Primitive** and **Non-Primitive** data types. The **7 Primitive** types are **String, Number, Boolean, Undefined, Null, BigInt, and Symbol**. The only **Non-Primitive** data type is **Object**, which includes objects, arrays, and functions.

---

## 🧠 Memory Trick

Remember:

```text
Primitive (7)

S → String
N → Number
B → Boolean
U → Undefined
N → Null
B → BigInt
S → Symbol

Object → Everything Else
```

Easy sentence:

> **"SNB UNBS + Object"**

Or simply remember:

```text
Primitive → Stores a single value

Object → Stores a collection of values
```

---

## ⭐ Keywords

- Data Type
- Primitive
- Non-Primitive
- String
- Number
- Boolean
- Undefined
- Null
- BigInt
- Symbol
- Object
- Reference Type
