# What are Hooks?

## 📖 Simple English Explanation

### **What is it?**

**Hooks** are **special functions in React** that let you use React features like **state, lifecycle methods, context, and refs** inside **Functional Components**.

Before Hooks were introduced, these features were only available in **Class Components**.

### **Why do we need it?**

- To use state in Functional Components.
- To perform side effects (API calls, timers, etc.).
- To access Context.
- To work with DOM elements using refs.
- To write cleaner and reusable logic.

---

## 🌊 Flow

```text
Functional Component
        ↓
Use React Hook
        ↓
Access React Features
        ↓
Manage State, Effects, Context, Refs, etc.
```

---

## ✍️ Syntax

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

---

## 💻 Example

```jsx
import { useState } from "react";

function App() {
  const [name, setName] = useState("Yesu");

  return (
    <>
      <h2>{name}</h2>

      <button onClick={() => setName("Raju")}>Change Name</button>
    </>
  );
}
```

**Output:**

```text
Initial:
Yesu

Click Button

Updated:
Raju
```

---

## 🎤 Interview Explanation

**Hooks** are special functions introduced in **React 16.8** that allow Functional Components to use React features such as **state, lifecycle methods, context, and refs**. They make code simpler, reusable, and eliminate the need to write Class Components for most use cases. Some commonly used Hooks are `useState`, `useEffect`, `useContext`, `useRef`, and `useReducer`.

---

## 🧠 Memory Trick

🪝 **Think of Hooks as Tools on a Tool Belt.**

- 👨‍🔧 Functional Component = Worker
- 🪝 Hooks = Tools attached to the belt
- 🛠️ Each Hook provides a different React feature.

```text
Functional Component
        ↓
     Hooks 🪝
        ↓
State • Effects • Context • Refs
```
