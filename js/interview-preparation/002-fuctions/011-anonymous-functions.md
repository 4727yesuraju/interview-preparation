# 📚 What are Anonymous Functions?

## 📖 Simple English Explanation

An **Anonymous Function** is a **function without a name**.

It is usually assigned to a variable or passed directly as an argument to another function.

---

## 🤔 Why is it Needed?

- Used for short, one-time functions.
- Commonly used as callbacks.
- Keeps the code concise and readable.

---

## 🌊 Flow

```text
Create Function
      │
      ▼
No Function Name
      │
      ▼
Assign to Variable
or
Pass as Callback
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

### Example 2: Callback Function

```javascript
setTimeout(function () {
  console.log("Executed!");
}, 1000);
```

**Output**

```text
Executed!
```

---

### Example 3: `forEach()` Callback

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

An **Anonymous Function** is a function that **does not have a name**. It is commonly assigned to a variable or passed as a callback to another function. Anonymous functions are widely used in callbacks, event handlers, and array methods like `forEach()`, `map()`, and `filter()`.

---

## 🧠 Memory Trick

```text
Anonymous
      │
      ▼
No Name 🙈
```

Easy Rule:

> **Anonymous = No Name**

---

## ⭐ Keywords

- Anonymous Function
- Function Expression
- Callback
- No Name
- `setTimeout()`
- `forEach()`
- Function as Value
