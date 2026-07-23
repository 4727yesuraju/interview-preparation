# 📚 What is a Function?

## 📖 Simple English Explanation

A **function** is a **reusable block of code** that performs a specific task.

Instead of writing the same code multiple times, you write it once inside a function and call it whenever needed.

---

## 🤔 Why is it Needed?

- Avoids code duplication.
- Makes code reusable.
- Improves readability and maintainability.
- Breaks large programs into smaller, manageable pieces.

---

## 🌊 Flow

```text
Create Function
       │
       ▼
Call Function
       │
       ▼
Execute Code
       │
       ▼
Return Result (Optional)
```

---

## ✍️ Syntax

```javascript
function functionName(parameters) {
  // Code
  return value; // Optional
}
```

---

## 💻 Example

### Example 1: Simple Function

```javascript
function greet() {
  console.log("Hello");
}

greet();
```

**Output**

```text
Hello
```

---

### Example 2: Function with Parameters

```javascript
function greet(name) {
  console.log(`Hello ${name}`);
}

greet("John");
```

**Output**

```text
Hello John
```

---

### Example 3: Function with Return Value

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

## 🎤 Interview Answer (30 Seconds)

A **function** is a reusable block of code that performs a specific task. It can accept **parameters** as input, execute some logic, and optionally return a value. Functions help reduce code duplication and make programs easier to read, maintain, and reuse.

---

## 🧠 Memory Trick

```text
Function
   │
   ▼
Write Once
   │
   ▼
Use Many Times
```

Easy Rule:

> **Function = Reusable Block of Code**

---

## ⭐ Keywords

- Function
- Reusable
- Parameters
- Arguments
- Return
- Function Call
- Code Reusability
