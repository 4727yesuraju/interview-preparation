# useCallback

## 📖 Simple English Explanation

### **What is it?**

`useCallback` is a **React Hook** used to **memoize (cache) a function**.

React remembers the function and returns the **same function reference** until one of its dependencies changes.

### **Why do we need it?**

- To avoid creating a new function reference on every render.
- Useful when passing functions to **memoized child components**.
- Helps prevent unnecessary child component re-renders.
- Useful when a function is used as a dependency of another Hook.

> ⚠️ `useCallback` is mainly a **performance optimization**, not something required for every function.

---

## 🌊 Flow

```text
Component Renders
        ↓
useCallback Checks Dependencies
        ↓
Dependencies Changed?
    ↓            ↓
   No            Yes
    ↓             ↓
Return Same     Create New
Function        Function
Reference       Reference
    ↓             ↓
    └──────→ Return Function
```

---

## ✍️ Syntax

```jsx
import { useCallback } from "react";

const functionName = useCallback(() => {
  // function logic
}, [dependencies]);
```

---

## 💻 Example

```jsx
import { useCallback, useState, memo } from "react";

const Child = memo(({ handleClick }) => {
  console.log("Child rendered");

  return <button onClick={handleClick}>Click Child</button>;
});

function App() {
  const [count, setCount] = useState(0);
  const [number, setNumber] = useState(10);

  const handleClick = useCallback(() => {
    console.log("Button clicked");
  }, []);

  return (
    <>
      <h2>Count: {count}</h2>
      <h2>Number: {number}</h2>

      <button onClick={() => setCount(count + 1)}>Increase Count</button>

      <Child handleClick={handleClick} />
    </>
  );
}
```

### What happens?

```text
Initial Render
      ↓
handleClick is created
      ↓
Child receives handleClick
      ↓
Child renders

Click "Increase Count"
      ↓
App re-renders
      ↓
useCallback returns SAME handleClick
      ↓
Child receives SAME function reference
      ↓
React.memo prevents unnecessary Child render
```

### Without `useCallback`

```text
App Re-renders
      ↓
New handleClick function is created
      ↓
Different function reference
      ↓
Child thinks prop changed
      ↓
Child re-renders
```

---

## 🎤 Interview Answer (30 Seconds)

`useCallback` is a React Hook used to **memoize a function reference** between renders. It returns the same function as long as its dependencies have not changed. It is mainly useful when passing callback functions to memoized child components or when a function is used as a dependency of another Hook.

---

## 🧠 Memory Trick

Think of **`useCallback` as a Function with Memory**.

```text
First Render
     ↓
Create Function
     ↓
Remember Function 🧠
     ↓
Render Again
     ↓
Dependencies Changed?
   ↓           ↓
  No           Yes
   ↓            ↓
Use Same     Create New
Function     Function
```

👉 **useCallback = Remember the FUNCTION**

### Easy Difference

```text
useMemo
   ↓
Remember the VALUE

useCallback
   ↓
Remember the FUNCTION
```

---
