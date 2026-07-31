# 📚 What is the `new` Keyword?

## 📖 Simple English Explanation

The **`new`** keyword is used to **create a new object from a constructor function or class**.

When you use `new`, JavaScript automatically creates a new object, links it to the constructor's prototype, executes the constructor, and returns the new object.

> **Simple Definition:**
>
> **The `new` keyword creates a new object from a constructor function or class.**

---

## 🤔 Why is it Needed?

- Create multiple objects easily.
- Automatically set up inheritance.
- Initialize object properties.
- Avoid manually creating and linking objects.

---

## 🌊 Flow

```text
new Person("John")
        │
        ▼
1. Create a new empty object {}
        │
        ▼
2. Link object to Person.prototype
        │
        ▼
3. Call Person() with this = new object
        │
        ▼
4. Return the new object
```

---

## ✍️ Syntax

### Using a Constructor Function

```javascript
function Person(name) {
  this.name = name;
}

const person = new Person("John");
```

---

### Using a Class

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
}

const person = new Person("John");
```

---

## 💻 Example

### Example 1: Constructor Function

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const person = new Person("John", 25);

console.log(person);
```

**Output**

```text
Person { name: "John", age: 25 }
```

---

### Example 2: Shared Method Using Prototype

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function () {
  console.log(`Hello ${this.name}`);
};

const person = new Person("John");

person.greet();
```

**Output**

```text
Hello John
```

---

### Example 3: Using a Class

```javascript
class Car {
  constructor(brand) {
    this.brand = brand;
  }

  drive() {
    console.log(`${this.brand} is driving`);
  }
}

const car = new Car("Toyota");

car.drive();
```

**Output**

```text
Toyota is driving
```

---

## 📋 What Happens Internally?

When you write:

```javascript
const person = new Person("John");
```

JavaScript does the following:

### Step 1

Creates a new empty object.

```javascript
const obj = {};
```

---

### Step 2

Links the object to `Person.prototype`.

```text
obj.__proto__ → Person.prototype
```

---

### Step 3

Calls the constructor with `this` pointing to the new object.

```javascript
Person.call(obj, "John");
```

Inside the constructor:

```javascript
this.name = "John";
```

becomes

```javascript
obj.name = "John";
```

---

### Step 4

Returns the new object.

```javascript
return obj;
```

---

## 📋 Real-World Uses

| Constructor/Class | Objects Created |
| ----------------- | --------------- |
| `User`            | Many users      |
| `Car`             | Many cars       |
| `Employee`        | Many employees  |
| `Product`         | Many products   |

---

## 🎤 Interview Answer (30 Seconds)

The `new` keyword creates a new object from a constructor function or class. It automatically creates an empty object, links it to the constructor's prototype, calls the constructor with `this` referring to the new object, initializes its properties, and finally returns the new object.

---

## 🧠 Memory Trick

```text
new Person()

      │
      ▼
Create {}

      │
      ▼
Link Prototype

      │
      ▼
Run Constructor

      │
      ▼
Return Object
```

Easy Rule:

> **`new` = Create → Link → Initialize → Return**

---

## ⭐ Keywords

- `new`
- Constructor Function
- Class
- Object Creation
- `this`
- Prototype
- Prototype Chain
- Instance
