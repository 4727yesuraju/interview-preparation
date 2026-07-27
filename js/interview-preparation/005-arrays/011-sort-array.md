# 📚 Sort an Array

## 📖 Simple English Explanation

Sorting an array means **arranging its elements in a specific order**.

The order can be:

- Ascending (Small → Large)
- Descending (Large → Small)
- Alphabetical (A → Z)

JavaScript provides the **`sort()`** method to sort arrays.

---

## 🤔 Why is it Needed?

- Display data in order.
- Sort names alphabetically.
- Sort prices, marks, or dates.
- Improve data readability.

---

## 🌊 Flow

```text
Original Array

[30, 10, 20]
      │
      ▼
sort()
      │
      ▼
[10, 20, 30]
```

---

## ✍️ Syntax

### Default Sort

```javascript
array.sort();
```

### Ascending Numbers

```javascript
array.sort((a, b) => a - b);
```

### Descending Numbers

```javascript
array.sort((a, b) => b - a);
```

---

## 💻 Example

### Example 1: Sort Strings

```javascript
const fruits = ["Orange", "Apple", "Mango"];

fruits.sort();

console.log(fruits);
```

**Output**

```text
["Apple", "Mango", "Orange"]
```

---

### Example 2: Sort Numbers (Ascending)

```javascript
const numbers = [30, 10, 20];

numbers.sort((a, b) => a - b);

console.log(numbers);
```

**Output**

```text
[10, 20, 30]
```

---

### Example 3: Sort Numbers (Descending)

```javascript
const numbers = [30, 10, 20];

numbers.sort((a, b) => b - a);

console.log(numbers);
```

**Output**

```text
[30, 20, 10]
```

---

## 🎤 Interview Answer (30 Seconds)

`sort()` is used to arrange array elements in a specific order. By default, it sorts elements as strings. For numbers, we use a compare function like `(a, b) => a - b` for ascending order and `(a, b) => b - a` for descending order.

---

## 🧠 Memory Trick

```text
Ascending
a - b ⬆️

Descending
b - a ⬇️
```

Easy Rule:

> **a - b = Small → Large**

> **b - a = Large → Small**

---

## ⭐ Keywords

- sort()
- Ascending
- Descending
- Compare Function
- a - b
- b - a

```

```
