# 📚 `includes()` vs `indexOf()`

## 📖 Simple English Explanation

Both `includes()` and `indexOf()` are used to **check whether an element exists in an array**.

- **`includes()`** → Returns `true` or `false`.
- **`indexOf()`** → Returns the **index** of the element. If not found, it returns `-1`.

---

## 🤔 Why is it Needed?

- **`includes()`** → Check if an element exists.
- **`indexOf()`** → Find the position (index) of an element.

---

## 🌊 Flow

```text
Need to Search an Element?
          │
          ▼
   ┌───────────────┐
   ▼               ▼
includes()     indexOf()
   │               │
Exists?         Position?
   │               │
true/false     Index or -1
```

---

## ✍️ Syntax

### `includes()`

```javascript
array.includes(element);
```

### `indexOf()`

```javascript
array.indexOf(element);
```

---

## 💻 Example

### Example 1: `includes()`

```javascript
const fruits = ["Apple", "Mango", "Orange"];

console.log(fruits.includes("Mango"));
console.log(fruits.includes("Banana"));
```

**Output**

```text
true
false
```

---

### Example 2: `indexOf()`

```javascript
const fruits = ["Apple", "Mango", "Orange"];

console.log(fruits.indexOf("Mango"));
console.log(fruits.indexOf("Banana"));
```

**Output**

```text
1
-1
```

---

### Example 3: Check Before Adding

```javascript
const fruits = ["Apple", "Mango"];

if (!fruits.includes("Orange")) {
  fruits.push("Orange");
}

console.log(fruits);
```

**Output**

```text
["Apple", "Mango", "Orange"]
```

---

## 🎤 Interview Answer (30 Seconds)

`includes()` and `indexOf()` are both used to search an array. `includes()` returns a boolean (`true` or `false`) indicating whether an element exists, while `indexOf()` returns the index of the element or `-1` if it is not found.

---

## 🧠 Memory Trick

```text
includes()
↓
Exists? ✅❌

indexOf()
↓
Where? 📍
```

Easy Rule:

> **includes = Exists?**

> **indexOf = Position?**

---

## ⭐ Keywords

- includes()
- indexOf()
- Search
- Boolean
- Index
- Array
