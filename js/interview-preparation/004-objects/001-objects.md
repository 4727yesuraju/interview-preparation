# 📚 What is an Object?

## 📖 Simple English Explanation

An **Object** is a collection of **key-value pairs** used to store related data and functions.

- **Key** → Property name
- **Value** → Property value or function (method)

Objects help represent **real-world entities** like a user, product, or car.

---

## 🤔 Why is it Needed?

- Groups related data together.
- Makes data easy to organize and access.
- Represents real-world objects.
- Stores both data and functions.

---

## 🌊 Flow

```text
Object
   │
   ├── Key : Value
   ├── Key : Value
   └── Method()
```

---

## ✍️ Syntax

```javascript
const person = {
  name: "John",
  age: 25,
  greet() {
    console.log("Hello");
  },
};
```

---

## 💻 Example

### Example 1: Simple Object

```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(person.name);
console.log(person.age);
```

**Output**

```text
John
25
```

---

### Example 2: Object with Method

```javascript
const person = {
  name: "John",

  greet() {
    console.log(`Hello ${this.name}`);
  },
};

person.greet();
```

**Output**

```text
Hello John
```

---

### Example 3: Add a New Property

```javascript
const person = {
  name: "John",
};

person.age = 25;

console.log(person);
```

**Output**

```text
{ name: "John", age: 25 }
```

---

## 🎤 Interview Answer (30 Seconds)

An object is a collection of **key-value pairs** used to store related data and methods. It helps represent real-world entities such as users, products, and cars. We can access object properties using dot notation (`.`) or bracket notation (`[]`).

---

## 🧠 Memory Trick

```text
Object
   │
   ├── name : "John"
   ├── age : 25
   └── greet()
```

Easy Rule:

> **Object = Collection of Key-Value Pairs**

---

## ⭐ Keywords

- Object
- Key-Value Pair
- Property
- Method
- Dot Notation
- Bracket Notation
- `this`
