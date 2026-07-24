# 📚 Shallow Copy vs Deep Copy

## 📖 Simple English Explanation

When copying an object, there are **two types of copies**:

- **Shallow Copy** → Copies only the **first level**. Nested objects are **shared** between the original and the copy.
- **Deep Copy** → Copies **all levels**, including nested objects. The original and copy are completely independent.

---

## 🤔 Why is it Needed?

- Prevents accidental changes to the original object.
- Important when working with nested objects.
- Commonly used in React state management and API data.

---

## 🌊 Flow

```text
Original Object
       │
       ▼
Copy Object
       │
 ┌─────┴─────┐
 │           │
 ▼           ▼
Shallow    Deep
Copy       Copy
 │           │
Shares      Independent
Nested      Nested
Objects     Objects
```

---

## ✍️ Syntax

### Shallow Copy

```javascript
const copy = { ...original };
```

### Deep Copy

```javascript
const copy = structuredClone(original);
```

---

## 💻 Example

### Example 1: Shallow Copy

```javascript
const user1 = {
  name: "John",
  address: {
    city: "Hyderabad",
  },
};

const user2 = { ...user1 };

user2.address.city = "Chennai";

console.log(user1.address.city);
```

**Output**

```text
Chennai
```

**Reason:** `address` is a nested object, so both objects share the same reference.

---

### Example 2: Deep Copy

```javascript
const user1 = {
  name: "John",
  address: {
    city: "Hyderabad",
  },
};

const user2 = structuredClone(user1);

user2.address.city = "Chennai";

console.log(user1.address.city);
console.log(user2.address.city);
```

**Output**

```text
Hyderabad
Chennai
```

---

### Example 3: Primitive Property

```javascript
const user1 = {
  name: "John",
};

const user2 = { ...user1 };

user2.name = "Alice";

console.log(user1.name);
console.log(user2.name);
```

**Output**

```text
John
Alice
```

**Reason:** Primitive values are copied by value.

---

## 🎤 Interview Answer (30 Seconds)

A **shallow copy** copies only the first level of an object. Nested objects are still shared by reference, so changes to nested data affect both objects. A **deep copy** copies every level, making the original and copied objects completely independent.

---

## 🧠 Memory Trick

```text
Shallow Copy 🌊
↓
First Level Only

Deep Copy 🌊🌊
↓
Everything
```

Easy Rule:

> **Shallow = Shared Nested Objects**

> **Deep = Independent Objects**

---

## ⭐ Keywords

- Shallow Copy
- Deep Copy
- Spread Operator
- structuredClone()
- Reference
- Nested Object
