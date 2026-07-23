# 📚 What are Arrow Functions?

## 📖 Simple English Explanation

**Arrow Functions** are a shorter way to write functions in JavaScript, introduced in **ES6**.

They use the **arrow (`=>`)** syntax instead of the `function` keyword.

Arrow functions make code cleaner and are commonly used in modern JavaScript and React.

---

## 🤔 Why is it Needed?

- Shorter and cleaner syntax.
- Easier to read and write.
- Commonly used in callbacks and array methods.
- Does not have its own `this` (important interview point).

---

## 🌊 Flow

```text
Need a Function
       │
       ▼
Use =>
       │
       ▼
Execute Logic
       │
       ▼
Return Result
```

---

## ✍️ Syntax

### Normal Function

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

---

## 💻 Example

### Example 1: Basic Arrow Function

```javascript
const greet = () => {
  console.log("Hello");
};

greet();
```

**Output**

```text
Hello
```

---

### Example 2: Parameters

```javascript
const add = (a, b) => {
  return a + b;
};

console.log(add(10, 20));
```

**Output**

```text
30
```

---

### Example 3: Implicit Return

```javascript
const add = (a, b) => a + b;

console.log(add(10, 20));
```

**Output**

```text
30
```

---

## 🎤 Interview Answer (30 Seconds)

Arrow Functions are an ES6 feature that provides a shorter syntax for writing functions using the `=>` operator. They make code more concise and do not have their own `this`, instead inheriting `this` from the surrounding scope.

---

## 🧠 Memory Trick

```text
function
   ↓

() => {}
```

Easy Rule:

> **Arrow Function = Short Function**

---

## ⭐ Keywords

- Arrow Function
- ES6
- `=>`
- Short Syntax
- Implicit Return
- Lexical `this`
