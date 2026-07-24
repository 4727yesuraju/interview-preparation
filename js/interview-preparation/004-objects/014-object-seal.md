# 📚 What is `Object.seal()`?

## 📖 Simple English Explanation

`Object.seal()` is used to **seal an object**.

After sealing an object, you:

- ✅ Can update existing properties.
- ❌ Cannot add new properties.
- ❌ Cannot delete existing properties.

---

## 🤔 Why is it Needed?

- Prevents the object structure from changing.
- Allows updating existing values.
- Protects objects from accidental additions or deletions.

---

## 🌊 Flow

```text
Create Object
      │
      ▼
Object.seal()
      │
      ▼
Object Sealed
      │
      ├── Add Property ❌
      ├── Delete Property ❌
      └── Update Property ✅
```

---

## ✍️ Syntax

```javascript
Object.seal(object);
```

---

## 💻 Example

### Example 1: Update Property ✅

```javascript
const person = {
  name: "John",
};

Object.seal(person);

person.name = "Alice";

console.log(person);
```

**Output**

```text
{ name: "Alice" }
```

---

### Example 2: Add Property ❌

```javascript
const person = {
  name: "John",
};

Object.seal(person);

person.age = 25;

console.log(person);
```

**Output**

```text
{ name: "John" }
```

---

### Example 3: Delete Property ❌

```javascript
const person = {
  name: "John",
};

Object.seal(person);

delete person.name;

console.log(person);
```

**Output**

```text
{ name: "John" }
```

---

## 🎤 Interview Answer (30 Seconds)

`Object.seal()` prevents adding and deleting properties from an object, but it still allows updating existing property values. It is useful when you want to keep the object's structure fixed while allowing its data to change.

---

## 🧠 Memory Trick

```text
Seal 📦
   │
   ▼
Structure Locked 🔒
Values Can Change ✏️
```

Easy Rule:

> **Seal = Update Only**

---

## ⭐ Keywords

- Object.seal()
- Sealed Object
- Update Allowed
- Add Not Allowed
- Delete Not Allowed
