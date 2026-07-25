# 📚 Remove Duplicates from an Array

## 📖 Simple English Explanation

Removing duplicates means **keeping only unique values** in an array.

Example:

```javascript
[1, 2, 2, 3, 3, 4];
```

becomes

```javascript
[1, 2, 3, 4];
```

---

## 🤔 Why is it Needed?

- Remove repeated values.
- Clean API or database data.
- Improve data quality.

---

## 🌊 Flow

```text
Original Array

[1, 2, 2, 3, 3, 4]
        │
        ▼
Remove Duplicates
        │
        ▼
[1, 2, 3, 4]
```

---

## ✍️ Syntax

### Using `Set` (Recommended)

```javascript
const uniqueArray = [...new Set(array)];
```

---

## 💻 Example

### Example 1: Using `Set` ✅

```javascript
const numbers = [1, 2, 2, 3, 3, 4];

const unique = [...new Set(numbers)];

console.log(unique);
```

**Output**

```text
[1, 2, 3, 4]
```

---

### Example 2: Using `filter()`

```javascript
const numbers = [1, 2, 2, 3, 3, 4];

const unique = numbers.filter((item, index) => numbers.indexOf(item) === index);

console.log(unique);
```

**Output**

```text
[1, 2, 3, 4]
```

---

### Example 3: Remove Duplicate Strings

```javascript
const fruits = ["Apple", "Mango", "Apple", "Orange"];

const unique = [...new Set(fruits)];

console.log(unique);
```

**Output**

```text
["Apple", "Mango", "Orange"]
```

---

## 🎤 Interview Answer (30 Seconds)

The easiest way to remove duplicates from an array is by using a `Set`, because a `Set` stores only unique values. We can convert the array to a `Set` and then convert it back to an array using the spread operator.

---

## 🧠 Memory Trick

```text
Array
 │
 ▼
Set
 │
 ▼
Unique Values
```

Easy Rule:

> **Set = No Duplicates**

---

## ⭐ Keywords

- Set
- Unique Values
- Spread Operator (`...`)
- filter()
- indexOf()
- Duplicates
