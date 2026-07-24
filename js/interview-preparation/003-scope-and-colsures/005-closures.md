# 📚 What is a Closure?

## 📖 Simple English Explanation

A **Closure** is created when an **inner function remembers and can access the variables of its outer function**, even **after the outer function has finished executing**.

Closures are possible because of **lexical scope**.

---

## 🤔 Why is it Needed?

- Keeps data private.
- Remembers values between function calls.
- Used in callbacks, event handlers, and modules.
- Helps create private variables.

---

## 🌊 Flow

```text
Outer Function Runs
        │
        ▼
Creates Variable
        │
        ▼
Returns Inner Function
        │
        ▼
Outer Function Ends
        │
        ▼
Inner Function Still
Remembers Outer Variable ✅
```

---

## ✍️ Syntax

```javascript
function outer() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}
```

---

## 💻 Example

### Example 1: Basic Closure

```javascript
function outer() {
  let message = "Hello";

  return function () {
    console.log(message);
  };
}

const greet = outer();

greet();
```

**Output**

```text
Hello
```

---

### Example 2: Counter

```javascript
function counter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const increment = counter();

console.log(increment());
console.log(increment());
console.log(increment());
```

**Output**

```text
1
2
3
```

---

### Example 3: Private Variable

```javascript
function bankAccount() {
  let balance = 1000;

  return function () {
    return balance;
  };
}

const getBalance = bankAccount();

console.log(getBalance());
```

**Output**

```text
1000
```

---

## 🎤 Interview Answer (30 Seconds)

A **Closure** is a combination of a function and its lexical environment. It allows an inner function to access variables from its outer function even after the outer function has finished executing. Closures are commonly used for data privacy, callbacks, event handlers, and maintaining state.

---

## 🧠 Memory Trick

```text
Outer Function Ends
        │
        ▼
Inner Function
Still Remembers 🧠
Outer Variables
```

Easy Rule:

> **Closure = Remember Outer Variables**

---

## ⭐ Keywords

- Closure
- Lexical Scope
- Inner Function
- Outer Function
- Private Variables
- State
- Callback
