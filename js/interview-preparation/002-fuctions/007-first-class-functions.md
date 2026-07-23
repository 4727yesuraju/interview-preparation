# 📚 What are First-Class Functions?

## 📖 Simple English Explanation

**First-Class Functions** mean that **functions are treated like any other value** in JavaScript.

This means a function can be:

- Assigned to a variable.
- Passed as an argument to another function.
- Returned from another function.

Because of this feature, JavaScript supports **Higher-Order Functions** and **Callbacks**.

---

## 🤔 Why is it Needed?

- Makes functions flexible.
- Enables callbacks and higher-order functions.
- Supports functional programming.
- Improves code reusability.

---

## 🌊 Flow

```text
Function
    │
    ▼
Treat Like a Value
    │
    ├── Store in Variable
    ├── Pass as Argument
    └── Return from Function
```

---

## ✍️ Syntax

```javascript
const greet = function () {
  console.log("Hello");
};
```

---

## 💻 Example

### Example 1: Assign to a Variable

```javascript
const greet = function () {
  console.log("Hello");
};

greet();
```

**Output**

```text
Hello
```

---

### Example 2: Pass as an Argument

```javascript
function greet() {
  console.log("Hello");
}

function execute(callback) {
  callback();
}

execute(greet);
```

**Output**

```text
Hello
```

---

### Example 3: Return a Function

```javascript
function multiply(x) {
  return function (y) {
    return x * y;
  };
}

const double = multiply(2);

console.log(double(5));
```

**Output**

```text
10
```

---

## 🎤 Interview Answer (30 Seconds)

First-Class Functions mean that functions are treated like any other value in JavaScript. They can be assigned to variables, passed as arguments, and returned from other functions. This feature enables callbacks, higher-order functions, and functional programming.

---

## 🧠 Memory Trick

```text
Function
   │
   ▼
Acts Like a Value
   │
   ├── Store
   ├── Pass
   └── Return
```

Easy Rule:

> **First-Class Function = Function behaves like a variable.**

---

## ⭐ Keywords

- First-Class Functions
- Function as Value
- Callback
- Higher-Order Function
- Function Variable
- Functional Programming
