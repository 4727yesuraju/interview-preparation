# 📚 Flatten an Array

## 📖 Simple English Explanation

**Flattening an array** means converting a **nested array** into a **single-level array**.

Example:

```javascript
[1, [2, 3], [4, 5]];
```

becomes

```javascript
[1, 2, 3, 4, 5];
```

---

## 🤔 Why is it Needed?

- Remove nested arrays.
- Make data easier to process.
- Common when working with API responses and nested data.

---

## 🌊 Flow

```text
Nested Array

[1, [2, 3], [4, 5]]
          │
          ▼
Flatten
          │
          ▼
[1, 2, 3, 4, 5]
```

---

## ✍️ Syntax

### Using `flat()`

```javascript
array.flat(depth);
```

---

## 💻 Example

### Example 1: Flatten One Level

```javascript
const arr = [1, [2, 3], [4, 5]];

console.log(arr.flat());
```

**Output**

```text
[1, 2, 3, 4, 5]
```

---

### Example 2: Flatten Multiple Levels

```javascript
const arr = [1, [2, [3, 4]]];

console.log(arr.flat(2));
```

**Output**

```text
[1, 2, 3, 4]
```

---

### Example 3: Flatten All Levels

```javascript
const arr = [1, [2, [3, [4]]]];

console.log(arr.flat(Infinity));
```

**Output**

```text
[1, 2, 3, 4]
```

---

## 🎤 Interview Answer (30 Seconds)

Flattening an array means converting a nested array into a single-level array. JavaScript provides the `flat()` method, where you can specify the depth to flatten. Using `flat(Infinity)` flattens all nested levels.

---

## 🧠 Memory Trick

```text
Nested Array 📦📦
        │
        ▼
flat()
        │
        ▼
Single Array 📦
```

Easy Rule:

> **flat() = Remove Nesting**

---

## ⭐ Keywords

- flat()
- Flatten
- Nested Array
- Depth
- Infinity
