# 📚 What are Symbols?

## 📖 Simple English Explanation

A **Symbol** is a **unique and immutable (cannot be changed)** primitive data type introduced in **ES6**.

Every Symbol is **unique**, even if two Symbols have the same description.

Symbols are mainly used as **object property keys** to avoid property name conflicts.

> **Simple Definition:**
>
> **A Symbol is a unique value that is commonly used as a unique key for object properties.**

---

## 🤔 Why is it Needed?

- Prevent property name conflicts.
- Create unique object keys.
- Hide object properties from normal iteration.
- Used internally by JavaScript features like iterators (`Symbol.iterator`).

---

## 🌊 Flow

```text
Create Symbol
      │
      ▼
Unique Value
      │
      ▼
Use as Object Key
      │
      ▼
No Name Conflicts
```

---

## ✍️ Syntax

### Create a Symbol

```javascript
const id = Symbol("id");
```

### Use Symbol as an Object Key

```javascript
const user = {
  [id]: 101,
};
```

---

## 💻 Example

### Example 1: Creating a Symbol

```javascript
const id = Symbol("id");

console.log(id);
```

**Output**

```text
Symbol(id)
```

---

### Example 2: Every Symbol is Unique

```javascript
const id1 = Symbol("id");
const id2 = Symbol("id");

console.log(id1 === id2);
```

**Output**

```text
false
```

> Even though both have the same description (`"id"`), they are different Symbols.

---

### Example 3: Using a Symbol as an Object Key

```javascript
const id = Symbol("id");

const user = {
  name: "John",
  [id]: 101,
};

console.log(user.name);
console.log(user[id]);
```

**Output**

```text
John
101
```

---

### Example 4: Symbol Properties Are Not Returned by `Object.keys()`

```javascript
const id = Symbol("id");

const user = {
  name: "John",
  [id]: 101,
};

console.log(Object.keys(user));
```

**Output**

```text
["name"]
```

The Symbol property is **not included**.

To get Symbol keys:

```javascript
console.log(Object.getOwnPropertySymbols(user));
```

**Output**

```text
[Symbol(id)]
```

---

## 📋 Real-World Uses

| Use Case                   | Why Use Symbol?             |
| -------------------------- | --------------------------- |
| Unique object IDs          | Avoid key conflicts         |
| Library development        | Prevent property collisions |
| Internal object properties | Hide from normal iteration  |
| `Symbol.iterator`          | Make objects iterable       |

---

## 🎤 Interview Answer (30 Seconds)

A Symbol is a unique primitive data type introduced in ES6. Every Symbol is unique, even if it has the same description. Symbols are mainly used as object property keys to avoid naming conflicts and to create properties that are hidden from normal property enumeration methods like `Object.keys()`.

---

## 🧠 Memory Trick

```text
Symbol("id")
      │
      ▼
Unique Key 🔑
      │
      ▼
Object
      │
      ▼
No Name Conflicts
```

Easy Rule:

> **Symbol = Unique Key**

---

## ⭐ Keywords

- Symbol
- Primitive Data Type
- ES6
- Unique Value
- Object Key
- Symbol.iterator
- Object.getOwnPropertySymbols()
- Property Collision
