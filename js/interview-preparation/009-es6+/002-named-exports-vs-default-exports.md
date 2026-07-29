# 📚 Named Exports vs Default Exports

## 📖 Simple English Explanation

JavaScript provides **two ways to export code from a module**:

1. **Named Export** → Export one or more values by **name**.
2. **Default Export** → Export **one main value** from a file.

The main difference is **how you export and import them**.

---

## 🤔 Why is it Needed?

- **Named Exports** → Export multiple functions, variables, or classes from the same file.
- **Default Export** → Export one primary function, class, or object from a file.

---

## 🌊 Flow

### Named Export

```text
math.js
 │
 ├── export add()
 ├── export subtract()
 └── export multiply()
        │
        ▼
app.js
        │
import { add, subtract }
```

---

### Default Export

```text
math.js
 │
 └── export default add()
         │
         ▼
app.js
         │
import add
```

---

## ✍️ Syntax

### Named Export

```javascript
// math.js
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}
```

```javascript
// app.js
import { add, subtract } from "./math.js";
```

---

### Default Export

```javascript
// math.js
export default function add(a, b) {
  return a + b;
}
```

```javascript
// app.js
import add from "./math.js";
```

---

## 💻 Example

### Example 1: Named Export

**math.js**

```javascript
export function add(a, b) {
  return a + b;
}

export function multiply(a, b) {
  return a * b;
}
```

**app.js**

```javascript
import { add, multiply } from "./math.js";

console.log(add(5, 3));
console.log(multiply(5, 3));
```

**Output**

```text
8
15
```

---

### Example 2: Default Export

**greet.js**

```javascript
export default function greet(name) {
  return `Hello ${name}`;
}
```

**app.js**

```javascript
import greet from "./greet.js";

console.log(greet("John"));
```

**Output**

```text
Hello John
```

---

### Example 3: Rename During Import

```javascript
// math.js
export function add(a, b) {
  return a + b;
}
```

```javascript
// app.js
import { add as sum } from "./math.js";

console.log(sum(2, 3));
```

**Output**

```text
5
```

---

## 📋 Comparison

| Feature                    | Named Export                      | Default Export                 |
| -------------------------- | --------------------------------- | ------------------------------ |
| Number of exports per file | Multiple                          | Only one                       |
| Import with `{}`           | ✅ Yes                            | ❌ No                          |
| Import name must match?    | ✅ Yes (unless renamed with `as`) | ❌ No (can use any name)       |
| Best for                   | Utility files with many exports   | One main function/class/object |

---

## 🎤 Interview Answer (30 Seconds)

Named exports allow a module to export multiple values, and they must be imported using the same names inside curly braces. Default export allows a module to export one main value, and it is imported without curly braces. Use named exports when a file contains multiple reusable items, and use a default export when the file has one primary item.

---

## 🧠 Memory Trick

```text
Named Export
────────────
export add
export subtract
       │
       ▼
import { add, subtract }


Default Export
──────────────
export default greet
         │
         ▼
import greet
```

Easy Rule:

> **Named Export = Many Things `{ }`**

> **Default Export = One Main Thing (No `{ }`)**

---

## ⭐ Keywords

- Named Export
- Default Export
- export
- export default
- import
- Curly Braces
- ES Modules
- Reusable Code
