# 📚 What are Getters and Setters?

## 📖 Simple English Explanation

**Getters** and **Setters** are special methods in JavaScript classes used to **get** and **set** property values.

- **Getter (`get`)** → Reads (returns) a property's value.
- **Setter (`set`)** → Updates (changes) a property's value.

They let you **control how properties are accessed and modified**.

> **Simple Definition:**
>
> **Getters read a property's value, and Setters update a property's value.**

---

## 🤔 Why is it Needed?

- Control access to object properties.
- Validate data before updating it.
- Hide internal implementation details.
- Keep object data safe and consistent.

---

## 🌊 Flow

```text
Object
   │
   ├── Read Property
   │       │
   │       ▼
   │    Getter (get)
   │
   └── Update Property
           │
           ▼
       Setter (set)
```

---

## ✍️ Syntax

```javascript
class Person {
  constructor(name) {
    this._name = name;
  }

  get name() {
    return this._name;
  }

  set name(value) {
    this._name = value;
  }
}
```

> By convention, `_name` is used as the internal property, while `name` is accessed through the getter and setter.

---

## 💻 Example

### Example 1: Getter

```javascript
class Person {
  constructor(name) {
    this._name = name;
  }

  get name() {
    return this._name;
  }
}

const person = new Person("John");

console.log(person.name);
```

**Output**

```text
John
```

---

### Example 2: Setter

```javascript
class Person {
  constructor(name) {
    this._name = name;
  }

  set name(value) {
    this._name = value;
  }

  get name() {
    return this._name;
  }
}

const person = new Person("John");

person.name = "Alice";

console.log(person.name);
```

**Output**

```text
Alice
```

---

### Example 3: Validation Using Setter

```javascript
class Person {
  constructor(age) {
    this._age = age;
  }

  get age() {
    return this._age;
  }

  set age(value) {
    if (value < 0) {
      console.log("Age cannot be negative");
      return;
    }

    this._age = value;
  }
}

const person = new Person(20);

person.age = -5;

console.log(person.age);
```

**Output**

```text
Age cannot be negative
20
```

---

## 📋 Comparison

| Getter             | Setter                      |
| ------------------ | --------------------------- |
| Reads a value      | Updates a value             |
| Uses `get` keyword | Uses `set` keyword          |
| Returns data       | Receives one value as input |
| No parameters      | One parameter               |

---

## 🎤 Interview Answer (30 Seconds)

Getters and setters are special methods in JavaScript classes used to control access to object properties. A getter returns a property's value, while a setter updates it. They are useful for validation, encapsulation, and controlling how data is accessed or modified.

---

## 🧠 Memory Trick

```text
Getter
   │
   ▼
GET 📥
Read Value

Setter
   │
   ▼
SET 📤
Update Value
```

Easy Rule:

> **Getter = Read**

> **Setter = Update**

---

## ⭐ Keywords

- Getter
- Setter
- get
- set
- Class
- Object
- Property
- Validation
- Encapsulation
