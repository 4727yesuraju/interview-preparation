# 📚 What is Prototypal Inheritance?

## 📖 Simple English Explanation

**Prototypal Inheritance** is the mechanism by which **one object can inherit (reuse) properties and methods from another object**.

In JavaScript, every object has a hidden link to another object called its **prototype**. If JavaScript cannot find a property or method on the current object, it looks for it in the prototype.

> **Simple Definition:**
>
> **Prototypal Inheritance allows an object to access properties and methods from another object through its prototype.**

---

## 🤔 Why is it Needed?

- Reuse code without copying it.
- Share methods between multiple objects.
- Save memory because shared methods exist only once.
- Forms the foundation of JavaScript's object system.

---

## 🌊 Flow

```text
person Object
│
├── name = "John"
│
└── Prototype
      │
      ▼
animal Object
│
└── speak()

person.speak()
      │
      ▼
Not Found in person
      │
      ▼
Look in Prototype
      │
      ▼
Found ✅
```

---

## ✍️ Syntax

### Using `Object.create()`

```javascript
const parent = {
  greet() {
    console.log("Hello");
  },
};

const child = Object.create(parent);
```

---

## 💻 Example

### Example 1: Basic Prototypal Inheritance

```javascript
const animal = {
  speak() {
    console.log("Animal speaks");
  },
};

const dog = Object.create(animal);

dog.speak();
```

**Output**

```text
Animal speaks
```

> `dog` doesn't have a `speak()` method, so JavaScript looks in its prototype (`animal`).

---

### Example 2: Child Has Its Own Property

```javascript
const animal = {
  type: "Animal",
};

const dog = Object.create(animal);

dog.name = "Buddy";

console.log(dog.name);
console.log(dog.type);
```

**Output**

```text
Buddy
Animal
```

---

### Example 3: Property Lookup

```javascript
const parent = {
  city: "Hyderabad",
};

const child = Object.create(parent);

console.log(child.city);
```

**Output**

```text
Hyderabad
```

JavaScript searches like this:

```text
child.city
    │
    ▼
Found?
    │
   No
    │
    ▼
Prototype
    │
    ▼
Found ✅
```

---

## 📋 Prototype Chain

```text
dog
 │
 ▼
animal
 │
 ▼
Object.prototype
 │
 ▼
null
```

JavaScript keeps searching **up the prototype chain** until it finds the property or reaches `null`.

---

## 📋 Real-World Uses

| Use Case       | Example                              |
| -------------- | ------------------------------------ |
| Shared methods | `Array.prototype.map()`              |
| Custom objects | Reuse common methods                 |
| Classes        | `extends` uses prototypes internally |
| Frameworks     | Object inheritance                   |

---

## 🎤 Interview Answer (30 Seconds)

Prototypal inheritance is JavaScript's inheritance mechanism where one object can inherit properties and methods from another object through its prototype. If a property or method is not found on the object itself, JavaScript searches its prototype chain until it finds it or reaches `null`. This allows code reuse and efficient memory usage.

---

## 🧠 Memory Trick

```text
Child Object
      │
Not Found
      │
      ▼
Prototype
      │
Not Found
      │
      ▼
Object.prototype
      │
      ▼
null
```

Easy Rule:

> **Own Object → Prototype → Object.prototype → null**

---

## ⭐ Keywords

- Prototype
- Prototypal Inheritance
- Prototype Chain
- Object.create()
- Object.prototype
- Code Reuse
- Inheritance
- Property Lookup
