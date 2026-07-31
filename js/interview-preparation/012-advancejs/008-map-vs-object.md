# 📚 Map vs Object

## 📖 Simple English Explanation

Both **Map** and **Object** are used to store data as **key-value pairs**.

The main difference is:

- **Object** keys can only be **strings or symbols**.
- **Map** keys can be **any data type** (string, number, object, array, function, etc.).

> **Simple Definition:**
>
> - **Object** → Traditional JavaScript key-value storage.
> - **Map** → ES6 collection for storing key-value pairs with keys of any type.

---

## 🤔 Why is it Needed?

### Object

- Best for representing real-world entities.
- Commonly used for JSON data.
- Simple and lightweight.

### Map

- Allows any type of key.
- Provides built-in methods like `set()`, `get()`, `has()`, and `delete()`.
- Better for frequent additions, deletions, and lookups.

---

## 🌊 Flow

### Object

```text
user
 │
 ├── name → "John"
 └── age  → 25
```

---

### Map

```text
"name" ───► "John"
1 ─────────► "Admin"
{} ────────► "Object Key"
```

---

## ✍️ Syntax

### Object

```javascript
const user = {
  name: "John",
};

console.log(user.name);
```

---

### Map

```javascript
const user = new Map();

user.set("name", "John");

console.log(user.get("name"));
```

---

## 💻 Example

### Example 1: Object

```javascript
const user = {
  name: "John",
  age: 25,
};

console.log(user.name);
console.log(user.age);
```

**Output**

```text
John
25
```

---

### Example 2: Map

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

### Example 3: Object Keys

```javascript
const obj = {};

obj[1] = "One";

console.log(obj);
```

**Output**

```text
{ "1": "One" }
```

The number key becomes a string.

---

### Example 4: Map Keys

```javascript
const map = new Map();

map.set(1, "One");

console.log(map.get(1));
```

**Output**

```text
One
```

The key remains a number.

---

### Example 5: Object as Key

```javascript
const key = {};

const map = new Map();

map.set(key, "Hello");

console.log(map.get(key));
```

**Output**

```text
Hello
```

Objects can be keys in a Map.

---

## 📋 Map vs Object

| Feature                      | Object           | Map               |
| ---------------------------- | ---------------- | ----------------- |
| Key-Value Storage            | ✅ Yes           | ✅ Yes            |
| Key Types                    | String or Symbol | Any data type     |
| Built-in Methods             | Few              | Many              |
| Size Property                | ❌ No            | ✅ `size`         |
| Iterable                     | ❌ Not directly  | ✅ Yes            |
| Maintains Insertion Order    | Mostly           | ✅ Yes            |
| Best for Frequent Add/Delete | ❌               | ✅                |
| JSON Support                 | ✅ Native        | ❌ Convert needed |

---

## 🌍 Real-World Uses

| Use Case                  | Better Choice |
| ------------------------- | ------------- |
| API Response Data         | Object        |
| JSON Data                 | Object        |
| User Profile              | Object        |
| Cache                     | Map           |
| Dynamic Key-Value Storage | Map           |
| Object Keys               | Map           |

---

## 🎤 Interview Answer (30 Seconds)

Both Map and Object store data as key-value pairs. Objects are traditional JavaScript structures where keys are strings or symbols and are commonly used for JSON and representing entities. Maps were introduced in ES6 and allow keys of any data type, provide built-in methods, maintain insertion order, and are better for frequent additions, deletions, and lookups.

---

## 🧠 Memory Trick

```text
Object
│
├── JSON
├── User Data
└── String Keys

----------------------

Map
│
├── Any Key Type
├── Dynamic Data
└── Better Collections
```

Easy Rule:

> **Object = Data Structure**

> **Map = Collection Structure**

---

## ⭐ Keywords

- Object
- Map
- ES6
- Key-Value Pair
- `set()`
- `get()`
- `size`
- Iterable
- JSON
- Dynamic Keys
