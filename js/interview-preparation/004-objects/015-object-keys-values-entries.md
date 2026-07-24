# 📚 Difference between `Object.keys()`, `Object.values()`, and `Object.entries()`

## 📖 Simple English Explanation

These methods are used to get data from an object.

- **`Object.keys()`** → Returns an array of all **property names (keys)**.
- **`Object.values()`** → Returns an array of all **property values**.
- **`Object.entries()`** → Returns an array of **[key, value] pairs**.

---

## 🤔 Why is it Needed?

- Loop through object data.
- Convert object data into arrays.
- Easily access keys, values, or both.

---

## 🌊 Flow

```text
Object
  │
  ▼
 ┌─────────────┬──────────────┬────────────────┐
 │             │              │
 ▼             ▼              ▼
keys()      values()      entries()
 │             │              │
["name"]   ["John"]   [["name","John"]]
```

---

## ✍️ Syntax

### Object.keys()

```javascript
Object.keys(object);
```

### Object.values()

```javascript
Object.values(object);
```

### Object.entries()

```javascript
Object.entries(object);
```

---

## 💻 Example

### Example 1: `Object.keys()`

```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(Object.keys(person));
```

**Output**

```text
["name", "age"]
```

---

### Example 2: `Object.values()`

```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(Object.values(person));
```

**Output**

```text
["John", 25]
```

---

### Example 3: `Object.entries()`

```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(Object.entries(person));
```

**Output**

```text
[
  ["name", "John"],
  ["age", 25]
]
```

---

## 🎤 Interview Answer (30 Seconds)

`Object.keys()`, `Object.values()`, and `Object.entries()` are used to retrieve data from an object. `Object.keys()` returns property names, `Object.values()` returns property values, and `Object.entries()` returns key-value pairs as nested arrays.

---

## 🧠 Memory Trick

```text
keys()    🔑
values()  📦
entries() 🔑📦
```

Easy Rule:

> **Keys = Names**

> **Values = Data**

> **Entries = Name + Data**

---

## ⭐ Keywords

- Object.keys()
- Object.values()
- Object.entries()
- Keys
- Values
- Key-Value Pairs
