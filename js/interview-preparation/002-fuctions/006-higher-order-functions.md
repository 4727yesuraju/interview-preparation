# 📚 What are Higher-Order Functions?

## 📖 Simple English Explanation

A **Higher-Order Function (HOF)** is a function that **takes another function as an argument** or **returns another function**.

Since JavaScript treats functions as **first-class objects**, functions can be passed and returned just like variables.

---

## 🤔 Why is it Needed?

- Makes code reusable.
- Reduces duplicate code.
- Helps write clean and functional programming code.
- Used in methods like `map()`, `filter()`, and `reduce()`.

---

## 🌊 Flow

```text
Higher-Order Function
          │
          ▼
Receives a Function
or
Returns a Function
          │
          ▼
Executes the Function
```

---

## ✍️ Syntax

```javascript
function higherOrder(callback) {
  callback();
}
```

---

## 💻 Example

### Example 1: Function as Argument

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

### Example 2: Function Returning Another Function

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

### Example 3: `map()` is a Higher-Order Function

```javascript
const numbers = [1, 2, 3];

const result = numbers.map((num) => num * 2);

console.log(result);
```

**Output**

```text
[2, 4, 6]
```

---

## 🎤 Interview Answer (30 Seconds)

A **Higher-Order Function** is a function that either **accepts another function as an argument** or **returns another function**. JavaScript supports higher-order functions because functions are first-class objects. Common examples include `map()`, `filter()`, `reduce()`, and `forEach()`.

---

## 🧠 Memory Trick

```text
Higher-Order Function
        │
        ├── Takes Function
        │
        └── Returns Function
```

Easy Rule:

> **Function + Function = Higher-Order Function**

---

## ⭐ Keywords

- Higher-Order Function
- Callback Function
- First-Class Function
- `map()`
- `filter()`
- `reduce()`
- Function as Argument
- Function as Return Value
