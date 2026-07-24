# 📚 What is the `this` Keyword?

## 📖 Simple English Explanation

The **`this`** keyword refers to the **object that is currently executing the function**.

The value of `this` **depends on how the function is called**, not where it is written.

---

## 🤔 Why is it Needed?

- Access the current object's properties.
- Reuse the same function for different objects.
- Used in objects, classes, constructors, and event handlers.

---

## 🌊 Flow

```text
Function Called
      │
      ▼
Who Called It?
      │
      ▼
That Object
Becomes `this`
```

---

## ✍️ Syntax

```javascript
const person = {
  name: "John",

  greet() {
    console.log(this.name);
  },
};
```

---

## 💻 Example

### Example 1: `this` in an Object

```javascript
const person = {
  name: "John",

  greet() {
    console.log(this.name);
  },
};

person.greet();
```

**Output**

```text
John
```

---

### Example 2: `this` in Different Objects

```javascript
const person1 = {
  name: "John",
  greet() {
    console.log(this.name);
  },
};

const person2 = {
  name: "Alice",
  greet() {
    console.log(this.name);
  },
};

person1.greet();
person2.greet();
```

**Output**

```text
John
Alice
```

---

### Example 3: `this` in a Class

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(this.name);
  }
}

const person = new Person("John");

person.greet();
```

**Output**

```text
John
```

---

## 🎤 Interview Answer (30 Seconds)

The `this` keyword refers to the object that is currently executing the function. Its value is determined by **how the function is called**, not where it is defined. It is commonly used to access an object's own properties and methods.

---

## 🧠 Memory Trick

```text
Who Called the Function?
         │
         ▼
That is `this`
```

Easy Rule:

> **`this` = Current Caller**

---

## ⭐ Keywords

- `this`
- Current Object
- Function Call
- Object Method
- Class
- Context
