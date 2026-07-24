# 📚 Global Scope vs Local Scope

## 📖 Simple English Explanation

- **Global Scope** → A variable declared **outside all functions and blocks**. It can be accessed **from anywhere** in the program.

- **Local Scope** → A variable declared **inside a function or block**. It can be accessed **only within that function or block**.

---

## 🤔 Why is it Needed?

- Prevents variables from conflicting with each other.
- Protects data from being accessed everywhere.
- Makes code easier to understand and maintain.

---

## 🌊 Flow

```text
Variable Created
      │
      ▼
Where is it declared?
      │
 ┌────┴────┐
 │         │
Outside    Inside
Function   Function/Block
 │         │
 ▼         ▼
Global     Local
Scope      Scope
```

---

## ✍️ Syntax

### Global Scope

```javascript
let name = "John";
```

### Local Scope

```javascript
function greet() {
  let message = "Hello";
}
```

---

## 💻 Example

### Example 1: Global Scope

```javascript
let name = "John";

function greet() {
  console.log(name);
}

greet();
console.log(name);
```

**Output**

```text
John
John
```

---

### Example 2: Local Scope

```javascript
function greet() {
  let message = "Hello";

  console.log(message);
}

greet();

// console.log(message); // Error
```

**Output**

```text
Hello
```

---

### Example 3: Block Scope (Local Scope)

```javascript
if (true) {
  let age = 25;
  console.log(age);
}

// console.log(age); // Error
```

**Output**

```text
25
```

---

## 🎤 Interview Answer (30 Seconds)

Global scope means a variable is declared outside all functions and blocks, so it can be accessed from anywhere in the program. Local scope means a variable is declared inside a function or block, so it can only be accessed within that function or block. Using local scope helps avoid variable conflicts and keeps code organized.

---

## 🧠 Memory Trick

```text
Global 🌍
↓
Everywhere

Local 🏠
↓
Only Inside
```

Easy Rule:

> **Global = Everyone can access**

> **Local = Only family (function/block) can access**

---

## ⭐ Keywords

- Global Scope
- Local Scope
- Function Scope
- Block Scope
- Variable Visibility
- `let`
- `const`
- `var`
