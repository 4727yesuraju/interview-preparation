# 📚 `slice()` vs `splice()`

## 📖 Simple English Explanation

Both `slice()` and `splice()` are used to work with arrays, but they behave differently.

- **`slice()`** → Returns a **new array** without changing the original array.
- **`splice()`** → **Changes the original array** by adding, removing, or replacing elements.

---

## 🤔 Why is it Needed?

- **`slice()`** → Copy or extract part of an array.
- **`splice()`** → Modify an existing array.

---

## 🌊 Flow

```text
Array
  │
  ▼
Need Part of Array?
  │
  ├───────────────┐
  ▼               ▼
slice()        splice()
  │               │
New Array      Modify Original
Original Safe  Original Changes
```

---

## ✍️ Syntax

### `slice()`

```javascript
array.slice(start, end);
```

### `splice()`

```javascript
array.splice(start, deleteCount, item1, item2);
```

---

## 💻 Example

### Example 1: `slice()`

```javascript
const numbers = [10, 20, 30, 40, 50];

const result = numbers.slice(1, 4);

console.log(result);
console.log(numbers);
```

**Output**

```text
[20, 30, 40]
[10, 20, 30, 40, 50]
```

---

### Example 2: `splice()` (Remove)

```javascript
const numbers = [10, 20, 30, 40, 50];

numbers.splice(1, 2);

console.log(numbers);
```

**Output**

```text
[10, 40, 50]
```

---

### Example 3: `splice()` (Add)

```javascript
const numbers = [10, 20, 50];

numbers.splice(2, 0, 30, 40);

console.log(numbers);
```

**Output**

```text
[10, 20, 30, 40, 50]
```

---

### Example 4: `splice()` (Replace)

```javascript
const numbers = [10, 20, 30];

numbers.splice(1, 1, 100);

console.log(numbers);
```

**Output**

```text
[10, 100, 30]
```

---

## 🎤 Interview Answer (30 Seconds)

`slice()` returns a new array containing a portion of the original array without modifying it. `splice()` modifies the original array by adding, removing, or replacing elements. Use `slice()` when you want to keep the original array unchanged, and use `splice()` when you need to update the original array.

---

## 🧠 Memory Trick

```text
slice() 🍕
↓
Take a Piece

splice() ✂️
↓
Cut & Change
```

Easy Rule:

> **slice = Copy**

> **splice = Change**

---

## ⭐ Keywords

- slice()
- splice()
- Array
- Copy
- Modify
- Original Array
