# 📚 Difference between `call()`, `apply()`, and `bind()`

## 📖 Simple English Explanation

`call()`, `apply()`, and `bind()` are methods used to **change the value of `this`** inside a function.

The main difference is **how they pass arguments and when they execute the function**.

- **call()** → Calls the function immediately and passes arguments one by one.
- **apply()** → Calls the function immediately and passes arguments as an array.
- **bind()** → Does **not** call the function immediately. It returns a **new function** with `this` permanently bound.

---

## 🤔 Why is it Needed?

- Change the value of `this`.
- Reuse the same function for different objects.
- Useful in event handlers, callbacks, and function borrowing.

---

## 🌊 Flow

```text
Need to Change `this`
        │
        ▼
 ┌──────┼────────┐
 │      │        │
 ▼      ▼        ▼
call() apply() bind()
 │      │        │
Runs   Runs   Returns
Now    Now    New Function
```

---

## ✍️ Syntax

### call()

```javascript
function.call(thisArg, arg1, arg2);
```

### apply()

```javascript
function.apply(thisArg, [arg1, arg2]);
```

### bind()

```javascript
const newFunction = function.bind(thisArg);
```

---

## 💻 Example

### Example 1: `call()`

```javascript
const person = {
  name: "John",
};

function greet(city) {
  console.log(`${this.name} from ${city}`);
}

greet.call(person, "Hyderabad");
```

**Output**

```text
John from Hyderabad
```

---

### Example 2: `apply()`

```javascript
const person = {
  name: "John",
};

function greet(city) {
  console.log(`${this.name} from ${city}`);
}

greet.apply(person, ["Hyderabad"]);
```

**Output**

```text
John from Hyderabad
```

---

### Example 3: `bind()`

```javascript
const person = {
  name: "John",
};

function greet(city) {
  console.log(`${this.name} from ${city}`);
}

const greetJohn = greet.bind(person);

greetJohn("Hyderabad");
```

**Output**

```text
John from Hyderabad
```

---

## 🎤 Interview Answer (30 Seconds)

`call()`, `apply()`, and `bind()` are used to control the value of `this`.

- `call()` executes the function immediately and accepts arguments individually.
- `apply()` executes the function immediately but accepts arguments as an array.
- `bind()` does not execute the function immediately. It returns a new function with `this` permanently bound.

---

## 🧠 Memory Trick

```text
call()
↓
Call Now 📞

apply()
↓
Array 📦

bind()
↓
Bind & Use Later 🔗
```

Easy Rule:

> **call = Call Now**

> **apply = Array**

> **bind = Bind for Later**

---

## ⭐ Keywords

- call()
- apply()
- bind()
- this
- Function Borrowing
- Context
