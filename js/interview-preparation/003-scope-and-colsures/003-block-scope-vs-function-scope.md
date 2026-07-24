# 📚 Block Scope vs Function Scope

## 📖 Simple English Explanation

- **Block Scope** → A variable declared inside **`{}`** using `let` or `const` can only be accessed **inside that block**.

- **Function Scope** → A variable declared inside a **function** (or using `var`) can only be accessed **inside that function**.

---

## 🤔 Why is it Needed?

- Prevents accidental access to variables.
- Avoids variable conflicts.
- Makes code safer and easier to maintain.

---

## 🌊 Flow

```text
Variable Created
       │
       ▼
Where is it declared?
       │
 ┌─────┴─────┐
 │           │
Inside {}    Inside Function
(let/const)      (var)
 │               │
 ▼               ▼
Block Scope   Function Scope
```

---

## ✍️ Syntax

### Block Scope

```javascript
{
  let name = "John";
}
```

### Function Scope

```javascript
function greet() {
  var message = "Hello";
}
```

---

## 💻 Example

### Example 1: Block Scope

```javascript
if (true) {
  let age = 25;
  console.log(age);
}

// console.log(age); // Error
```

**Output**

```text
25
```

---

### Example 2: Function Scope

```javascript
function greet() {
  var message = "Hello";
  console.log(message);
}

greet();

// console.log(message); // Error
```

**Output**

```text
Hello
```

---

### Example 3: `var` is NOT Block Scoped

```javascript
if (true) {
  var x = 10;
}

console.log(x);
```

**Output**

```text
10
```

**Reason:** `var` ignores the block `{}` and belongs to the surrounding function (or global scope if not inside a function).

---

## 🎤 Interview Answer (30 Seconds)

Block scope means a variable declared with `let` or `const` is accessible only inside the block (`{}`) where it is declared. Function scope means a variable declared with `var` is accessible throughout the entire function where it is declared. The main difference is that `let` and `const` are block-scoped, while `var` is function-scoped.

---

## 🧠 Memory Trick

```text
let / const
      │
      ▼
Inside {}

var
 │
 ▼
Inside Function
```

Easy Rule:

> **`let` & `const` → Block Scope 📦**

> **`var` → Function Scope 🏠**

---

## ⭐ Keywords

- Block Scope
- Function Scope
- `let`
- `const`
- `var`
- Scope
- Variable Visibility
