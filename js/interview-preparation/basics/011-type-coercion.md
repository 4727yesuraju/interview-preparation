# 📚 What is Type Coercion?

## 📖 Simple English Explanation

**Type Coercion** is the automatic conversion of one data type to another by JavaScript.

JavaScript does this when different data types are used together in operations or comparisons.

For example, if you add a **number** and a **string**, JavaScript automatically converts the number into a string.

---

## 🤔 Why is it Needed?

- To allow operations between different data types.
- Makes JavaScript more flexible.
- Reduces the need for manual type conversion.

---

## 🌊 Flow

```text
Different Data Types
        │
        ▼
JavaScript detects them
        │
        ▼
Automatically converts
one data type
        │
        ▼
Performs the operation
```

---

## ✍️ Syntax

```javascript
5 + "5";
```

---

## 💻 Example

```javascript
console.log(5 + "5"); // "55"
console.log("10" - 5); // 5
console.log(true + 1); // 2
console.log(false + 1); // 1
console.log(null == undefined); // true
```

---

## 🎤 Interview Answer (30 Seconds)

Type coercion is the automatic conversion of one data type to another by JavaScript. It happens when different data types are used together in operations or comparisons. For example, `5 + "5"` returns `"55"` because JavaScript converts the number `5` into a string.

---

## 🧠 Memory Trick

```text
Different Types
       │
       ▼
JavaScript Converts
       │
       ▼
Operation Continues
```

Remember:

> **Type Coercion = Automatic Type Conversion**

---

## ⭐ Keywords

- Type Coercion
- Automatic Conversion
- String
- Number
- Boolean
- `==`
- `===`
- Implicit Conversion
