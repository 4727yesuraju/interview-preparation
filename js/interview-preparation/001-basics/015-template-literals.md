# 📚 What are Template Literals?

## 📖 Simple English Explanation

**Template literals** are a modern way to create strings in JavaScript using **backticks (` `)** instead of single (`'`) or double (`"`) quotes.

They allow you to:

- Insert variables using **`${}`** (string interpolation).
- Write **multi-line strings** easily.
- Make string formatting more readable.

---

## 🤔 Why is it Needed?

- Makes string concatenation easier.
- Improves code readability.
- Supports multi-line strings without `\n`.

---

## 🌊 Flow

```text
Create a String
       │
       ▼
Use Backticks (` `)
       │
       ▼
Insert Variables
using ${}
       │
       ▼
Final String
```

---

## ✍️ Syntax

```javascript
let message = `Hello ${name}`;
```

---

## 💻 Example

### Example 1: String Interpolation

```javascript
let name = "John";

console.log(`Hello ${name}`);
```

**Output**

```text
Hello John
```

---

### Example 2: Multiple Variables

```javascript
let name = "John";
let age = 25;

console.log(`${name} is ${age} years old.`);
```

**Output**

```text
John is 25 years old.
```

---

### Example 3: Multi-line String

```javascript
let message = `Welcome
to
JavaScript`;

console.log(message);
```

**Output**

```text
Welcome
to
JavaScript
```

---

## 🎤 Interview Answer (30 Seconds)

Template literals are a feature introduced in **ES6** that use **backticks (` `)** to create strings. They support **string interpolation** using `${}` and **multi-line strings**, making the code more readable and easier to write than traditional string concatenation.

---

## 🧠 Memory Trick

```text
' ' or " "
       ❌

` `
       ✅
       │
       ▼
${} → Insert Variables
```

Easy Rule:

> **Backticks + `${}` = Template Literals**

---

## ⭐ Keywords

- Template Literals
- Backticks (` `)
- String Interpolation
- `${}`
- Multi-line Strings
- ES6
