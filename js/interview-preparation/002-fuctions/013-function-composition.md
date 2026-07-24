# 📚 What is Function Composition?

## 📖 Simple English Explanation

**Function Composition** is a technique where the **output of one function becomes the input of another function**.

Instead of calling functions separately, we **combine multiple functions** to perform a task step by step.

---

## 🤔 Why is it Needed?

- Makes code reusable.
- Breaks complex logic into small functions.
- Improves readability and maintainability.

---

## 🌊 Flow

```text
Input
  │
  ▼
Function A
  │
(Output)
  │
  ▼
Function B
  │
(Output)
  │
  ▼
Final Result
```

---

## ✍️ Syntax

```javascript
const result = functionB(functionA(value));
```

---

## 💻 Example

### Example 1: Basic Function Composition

```javascript
function double(num) {
  return num * 2;
}

function square(num) {
  return num * num;
}

const result = square(double(5));

console.log(result);
```

**Output**

```text
100
```

**Flow:**

```text
5
↓
double()
↓
10
↓
square()
↓
100
```

---

### Example 2: Compose Multiple Functions

```javascript
function add2(num) {
  return num + 2;
}

function multiply3(num) {
  return num * 3;
}

console.log(multiply3(add2(4)));
```

**Output**

```text
18
```

---

### Example 3: Composition Helper

```javascript
const compose = (f, g) => (x) => f(g(x));

const double = (x) => x * 2;
const square = (x) => x * x;

const result = compose(square, double);

console.log(result(5));
```

**Output**

```text
100
```

---

## 🎤 Interview Answer (30 Seconds)

Function Composition is a technique where the output of one function becomes the input of another function. It allows us to combine small, reusable functions to build more complex functionality. This approach improves code readability, reusability, and maintainability.

---

## 🧠 Memory Trick

```text
Input
  │
  ▼
Function 1
  │
  ▼
Function 2
  │
  ▼
Function 3
  │
  ▼
Output
```

Easy Rule:

> **Output of one function = Input of the next function**

---

## ⭐ Keywords

- Function Composition
- Function Chaining
- Functional Programming
- Reusability
- Composition
- Higher-Order Function
