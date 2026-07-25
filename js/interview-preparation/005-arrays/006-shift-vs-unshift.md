# 📚 `shift()` vs `unshift()`

## 📖 Simple English Explanation

Both `shift()` and `unshift()` work on the **beginning (start)** of an array.

- **`shift()`** → Removes the **first element** from an array.
- **`unshift()`** → Adds one or more elements to the **beginning** of an array.

Both methods **modify the original array**.

---

## 🤔 Why is it Needed?

- **`shift()`** → Remove the first element.
- **`unshift()`** → Add new elements at the beginning.
- Useful for queue operations (FIFO).

---

## 🌊 Flow

```text
Array
  │
  ▼
Need to Work at Beginning?
  │
  ├───────────────┐
  ▼               ▼
shift()       unshift()
  │               │
Remove First   Add First
```

---

## ✍️ Syntax

### `shift()`

```javascript
array.shift();
```

### `unshift()`

```javascript
array.unshift(element1, element2);
```

---

## 💻 Example

### Example 1: `shift()`

```javascript
const fruits = ["Apple", "Mango", "Orange"];

const removed = fruits.shift();

console.log(removed);
console.log(fruits);
```

**Output**

```text
Apple
["Mango", "Orange"]
```

---

### Example 2: `unshift()`

```javascript
const fruits = ["Mango", "Orange"];

fruits.unshift("Apple");

console.log(fruits);
```

**Output**

```text
["Apple", "Mango", "Orange"]
```

---

### Example 3: Add Multiple Elements

```javascript
const numbers = [3, 4];

numbers.unshift(1, 2);

console.log(numbers);
```

**Output**

```text
[1, 2, 3, 4]
```

---

## 🎤 Interview Answer (30 Seconds)

`shift()` removes the first element from an array and returns it. `unshift()` adds one or more elements to the beginning of an array and returns the new length. Both methods modify the original array.

---

## 🧠 Memory Trick

```text
shift() ⬅️
↓
Remove First

unshift() ➕
↓
Add First
```

Easy Rule:

> **shift = Remove First**

> **unshift = Add First**

---

## ⭐ Keywords

- shift()
- unshift()
- Array
- First Element
- Remove
- Add
- Original Array
