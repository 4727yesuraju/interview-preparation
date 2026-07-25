# 📚 `map()` vs `forEach()`

## 📖 Simple English Explanation

Both `map()` and `forEach()` are used to **loop through an array**.

- **`forEach()`** → Executes a function for each element but **does not return a new array**.
- **`map()`** → Executes a function for each element and **returns a new array**.

---

## 🤔 Why is it Needed?

- `forEach()` → Use when you only want to perform an action (e.g., print, update UI).
- `map()` → Use when you want to transform data and create a new array.

---

## 🌊 Flow

```text
Array
  │
  ▼
Loop Through Elements
  │
  ├───────────────┐
  ▼               ▼
forEach()       map()
  │               │
Action Only     Transform Data
  │               │
No Return      Returns New Array
```

---

## ✍️ Syntax

### `forEach()`

```javascript
array.forEach((item) => {
  // action
});
```

### `map()`

```javascript
const newArray = array.map((item) => {
  return item;
});
```

---

## 💻 Example

### Example 1: `forEach()`

```javascript
const numbers = [1, 2, 3];

numbers.forEach((num) => {
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

### Example 2: `map()`

```javascript
const numbers = [1, 2, 3];

const doubled = numbers.map((num) => num * 2);

console.log(doubled);
```

**Output**

```text
[2, 4, 6]
```

---

### Example 3: Return Value

```javascript
const numbers = [1, 2, 3];

const result1 = numbers.forEach((num) => num * 2);
const result2 = numbers.map((num) => num * 2);

console.log(result1);
console.log(result2);
```

**Output**

```text
undefined
[2, 4, 6]
```

---

## 🎤 Interview Answer (30 Seconds)

Both `map()` and `forEach()` iterate over arrays. The main difference is that `map()` returns a **new array** with transformed values, while `forEach()` only performs an action and returns `undefined`. Use `map()` when you need a new array and `forEach()` when you just need to iterate.

---

## 🧠 Memory Trick

```text
forEach()
↓
Do Something ✅

map()
↓
Create Something 🆕
```

Easy Rule:

> **forEach = Action**

> **map = Transformation**

---

## ⭐ Keywords

- map()
- forEach()
- Iteration
- New Array
- Transformation
- Callback
