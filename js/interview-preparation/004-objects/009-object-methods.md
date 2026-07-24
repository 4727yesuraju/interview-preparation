# 📚 What are Object Methods?

## 📖 Simple English Explanation

An **object method** is a **function stored inside an object**.

- **Property** → Stores data.
- **Method** → Performs an action.

Methods allow an object to perform operations using its own data.

---

## 🤔 Why is it Needed?

- Adds behavior to objects.
- Keeps related data and functionality together.
- Represents real-world actions.

---

## 🌊 Flow

```text
Object
   │
   ├── Properties (Data)
   └── Methods (Functions)
            │
            ▼
      Perform Action
```

---

## ✍️ Syntax

### Method Shorthand (Recommended)

```javascript
const person = {
  greet() {
    console.log("Hello");
  },
};
```

### Function Syntax

```javascript
const person = {
  greet: function () {
    console.log("Hello");
  },
};
```

---

## 💻 Example

### Example 1: Simple Method

```javascript
const person = {
  greet() {
    console.log("Hello");
  },
};

person.greet();
```

**Output**

```text
Hello
```

---

### Example 2: Method Using `this`

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

### Example 3: Multiple Methods

```javascript
const calculator = {
  add(a, b) {
    return a + b;
  },

  subtract(a, b) {
    return a - b;
  },
};

console.log(calculator.add(10, 5));
console.log(calculator.subtract(10, 5));
```

**Output**

```text
15
5
```

---

## 🎤 Interview Answer (30 Seconds)

Object methods are functions defined inside an object. They represent the actions an object can perform and can access the object's properties using the `this` keyword. Object methods help group related data and behavior together.

---

## 🧠 Memory Trick

```text
Object
 │
 ├── Data
 └── Action
```

Easy Rule:

> **Property = Data 📄**

> **Method = Action ⚙️**

---

## ⭐ Keywords

- Object Method
- Function
- Property
- `this`
- Method Shorthand
- Object
