# 📚 What is a Callback Function?

## 📖 Simple English Explanation

A **callback function** is a **function that is passed as an argument to another function**.

The callback function is **executed later**, usually after another task or operation is completed.

---

## 🤔 Why is it Needed?

- To execute code after a task finishes.
- Used in asynchronous operations like API calls, file reading, and timers.
- Makes code more flexible and reusable.

---

## 🌊 Flow

```text
Function A Calls Function B
          │
          ▼
Pass Callback Function
          │
          ▼
Function B Completes Its Task
          │
          ▼
Execute Callback Function
```

---

## ✍️ Syntax

```javascript
function main(callback) {
  callback();
}
```

---

## 💻 Example

### Example 1: Simple Callback

```javascript
function greet(name) {
  console.log(`Hello ${name}`);
}

function processUser(callback) {
  callback("John");
}

processUser(greet);
```

**Output**

```text
Hello John
```

---

### Example 2: Callback with `setTimeout`

```javascript
setTimeout(() => {
  console.log("Executed after 2 seconds");
}, 2000);
```

**Output**

```text
Executed after 2 seconds
```

---

### Example 3: Callback with Array Method

```javascript
const numbers = [1, 2, 3];

numbers.forEach(function (num) {
  console.log(num);
});
```

**Output**

```text
1
2
3
```

---

## 🎤 Interview Answer (30 Seconds)

A **callback function** is a function that is **passed as an argument to another function** and is **executed later** after a specific task is completed. Callback functions are commonly used in asynchronous operations like API calls, timers, event handling, and array methods such as `forEach()`, `map()`, and `filter()`.

---

## 🧠 Memory Trick

```text
Function A
    │
Pass Callback
    │
    ▼
Task Completes
    │
    ▼
Callback Executes
```

Easy Rule:

> **Callback = "Call Me Back Later" 📞**

---

## ⭐ Keywords

- Callback Function
- Function as Argument
- Asynchronous
- `setTimeout()`
- Event Handling
- `forEach()`
- `map()`
- `filter()`
