# 📚 Dot Notation vs Bracket Notation

## 📖 Simple English Explanation

Both **dot notation (`.`)** and **bracket notation (`[]`)** are used to **access or modify object properties**.

- **Dot Notation (`.`)** → Use when you know the property name.
- **Bracket Notation (`[]`)** → Use when the property name is stored in a variable or contains special characters/spaces.

---

## 🤔 Why is it Needed?

- To read object properties.
- To update object properties.
- To access dynamic property names.

---

## 🌊 Flow

```text
Need Property?
      │
      ▼
Know Property Name?
      │
 ┌────┴────┐
 │         │
 Yes       No / Dynamic
 │         │
 ▼         ▼
Dot       Bracket
Notation  Notation
```

---

## ✍️ Syntax

### Dot Notation

```javascript
object.property;
```

### Bracket Notation

```javascript
object["property"];
object[propertyName];
```

---

## 💻 Example

### Example 1: Dot Notation

```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(person.name);
```

**Output**

```text
John
```

---

### Example 2: Bracket Notation

```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(person["name"]);
```

**Output**

```text
John
```

---

### Example 3: Dynamic Property

```javascript
const person = {
  name: "John",
};

const key = "name";

console.log(person[key]);
```

**Output**

```text
John
```

---

### Example 4: Property with Space

```javascript
const person = {
  "full name": "John Doe",
};

console.log(person["full name"]);
```

**Output**

```text
John Doe
```

---

## 🎤 Interview Answer (30 Seconds)

Dot notation and bracket notation are both used to access object properties. Dot notation is simpler and is used when the property name is known. Bracket notation is used when the property name is dynamic, stored in a variable, or contains spaces or special characters.

---

## 🧠 Memory Trick

```text
Know Property?
      │
      ▼
Yes → .

No / Dynamic → []
```

Easy Rule:

> **Known Name = `.`**

> **Dynamic Name = `[]`**

---

## ⭐ Keywords

- Dot Notation
- Bracket Notation
- Object Property
- Dynamic Property
- Variable
