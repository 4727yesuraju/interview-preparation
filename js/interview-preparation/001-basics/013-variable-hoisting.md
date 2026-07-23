# 📚 What is Variable Hoisting?

## 📖 Simple English Explanation

**Hoisting** is JavaScript's behavior of **moving variable and function declarations to the top of their scope before executing the code**.

However, **only the declaration is hoisted, not the initialization (value assignment).**

- `var` → Hoisted and initialized with `undefined`.
- `let` & `const` → Hoisted, but **cannot be accessed before declaration** (Temporal Dead Zone).

---

## 🤔 Why is it Needed?

- JavaScript first scans the code before executing it.
- During this phase, it collects all variable and function declarations.
- This is why some variables and functions can be accessed before they appear in the code.

---

## 🌊 Flow

```text
JavaScript Starts
        │
        ▼
Creates Execution Context
        │
        ▼
Hoists Declarations
(Variables & Functions)
        │
        ▼
Executes Code Line by Line
```

---

## ✍️ Syntax

```javascript
console.log(a);

var a = 10;
```

---

## 💻 Example

### Example 1 (`var`)

```javascript
console.log(a);

var a = 10;
```

**Output**

```text
undefined
```

**Reason:**

JavaScript internally treats it like this:

```javascript
var a; // Hoisted

console.log(a); // undefined

a = 10;
```

---

### Example 2 (`let`)

```javascript
console.log(a);

let a = 10;
```

**Output**

```text
ReferenceError
```

---

### Example 3 (`const`)

```javascript
console.log(a);

const a = 10;
```

**Output**

```text
ReferenceError
```

---

## 🎤 Interview Answer (30 Seconds)

Variable hoisting is JavaScript's behavior of moving **variable declarations** to the top of their scope before executing the code. For `var`, only the declaration is hoisted and it is initialized with `undefined`, so accessing it before declaration returns `undefined`. For `let` and `const`, they are also hoisted but remain in the **Temporal Dead Zone (TDZ)** until their declaration is reached, so accessing them before declaration throws a **ReferenceError**.

---

## 🧠 Memory Trick

```text
var
↓
Hoisted
+
undefined ✅

let
↓
Hoisted
+
TDZ ❌

const
↓
Hoisted
+
TDZ ❌
```

Easy Rule:

> **All variables are hoisted.**  
> **Only `var` can be accessed before declaration (returns `undefined`).**  
> **`let` and `const` throw `ReferenceError` because of the TDZ.**

---

## ⭐ Keywords

- Hoisting
- Declaration
- Initialization
- Execution Context
- `var`
- `let`
- `const`
- `undefined`
- Temporal Dead Zone (TDZ)
- ReferenceError
