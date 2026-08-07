# Rules of Hooks

## 📖 Simple English Explanation

### **What are the Rules of Hooks?**

React Hooks have **rules that must be followed** so React can correctly track state and other Hook data between renders.

There are **two main rules**:

1. **Only call Hooks at the top level.**
   - Do **not** call Hooks inside loops, conditions, or nested functions.

2. **Only call Hooks inside React Function Components or Custom Hooks.**
   - Do **not** call Hooks inside regular JavaScript functions.

### **Why do we need these rules?**

- To ensure Hooks are called in the same order on every render.
- To prevent unexpected bugs.
- To help React correctly manage state and effects.

---

## 🌊 Flow

```text
Component Starts
       ↓
Call Hooks (Top Level)
       ↓
React Tracks Hook Order
       ↓
Component Renders Correctly
```

---

## ✍️ Syntax

### ✅ Correct

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return <h1>{count}</h1>;
}
```

### ❌ Incorrect

```jsx
import { useState } from "react";

function App() {
  if (true) {
    const [count, setCount] = useState(0);
  }

  return <h1>Hello</h1>;
}
```

---

## 💻 Example

### ✅ Using a Hook in a Functional Component

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return <button onClick={() => setCount(count + 1)}>{count}</button>;
}
```

### ❌ Using a Hook in a Regular Function

```jsx
import { useState } from "react";

function getCount() {
  const [count, setCount] = useState(0);
}
```

---

## 🎤 Interview Explanation

React Hooks must follow two important rules. First, **always call Hooks at the top level** of a React Functional Component or a Custom Hook, never inside loops, conditions, or nested functions. Second, **only call Hooks inside React Functional Components or Custom Hooks**, not inside regular JavaScript functions. These rules ensure React calls Hooks in the same order during every render, allowing it to manage state and effects correctly.

---

## 🧠 Memory Trick

🪝 **Remember: "Top & React"**

- ⬆️ **Top** → Call Hooks only at the top level.
- ⚛️ **React** → Call Hooks only inside React Components or Custom Hooks.

```text
✅ Top Level
       +
✅ React Component / Custom Hook
       ↓
Safe to Use Hooks
```
