# 📚 `filter()` vs `find()`

## 📖 Simple English Explanation

Both `filter()` and `find()` are used to **search elements in an array**.

- **`filter()`** → Returns **all matching elements** as a **new array**.
- **`find()`** → Returns **only the first matching element**.

---

## 🤔 Why is it Needed?

- `filter()` → Use when you need **multiple matching items**.
- `find()` → Use when you need **only the first matching item**.

---

## 🌊 Flow

```text
Array
  │
  ▼
Search Condition
  │
  ├───────────────┐
  ▼               ▼
filter()       find()
  │               │
All Matches    First Match
  │               │
New Array      Single Value
```

---

## ✍️ Syntax

### `filter()`

```javascript
const result = array.filter((item) => condition);
```

### `find()`

```javascript
const result = array.find((item) => condition);
```

---

## 💻 Example

### Example 1: `filter()`

```javascript
const numbers = [10, 20, 30, 40];

const result = numbers.filter((num) => num > 20);

console.log(result);
```

**Output**

```text
[30, 40]
```

---

### Example 2: `find()`

```javascript
const numbers = [10, 20, 30, 40];

const result = numbers.find((num) => num > 20);

console.log(result);
```

**Output**

```text
30
```

---

### Example 3: User Search

```javascript
const users = [
  { id: 1, name: "John" },
  { id: 2, name: "Alice" },
  { id: 3, name: "John" },
];

console.log(users.filter((user) => user.name === "John"));

console.log(users.find((user) => user.name === "John"));
```

**Output**

```text
[
  { id: 1, name: "John" },
  { id: 3, name: "John" }
]

{ id: 1, name: "John" }
```

---

## 🎤 Interview Answer (30 Seconds)

Both `filter()` and `find()` search an array based on a condition. `filter()` returns all matching elements as a new array, while `find()` returns only the first matching element. If no match is found, `filter()` returns an empty array, whereas `find()` returns `undefined`.

---

## 🧠 Memory Trick

```text
filter() 🧺
↓
Collect All

find() 🔍
↓
Find First
```

Easy Rule:

> **filter = All Matches**

> **find = First Match**

---

## ⭐ Keywords

- filter()
- find()
- Search
- Array
- First Match
- All Matches
