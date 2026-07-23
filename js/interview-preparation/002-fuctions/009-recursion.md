# 📚 What is Recursion?

## 📖 Simple English Explanation

**Recursion** is a technique where a **function calls itself** to solve a problem.

A recursive function **keeps calling itself until a stopping condition (base case) is reached**.

Without a base case, the function will keep calling itself forever and cause a **Stack Overflow** error.

---

## 🤔 Why is it Needed?

- Solves problems that can be broken into smaller, similar problems.
- Makes some algorithms simpler and cleaner.
- Commonly used in tree traversal, file systems, and factorial calculations.

---

## 🌊 Flow

```text
Function Called
      │
      ▼
Calls Itself
      │
      ▼
Base Case Reached?
      │
 ┌────┴────┐
 │         │
 No       Yes
 │         │
 ▼         ▼
Call      Stop
Again     Return Result
```

---

## ✍️ Syntax

```javascript
function recursiveFunction() {
  if (baseCondition) {
    return;
  }

  recursiveFunction();
}
```

---

## 💻 Example

### Example 1: Factorial

```javascript
function factorial(n) {
  if (n === 1) {
    return 1;
  }

  return n * factorial(n - 1);
}

console.log(factorial(5));
```

**Output**

```text
120
```

---

### Example 2: Countdown

```javascript
function countdown(n) {
  if (n === 0) {
    console.log("Done!");
    return;
  }

  console.log(n);
  countdown(n - 1);
}

countdown(3);
```

**Output**

```text
3
2
1
Done!
```

---

### Example 3: Infinite Recursion (❌)

```javascript
function test() {
  test();
}

test();
```

**Output**

```text
RangeError: Maximum call stack size exceeded
```

---

## 🎤 Interview Answer (30 Seconds)

Recursion is a programming technique where a function calls itself to solve a problem. It continues calling itself until it reaches a **base case**, which stops the recursion. Without a base case, recursion results in a **Stack Overflow** error.

---

## 🧠 Memory Trick

```text
Function
   │
   ▼
Calls Itself
   │
   ▼
Base Case?
   │
 ┌─┴─┐
 │   │
No  Yes
 │   │
 ▼   ▼
Again Stop
```

Easy Rule:

> **Recursion = Function Calls Itself Until the Base Case**

---

## ⭐ Keywords

- Recursion
- Recursive Function
- Base Case
- Call Stack
- Stack Overflow
- Function Calls Itself
