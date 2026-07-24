# 📚 What is Currying?

## 📖 Simple English Explanation

**Currying** is a technique where a function with **multiple parameters** is converted into a **series of functions**, each taking **one parameter**.

Instead of:

```javascript
add(2, 3);
```

We write:

```javascript
add(2)(3);
```

---

## 🤔 Why is it Needed?

- Makes functions reusable.
- Allows partial application of arguments.
- Creates specialized functions.
- Commonly used in functional programming.

---

## 🌊 Flow

```text
One Function
(2 Parameters)
       │
       ▼
Split into
Multiple Functions
       │
       ▼
Each Function
Takes One Parameter
```

---

## ✍️ Syntax

```javascript
function add(a) {
  return function (b) {
    return a + b;
  };
}
```

---

## 💻 Example

### Example 1: Basic Currying

```javascript
function add(a) {
  return function (b) {
    return a + b;
  };
}

console.log(add(2)(3));
```

**Output**

```text
5
```

---

### Example 2: Reusable Function

```javascript
function multiply(a) {
  return function (b) {
    return a * b;
  };
}

const double = multiply(2);

console.log(double(10));
```

**Output**

```text
20
```

---

### Example 3: Arrow Function

```javascript
const add = (a) => (b) => a + b;

console.log(add(10)(20));
```

**Output**

```text
30
```

---

## 🎤 Interview Answer (30 Seconds)

Currying is a functional programming technique where a function that takes multiple arguments is transformed into a series of functions, each accepting one argument. It improves code reusability, supports partial application, and helps create specialized functions.

---

## 🧠 Memory Trick

```text
Normal Function

add(a, b)

        │
        ▼

Curried Function

add(a)(b)
```

Easy Rule:

> **One Parameter per Function = Currying**

---

## ⭐ Keywords

- Currying
- Higher-Order Function
- Function Returning Function
- Functional Programming
- Partial Application
- Reusability
