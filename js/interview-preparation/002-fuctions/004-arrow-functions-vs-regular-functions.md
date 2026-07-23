# 📚 Arrow Functions vs Regular Functions

## 📖 Simple English Explanation

Both **Arrow Functions** and **Regular Functions** are used to create functions in JavaScript.

- **Regular Function** → Uses the `function` keyword and has its **own `this`**.
- **Arrow Function** → Uses the `=>` syntax and **inherits `this` from its surrounding scope (lexical `this`)**.

---

## 🤔 Why is it Needed?

- Regular functions are suitable for object methods and constructors.
- Arrow functions provide shorter syntax.
- Arrow functions are commonly used in callbacks and React.

---

## 🌊 Flow

```text
Need a Function
       │
       ▼
Choose Function Type
       │
 ┌─────┴─────┐
 │           │
 ▼           ▼
Regular     Arrow
Function    Function
```

---

## ✍️ Syntax

### Regular Function

```javascript
function add(a, b) {
  return a + b;
}
```

### Arrow Function

```javascript
const add = (a, b) => {
  return a + b;
};
```

Or

```javascript
const add = (a, b) => a + b;
```

---

## 💻 Example

### Example 1: Regular Function

```javascript
function greet(name) {
  return `Hello ${name}`;
}

console.log(greet("John"));
```

**Output**

```text
Hello John
```

---

### Example 2: Arrow Function

```javascript
const greet = (name) => `Hello ${name}`;

console.log(greet("John"));
```

**Output**

```text
Hello John
```

---

### Example 3: `this` Difference

```javascript
const person = {
  name: "John",

  regular() {
    console.log(this.name);
  },

  arrow: () => {
    console.log(this.name);
  },
};

person.regular(); // John
person.arrow(); // undefined
```

---

## 🎤 Interview Answer (30 Seconds)

Arrow functions are an ES6 feature that provides a shorter syntax for writing functions. The main difference is that **regular functions have their own `this`**, while **arrow functions inherit `this` from the surrounding scope (lexical `this`)**. Arrow functions are commonly used in callbacks and React, while regular functions are preferred for object methods and constructors.

---

## 🧠 Memory Trick

```text
Regular Function
↓
Own this 🧍

Arrow Function
↓
Parent's this 👨‍👩‍👧
```

Easy Rule:

> **Regular = Own `this`**

> **Arrow = Parent's `this`**

---

## ⭐ Keywords

- Arrow Function
- Regular Function
- ES6
- Lexical `this`
- `this`
- Callback
- Constructor
