# 📚 How to Create Objects using `class` and `Object.create()`

## 📖 Simple English Explanation

Besides object literals (`{}`), JavaScript also allows creating objects using:

1. **Class** → Used to create multiple objects with the same structure (Modern ES6 way).
2. **Object.create()** → Creates a new object using another object as its prototype.

---

## 🌊 Flow

```text
Need Multiple Similar Objects?
          │
          ▼
        Use Class
          │
          ▼
Create Objects

Need Prototype Inheritance?
          │
          ▼
Use Object.create()
          │
          ▼
Create Object from Another Object
```

---

## ✍️ Syntax

### Using Class

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

const person = new Person("John", 25);
```

### Using Object.create()

```javascript
const person = {
  greet() {
    console.log("Hello");
  },
};

const user = Object.create(person);
```

---

## 💻 Example

### Example 1: Using Class

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello ${this.name}`);
  }
}

const person1 = new Person("John", 25);
const person2 = new Person("Alice", 30);

person1.greet();
person2.greet();
```

**Output**

```text
Hello John
Hello Alice
```

---

### Example 2: Using Object.create()

```javascript
const person = {
  greet() {
    console.log("Hello");
  },
};

const user = Object.create(person);

user.greet();
```

**Output**

```text
Hello
```

---

### Example 3: Add Properties

```javascript
const person = {
  greet() {
    console.log(`Hello ${this.name}`);
  },
};

const user = Object.create(person);

user.name = "John";

user.greet();
```

**Output**

```text
Hello John
```

---

## 🎤 Interview Answer (30 Seconds)

A **class** is the modern ES6 way to create multiple objects with the same properties and methods. It acts like a blueprint for creating objects.

`Object.create()` creates a new object using an existing object as its prototype. The new object inherits the properties and methods of the prototype object.

---

## 🧠 Memory Trick

```text
Class 🏭
↓
Blueprint
↓
Create Many Objects

Object.create() 🔗
↓
Inherit from Another Object
```

---

## ⭐ Keywords

- Class
- Constructor
- new
- Object.create()
- Prototype
- Inheritance
