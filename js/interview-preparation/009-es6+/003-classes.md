# 📚 What are Classes?

## 📖 Simple English Explanation

A **Class** is a blueprint (template) for creating objects.

Instead of creating many similar objects manually, you create a class once and then create multiple objects from it.

A class can contain:

- Properties (data)
- Methods (functions)

> **Simple Definition:**
>
> **A Class is a blueprint used to create objects with the same properties and methods.**

---

## 🤔 Why is it Needed?

- Avoid writing duplicate code.
- Create multiple similar objects easily.
- Organize code in an object-oriented way.
- Improve code readability and reusability.

---

## 🌊 Flow

```text
Class (Blueprint)
        │
        ▼
Create Object (new)
        │
        ▼
Object 1
Object 2
Object 3
```

---

## ✍️ Syntax

```javascript
class ClassName {
  constructor(property) {
    this.property = property;
  }

  method() {
    // code
  }
}

const object = new ClassName(value);
```

---

## 💻 Example

### Example 1: Simple Class

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
}

const person1 = new Person("John", 25);

person1.greet();
```

**Output**

```text
Hi, I'm John
```

---

### Example 2: Multiple Objects

```javascript
class Car {
  constructor(brand) {
    this.brand = brand;
  }

  drive() {
    console.log(`${this.brand} is driving`);
  }
}

const car1 = new Car("Toyota");
const car2 = new Car("Honda");

car1.drive();
car2.drive();
```

**Output**

```text
Toyota is driving
Honda is driving
```

---

### Example 3: Class with Method

```javascript
class Calculator {
  add(a, b) {
    return a + b;
  }
}

const calc = new Calculator();

console.log(calc.add(5, 3));
```

**Output**

```text
8
```

---

## 📋 Real-World Uses

| Class      | Objects Created       |
| ---------- | --------------------- |
| `User`     | John, Alice, Bob      |
| `Car`      | Toyota, Honda, BMW    |
| `Product`  | Laptop, Phone, Tablet |
| `Employee` | Manager, Developer    |

---

## 🎤 Interview Answer (30 Seconds)

A class is a blueprint used to create objects in JavaScript. It defines the properties and methods that every object created from that class will have. Objects are created using the `new` keyword. Classes make code reusable, organized, and easier to maintain.

---

## 🧠 Memory Trick

```text
Blueprint 🏠
     │
     ▼
Class
     │
 new
     ▼
Objects
```

Easy Rule:

> **Class = Blueprint**

> **Object = Real Thing Created from the Blueprint**

---

## ⭐ Keywords

- Class
- Object
- Blueprint
- constructor
- this
- new
- Method
- Object-Oriented Programming (OOP)
