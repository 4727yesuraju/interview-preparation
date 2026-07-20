# 📚 What is the `typeof` Operator?

## 📖 Simple English Explanation

The **`typeof`** operator is used to **check the data type** of a value or variable.

It returns the data type as a **string**, such as `"string"`, `"number"`, or `"boolean"`.

---

## 🤔 Why is it Needed?

- To identify the data type of a variable.
- Helps write type-safe code.
- Useful for debugging and validation.

---

## 🌊 Flow

```text
Variable or Value
        │
        ▼
Apply typeof
        │
        ▼
Returns Data Type
(String, Number, Boolean, etc.)
```

---

## ✍️ Syntax

```javascript
typeof value;
```

---

## 💻 Example

```javascript
console.log(typeof "Hello"); // "string"
console.log(typeof 100); // "number"
console.log(typeof true); // "boolean"
console.log(typeof undefined); // "undefined"
console.log(typeof null); // "object"
console.log(typeof {}); // "object"
console.log(typeof []); // "object"
console.log(typeof function () {}); // "function"
```

---

## 🎤 Interview Answer (30 Seconds)

The **`typeof`** operator is used to determine the data type of a value or variable. It returns the type as a string, such as `"string"`, `"number"`, or `"boolean"`. It is commonly used for debugging, validation, and checking variable types before performing operations.

---

## 🧠 Memory Trick

```text
typeof
   │
   ▼
"Tell me the Type"
```

Remember:

> **`typeof` = Check the Data Type**

---

## ⭐ Keywords

- `typeof`
- Data Type
- String
- Number
- Boolean
- Undefined
- Object
- Function
