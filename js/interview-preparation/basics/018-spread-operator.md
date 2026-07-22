# 📚 What is the Spread Operator (`...`)?

## 📖 Simple English Explanation

The **Spread Operator (`...`)** is used to **expand** an array, object, or iterable into **individual elements**.

It is commonly used to:

- Copy arrays or objects.
- Merge arrays or objects.
- Pass array elements as function arguments.

---

## 🤔 Why is it Needed?

- Creates copies of arrays and objects.
- Merges arrays and objects easily.
- Makes code shorter and more readable.
- Passes array values as separate function arguments.

---

## 🌊 Flow

```text
Array / Object
       │
       ▼
Use ...
       │
       ▼
Expands into
Individual Elements
```

---

## ✍️ Syntax

```javascript
const newArray = [...array];

const newObject = { ...object };
```

---

## 💻 Example

### Example 1: Copy an Array

```javascript
const numbers = [10, 20, 30];

const copy = [...numbers];

console.log(copy);
```

**Output**

```text
[10, 20, 30]
```

---

### Example 2: Merge Arrays

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];

const result = [...arr1, ...arr2];

console.log(result);
```

**Output**

```text
[1, 2, 3, 4]
```

---

### Example 3: Pass Array as Function Arguments

```javascript
function sum(a, b, c) {
  return a + b + c;
}

const nums = [10, 20, 30];

console.log(sum(...nums));
```

**Output**

```text
60
```

---

## 🎤 Interview Answer (30 Seconds)

The **Spread Operator (`...`)** is an ES6 feature used to **expand** an array, object, or iterable into individual elements. It is commonly used to copy arrays or objects, merge them, and pass array elements as function arguments.

---

## 🧠 Memory Trick

```text
Spread
   │
   ▼
Expand 📤
```

Easy Rule:

> **Spread = Expand**

> **Rest = Collect**

---

## ⭐ Keywords

- Spread Operator
- `...`
- ES6
- Expand
- Array
- Object
- Copy
- Merge
- Iterable
