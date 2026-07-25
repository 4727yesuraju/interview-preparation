# 📚 `some()` vs `every()`

## 📖 Simple English Explanation

Both `some()` and `every()` are used to **check whether array elements satisfy a condition**.

- **`some()`** → Returns `true` if **at least one** element satisfies the condition.
- **`every()`** → Returns `true` only if **all** elements satisfy the condition.

---

## 🤔 Why is it Needed?

- `some()` → Check if at least one element matches.
- `every()` → Check if all elements match.
- Makes validation and condition checking easy.

---

## 🌊 Flow

```text
Array
  │
  ▼
Check Condition
  │
  ├───────────────┐
  ▼               ▼
some()         every()
  │               │
One Match?     All Match?
  │               │
true/false    true/false
```

---

## ✍️ Syntax

### `some()`

```javascript
const result = array.some((item) => condition);
```

### `every()`

```javascript
const result = array.every((item) => condition);
```

---

## 💻 Example

### Example 1: `some()`

```javascript
const numbers = [10, 20, 30, 40];

const result = numbers.some((num) => num > 25);

console.log(result);
```

**Output**

```text
true
```

---

### Example 2: `every()`

```javascript
const numbers = [10, 20, 30, 40];

const result = numbers.every((num) => num > 25);

console.log(result);
```

**Output**

```text
false
```

---

### Example 3: Student Marks

```javascript
const marks = [80, 75, 90];

console.log(marks.some((mark) => mark < 35));

console.log(marks.every((mark) => mark >= 35));
```

**Output**

```text
false
true
```

---

## 🎤 Interview Answer (30 Seconds)

Both `some()` and `every()` check whether array elements satisfy a condition. `some()` returns `true` if at least one element matches, while `every()` returns `true` only if every element matches. Both methods return a boolean value.

---

## 🧠 Memory Trick

```text
some()
↓
Someone ✔️

every()
↓
Everyone ✔️
```

Easy Rule:

> **some = At Least One**

> **every = All**

---

## ⭐ Keywords

- some()
- every()
- Boolean
- Condition
- Array
- Validation
