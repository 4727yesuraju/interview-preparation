# 📚 What are Map and Set?

## 📖 Simple English Explanation

**Map** and **Set** are special data structures introduced in **ES6**.

- **Map** stores data as **key-value pairs**.
- **Set** stores **only unique values** (no duplicates).

> **Simple Definition:**
>
> - **Map** → Collection of key-value pairs.
> - **Set** → Collection of unique values.

---

## 🤔 Why is it Needed?

### Map

- Store key-value pairs.
- Keys can be **any data type** (object, array, function, number, etc.).
- Easier to manage than plain objects in many cases.

### Set

- Store only unique values.
- Automatically remove duplicates.
- Quickly check if a value exists.

---

## 🌊 Flow

### Map

```text
Key
 │
 ▼
Value

"name" ───► "John"
1 ─────────► "Admin"
```

---

### Set

```text
Add Values

1
2
2
3
3
4

      │
      ▼

Set

1
2
3
4
```

Duplicates are automatically ignored.

---

## ✍️ Syntax

### Map

```javascript
const map = new Map();

map.set("name", "John");

console.log(map.get("name"));
```

---

### Set

```javascript
const set = new Set();

set.add(10);

console.log(set.has(10));
```

---

## 💻 Example

### Example 1: Map

```javascript
const user = new Map();

user.set("name", "John");
user.set("age", 25);

console.log(user.get("name"));
console.log(user.get("age"));
```

**Output**

```text
John
25
```

---

### Example 2: Any Type as Key

```javascript
const map = new Map();

const obj = {};

map.set(obj, "Object Key");

console.log(map.get(obj));
```

**Output**

```text
Object Key
```

Unlike plain objects, **Map keys are not limited to strings or symbols**.

---

### Example 3: Set

```javascript
const numbers = new Set();

numbers.add(1);
numbers.add(2);
numbers.add(2);
numbers.add(3);

console.log(numbers);
```

**Output**

```text
Set(3) {1, 2, 3}
```

Duplicate `2` is ignored.

---

### Example 4: Remove Duplicates Using Set

```javascript
const arr = [1, 2, 2, 3, 3, 4];

const unique = [...new Set(arr)];

console.log(unique);
```

**Output**

```text
[1, 2, 3, 4]
```

---

## 📋 Object vs Map

| Feature                | Object                     | Map                                  |
| ---------------------- | -------------------------- | ------------------------------------ |
| Stores key-value pairs | ✅ Yes                     | ✅ Yes                               |
| Key Types              | Strings and Symbols        | Any data type                        |
| Keeps insertion order  | Generally yes (with rules) | ✅ Yes                               |
| Built-in methods       | Few                        | Many (`set`, `get`, `has`, `delete`) |
| `size` property        | ❌ No                      | ✅ Yes                               |

---

## 📋 Array vs Set

| Feature              | Array  | Set                |
| -------------------- | ------ | ------------------ |
| Allows duplicates    | ✅ Yes | ❌ No              |
| Ordered              | ✅ Yes | ✅ Yes             |
| Stores unique values | ❌ No  | ✅ Yes             |
| Common use           | Lists  | Unique collections |

---

## 🌍 Real-World Uses

| Use Case                      | Use |
| ----------------------------- | --- |
| User settings                 | Map |
| Product ID → Product details  | Map |
| Cache                         | Map |
| Remove duplicate array values | Set |
| Unique tags                   | Set |
| Unique user IDs               | Set |

---

## 🎤 Interview Answer (30 Seconds)

Map and Set are ES6 collection types. A Map stores data as key-value pairs and allows keys of any data type, while a Set stores only unique values and automatically removes duplicates. Maps are useful for flexible key-value storage, and Sets are commonly used to maintain collections of unique values.

---

## 🧠 Memory Trick

```text
Map 🗺️

Key ─────► Value

------------------------

Set 📦

1
2
2
3

↓

1
2
3
```

Easy Rule:

> **Map = Key → Value**

> **Set = Unique Values**

---

## ⭐ Keywords

- Map
- Set
- ES6
- Key-Value Pair
- Unique Values
- `set()`
- `get()`
- `add()`
- `has()`
- `delete()`
- `size`
