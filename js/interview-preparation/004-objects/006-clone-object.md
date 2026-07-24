# 📚 How do you Clone an Object?

## 📖 Simple English Explanation

**Cloning an object** means creating a **new object with the same properties** as the original object.

This is useful because assigning one object to another variable **does not create a copy**. Instead, both variables point to the **same object** in memory.

---

## 🤔 Why is it Needed?

- Prevents accidental changes to the original object.
- Creates an independent copy.
- Commonly used in React state updates and API data handling.

---

## 🌊 Flow

```text
Original Object
       │
       ▼
Clone Object
       │
       ▼
Two Separate Objects
```

---

## ✍️ Syntax

### Spread Operator (Recommended)

```javascript
const clone = { ...original };
```

### Object.assign()

```javascript
const clone = Object.assign({}, original);
```

---

## 💻 Example

### Example 1: Assignment (Not a Clone) ❌

```javascript
const person1 = {
  name: "John",
};

const person2 = person1;

person2.name = "Alice";

console.log(person1.name);
```

**Output**

```text
Alice
```

**Reason:** Both variables refer to the **same object**.

---

### Example 2: Spread Operator ✅

```javascript
const person1 = {
  name: "John",
};

const person2 = { ...person1 };

person2.name = "Alice";

console.log(person1.name);
console.log(person2.name);
```

**Output**

```text
John
Alice
```

---

### Example 3: Object.assign() ✅

```javascript
const person1 = {
  name: "John",
};

const person2 = Object.assign({}, person1);

person2.name = "Alice";

console.log(person1.name);
console.log(person2.name);
```

**Output**

```text
John
Alice
```

---

## 🎤 Interview Answer (30 Seconds)

An object can be cloned using the **spread operator (`...`)** or **`Object.assign()`**. These create a **shallow copy** of the object. Simply assigning one object to another variable does not clone it—it only copies the reference.

---

## 🧠 Memory Trick

```text
=
│
Reference ❌

...
│
Clone ✅
```

Easy Rule:

> **`=` = Same Object**

> **`...` = New Object**

---

## ⭐ Keywords

- Clone
- Shallow Copy
- Spread Operator
- `Object.assign()`
- Reference
- Object Copy
