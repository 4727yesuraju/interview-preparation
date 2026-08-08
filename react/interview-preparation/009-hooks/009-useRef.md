# useRef

## 📖 Simple English Explanation

### **What is it?**

`useRef` is a **React Hook** used to store a value that **persists between renders**.

It returns a ref object with a `.current` property.

Changing `ref.current` **does not cause the component to re-render**.

`useRef` is also commonly used to **access DOM elements directly**.

### **Why do we need it?**

- To access DOM elements directly.
- To store a value that should persist between renders.
- To store previous values.
- To store timer IDs, interval IDs, or other mutable values.
- To change a value without causing a re-render.

> ⚠️ Unlike `useState`, changing `ref.current` does **not** trigger a re-render.

---

## 🌊 Flow

```text
Component Renders
       ↓
useRef Creates Ref Object
       ↓
ref.current stores a value
       ↓
Component Re-renders
       ↓
Same Ref Object is Preserved
       ↓
ref.current still contains the value
```

### Updating `useRef`

```text
ref.current = newValue
       ↓
Value Changes
       ↓
No Re-render
```

---

## ✍️ Syntax

```jsx
import { useRef } from "react";

const ref = useRef(initialValue);
```

Access or update the value:

```jsx
ref.current = newValue;

console.log(ref.current);
```

---

## 💻 Example 1 — Accessing DOM Element

```jsx
import { useRef } from "react";

function App() {
  const inputRef = useRef(null);

  const handleFocus = () => {
    inputRef.current.focus();
  };

  return (
    <>
      <input ref={inputRef} />

      <button onClick={handleFocus}>Focus Input</button>
    </>
  );
}
```

### What happens?

```text
Initial Render
      ↓
inputRef.current = input element
      ↓
Click "Focus Input"
      ↓
inputRef.current.focus()
      ↓
Input gets focus
```

Here, `useRef` allows us to directly access the DOM element.

---

## 💻 Example 2 — Store a Value Without Re-render

```jsx
import { useRef, useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  const renderCount = useRef(0);

  renderCount.current += 1;

  return (
    <>
      <h2>Count: {count}</h2>

      <h2>Render Count: {renderCount.current}</h2>

      <button onClick={() => setCount(count + 1)}>Increase</button>
    </>
  );
}
```

`renderCount.current` persists between renders, but changing it directly does not cause a render.

---

## 💻 Example 3 — Store Previous Value

```jsx
import { useEffect, useRef, useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  const previousCount = useRef();

  useEffect(() => {
    previousCount.current = count;
  }, [count]);

  return (
    <>
      <h2>Current: {count}</h2>

      <h2>Previous: {previousCount.current}</h2>

      <button onClick={() => setCount(count + 1)}>Increase</button>
    </>
  );
}
```

### Flow

```text
count = 0
previousCount = undefined

        ↓

Click Increase

        ↓

count = 1

        ↓

Component Re-renders

        ↓

previousCount = 0

        ↓

After useEffect

        ↓

previousCount.current = 1
```

---

## 🆚 useRef vs useState

| Feature                         | useRef     | useState |
| ------------------------------- | ---------- | -------- |
| Stores value                    | ✅         | ✅       |
| Persists between renders        | ✅         | ✅       |
| Changing value causes re-render | ❌         | ✅       |
| Access DOM element              | ✅         | ❌       |
| Access value using `.current`   | ✅         | ❌       |
| Used for UI data                | Usually ❌ | ✅       |

### Easy Rule

```text
Need UI to update?
       ↓
    useState

Need value to persist
without re-render?
       ↓
    useRef
```

---

## 🎤 Interview Answer (30 Seconds)

`useRef` is a React Hook that returns a mutable object with a `.current` property. The value stored in `ref.current` persists across component renders, but changing it does not trigger a re-render. It is commonly used to access DOM elements directly and to store values such as previous values, timer IDs, or other mutable data that does not need to update the UI.

---

## 🧠 Memory Trick

Think of **`useRef` as a Small Persistent Box** 📦.

```text
useRef()
   ↓
Creates a Box 📦
   ↓
box.current
   ↓
Store Value
   ↓
Component Re-renders
   ↓
Same Box 📦
   ↓
Value is still there
```

👉 **useRef = Remember a value without re-rendering**

### Easy Difference

```text
useState
   ↓
Change value
   ↓
Re-render UI

useRef
   ↓
Change value
   ↓
No re-render
```

---
