# 📚 What is Object Destructuring?

## 📖 Simple English Explanation

**Object Destructuring** is an ES6 feature that lets you **extract properties from an object and store them in variables**.

Instead of accessing each property using `object.property`, you can extract them in a shorter way.

---

## 🤔 Why is it Needed?

- Makes code shorter and cleaner.
- Improves readability.
- Commonly used in React, API responses, and function parameters.

---

## 🌊 Flow

```text
Object
   │
   ▼
Destructure
   │
   ▼
Variables
```

---

## ✍️ Syntax

```javascript
const { property1, property2 } = object;
```

---

## 💻 Example

### Example 1: Basic Destructuring

```javascript
const person = {
  name: "John",
  age: 25,
};

const { name, age } = person;

console.log(name);
console.log(age);
```

**Output**

```text
John
25
```

---

### Example 2: Rename Variables

```javascript
const person = {
  name: "John",
};

const { name: userName } = person;

console.log(userName);
```

**Output**

```text
John
```

---

### Example 3: Default Value

```javascript
const person = {
  name: "John",
};

const { name, city = "Hyderabad" } = person;

console.log(name);
console.log(city);
```

**Output**

```text
John
Hyderabad
```

---

## 🎤 Interview Answer (30 Seconds)

Object destructuring is an ES6 feature that allows us to extract properties from an object into separate variables using a concise syntax. It makes code cleaner, more readable, and is commonly used in React components, API responses, and function parameters.

---

## 🧠 Memory Trick

```text
Object
  │
  ▼
Take Properties
  │
  ▼
Store in Variables
```

Easy Rule:

> **Destructuring = Unpacking an Object**

---

## ⭐ Keywords

- Object Destructuring
- ES6
- Object Properties
- Variable Extraction
- Default Values
- Renaming
