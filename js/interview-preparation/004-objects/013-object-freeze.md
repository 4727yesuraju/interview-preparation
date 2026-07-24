# 📚 What is `Object.freeze()`?

## 📖 Simple English Explanation

`Object.freeze()` is used to make an object **immutable** (read-only).

After freezing an object, you **cannot**:

- Add new properties ❌
- Update existing properties ❌
- Delete properties ❌

---

## 🤔 Why is it Needed?

- Prevents accidental changes.
- Protects important configuration or constant objects.
- Makes code safer and more predictable.

---

## 🌊 Flow

```text
Create Object
      │
      ▼
Object.freeze()
      │
      ▼
Object Becomes Read-Only
      │
      ▼
No Add ❌
No Update ❌
No Delete ❌
```

---

## ✍️ Syntax

```javascript
Object.freeze(object);
```

---

## 💻 Example

### Example 1: Update Property

```javascript
const person = {
  name: "John",
};

Object.freeze(person);

person.name = "Alice";

console.log(person.name);
```

**Output**

```text
John
```

---

### Example 2: Add Property

```javascript
const person = {
  name: "John",
};

Object.freeze(person);

person.age = 25;

console.log(person);
```

**Output**

```text
{ name: "John" }
```

---

### Example 3: Delete Property

```javascript
const person = {
  name: "John",
};

Object.freeze(person);

delete person.name;

console.log(person);
```

**Output**

```text
{ name: "John" }
```

---

## 🎤 Interview Answer (30 Seconds)

`Object.freeze()` makes an object immutable. After freezing, you cannot add, modify, or delete its properties. It is commonly used to protect configuration objects and prevent accidental changes.

---

## 🧠 Memory Trick

```text
Freeze 🧊
      │
      ▼
Locked Object 🔒
```

Easy Rule:

> **Freeze = Read-Only Object**

---

## ⭐ Keywords

- Object.freeze()
- Immutable
- Read-Only
- Prevent Modification
- Object
