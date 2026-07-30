# 📚 `__proto__` vs `prototype`

## 📖 Simple English Explanation

`__proto__` and `prototype` are **different**, but many beginners confuse them.

- **`__proto__`** → Exists on an **object**. It points to the object's prototype.
- **`prototype`** → Exists on a **constructor function or class**. It is used to define methods that all objects created from it will share.

> **Simple Definition:**
>
> - **`__proto__` = Object's link to its prototype.**
> - **`prototype` = Blueprint used when creating objects.**

---

## 🤔 Why is it Needed?

### `prototype`

- Share methods between all objects.
- Save memory.
- Used for inheritance.

### `__proto__`

- Connect an object to its prototype.
- Used by JavaScript during property lookup.

---

## 🌊 Flow

```text
function Person()

        │
        ▼
Person.prototype
        │
        ▼
new Person()
        │
        ▼
person Object
        │
        ▼
person.__proto__
        │
        ▼
Person.prototype
```

**Important**

```text
person.__proto__ === Person.prototype

✅ true
```

---

## ✍️ Syntax

### Using `prototype`

```javascript
function Person() {}

Person.prototype.sayHello = function () {
  console.log("Hello");
};
```

---

### Using `__proto__`

```javascript
const person = new Person();

console.log(person.__proto__);
```

---

## 💻 Example

### Example 1: `prototype`

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function () {
  console.log(`Hello ${this.name}`);
};

const p1 = new Person("John");
const p2 = new Person("Alice");

p1.greet();
p2.greet();
```

**Output**

```text
Hello John
Hello Alice
```

Both objects share **one** `greet()` method.

---

### Example 2: `__proto__`

```javascript
function Person() {}

Person.prototype.city = "Hyderabad";

const person = new Person();

console.log(person.city);
```

**Output**

```text
Hyderabad
```

JavaScript searches like this:

```text
person
 │
 ▼
city ❌
 │
 ▼
person.__proto__
 │
 ▼
Person.prototype
 │
 ▼
city ✅
```

---

### Example 3: Relationship

```javascript
function Person() {}

const person = new Person();

console.log(person.__proto__ === Person.prototype);
```

**Output**

```text
true
```

---

## 📋 Comparison

| Feature                     | `__proto__`                      | `prototype`                          |
| --------------------------- | -------------------------------- | ------------------------------------ |
| Belongs to                  | Object                           | Constructor function / Class         |
| Purpose                     | Points to the object's prototype | Stores shared properties and methods |
| Used during property lookup | ✅ Yes                           | Indirectly (via `__proto__`)         |
| Exists on normal objects    | ✅ Yes                           | ❌ No                                |

---

## 📋 Real-World Example

```javascript
function Car() {}

Car.prototype.start = function () {
  console.log("Car Started");
};

const car = new Car();

car.start();
```

Flow:

```text
car.start()

car
 │
 ▼
Not Found
 │
 ▼
car.__proto__
 │
 ▼
Car.prototype
 │
 ▼
start() ✅
```

---

## 🎤 Interview Answer (30 Seconds)

`prototype` is a property of constructor functions and classes that stores methods and properties shared by all instances. `__proto__` is a property of an object that points to its prototype. When a property is not found on an object, JavaScript follows the `__proto__` link to search the prototype chain. In objects created with `new`, `object.__proto__` is equal to `Constructor.prototype`.

---

## 🧠 Memory Trick

```text
Constructor
      │
prototype
      │
      ▼
Shared Methods

----------------------

Object
      │
__proto__
      │
      ▼
Points to Prototype
```

Easy Rule:

> **`prototype` belongs to the constructor.**

> **`__proto__` belongs to the object.**

---

## ⭐ Keywords

- `prototype`
- `__proto__`
- Constructor
- Object
- Prototype Chain
- Inheritance
- Shared Methods
- Property Lookup
