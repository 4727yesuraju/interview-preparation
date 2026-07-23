# 📚 Function Declaration vs Function Expression

## 📖 Simple English Explanation

Both **Function Declaration** and **Function Expression** are used to create functions in JavaScript.

- **Function Declaration** → Function is declared using the `function` keyword with a function name.
- **Function Expression** → Function is created and assigned to a variable.

---

## 🤔 Why is it Needed?

- Both are used to write reusable code.
- Function Expressions are useful when passing functions as values (callbacks, event handlers).
- Function Declarations are simple and easy to read.

---

## 🌊 Flow

```text
Need a Function
       │
       ▼
Choose a Type
       │
 ┌─────┴─────┐
 │           │
 ▼           ▼
Function    Function
Declaration Expression
```

---

## ✍️ Syntax

### Function Declaration

```javascript
function greet() {
  console.log("Hello");
}
```

### Function Expression

```javascript
const greet = function () {
  console.log("Hello");
};
```

---

## 💻 Example

### Example 1: Function Declaration

```javascript
function add(a, b) {
  return a + b;
}

console.log(add(10, 20));
```

**Output**

```text
30
```

---

### Example 2: Function Expression

```javascript
const add = function (a, b) {
  return a + b;
};

console.log(add(10, 20));
```

**Output**

```text
30
```

---

### Example 3: Hoisting Difference

```javascript
// Function Declaration
greet();

function greet() {
  console.log("Hello");
}
```

**Output**

```text
Hello
```

```javascript
// Function Expression
greet();

const greet = function () {
  console.log("Hello");
};
```

**Output**

```text
ReferenceError
```

---

## 🎤 Interview Answer (30 Seconds)

A **Function Declaration** defines a named function using the `function` keyword and is **fully hoisted**, so it can be called before its declaration.

A **Function Expression** stores a function inside a variable. It is **not fully hoisted**, so it **cannot be called before the variable is initialized**.

---

## 🧠 Memory Trick

```text
Function Declaration
↓
Create Function
↓
Can Call Before Declaration ✅

Function Expression
↓
Store Function in Variable
↓
Call Only After Assignment ✅
```

Easy Rule:

> **Declaration = Directly Create**

> **Expression = Store in Variable**

---

## ⭐ Keywords

- Function Declaration
- Function Expression
- Hoisting
- Named Function
- Anonymous Function
- Variable
- ES6
