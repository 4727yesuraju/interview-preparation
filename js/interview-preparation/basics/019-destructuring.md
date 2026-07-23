# 📚 What is Destructuring?

## 📖 Simple English Explanation

**Destructuring** is an ES6 feature that allows you to **extract values** from **arrays** or **objects** and store them in separate variables.

It makes the code **shorter, cleaner, and easier to read**.

---

## 🤔 Why is it Needed?

- Reduces repetitive code.
- Makes it easy to access array and object values.
- Improves code readability.

---

## 🌊 Flow

```text
Array / Object
       │
       ▼
Use Destructuring
       │
       ▼
Extract Values
       │
       ▼
Store in Variables
```

---

## ✍️ Syntax

### Array Destructuring

```javascript
const [a, b] = array;
```

### Object Destructuring

```javascript
const { name, age } = object;
```

---

## 💻 Example

### Example 1: Array Destructuring

```javascript
const colors = ["Red", "Green", "Blue"];

const [first, second] = colors;

console.log(first);
console.log(second);
```

**Output**

```text
Red
Green
```

---

### Example 2: Object Destructuring

```javascript
const user = {
  name: "John",
  age: 25,
};

const { name, age } = user;

console.log(name);
console.log(age);
```

**Output**

```text
John
25
```

---

### Example 3: Rename Variables

```javascript
const user = {
  name: "John",
};

const { name: userName } = user;

console.log(userName);
```

**Output**

```text
John
```

---

## 🎤 Interview Answer (30 Seconds)

Destructuring is an ES6 feature that allows us to extract values from arrays or objects and assign them to separate variables in a single statement. It makes the code shorter, cleaner, and easier to read.

---

## 🧠 Memory Trick

```text
Array / Object
       │
       ▼
Take Out Values
       │
       ▼
Store in Variables
```

Easy Rule:

> **Destructuring = Extract Values**

---

## ⭐ Keywords

- Destructuring
- ES6
- Array
- Object
- Extract
- Variables
- Readability
