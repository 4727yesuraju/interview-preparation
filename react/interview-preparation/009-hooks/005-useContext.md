# useEffect

## 📖 Simple English Explanation

### **What is it?**

`useEffect` is a **React Hook** that lets you **perform side effects** in a Functional Component.

A **side effect** is any operation that happens outside of rendering the UI, such as:

- Fetching data from an API
- Setting a timer
- Adding event listeners
- Updating the document title

### **Why do we need it?**

- To fetch data from APIs.
- To perform actions after a component renders.
- To set up timers or intervals.
- To add and remove event listeners.
- To synchronize the component with external systems.

---

## 🌊 Flow

```text
Component Renders
        ↓
useEffect Runs
        ↓
Perform Side Effect
(API Call, Timer, Event Listener, etc.)
        ↓
State Updates (Optional)
        ↓
React Re-renders (if state changes)
```

---

## ✍️ Syntax

```jsx
import { useEffect } from "react";

function App() {
  useEffect(() => {
    console.log("Component Rendered");
  }, []);

  return <h1>Hello React</h1>;
}
```

---

## 💻 Example

```jsx
import { useEffect, useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);

  return (
    <>
      <h2>{count}</h2>

      <button onClick={() => setCount(count + 1)}>Increment</button>
    </>
  );
}
```

**Output:**

```text
Initial:
Count: 0
Browser Tab Title:
Count: 0

Click Increment

Count: 1
Browser Tab Title:
Count: 1
```

---

## 🎤 Interview Explanation

`useEffect` is a React Hook used to perform **side effects** in Functional Components. It runs after the component renders and is commonly used for API calls, timers, event listeners, and updating the document title. The **dependency array** controls when the effect runs. An empty array (`[]`) runs the effect only once after the initial render, while specifying dependencies runs the effect whenever those values change.

---

## 🧠 Memory Trick

⚡ **Think of `useEffect` as an Electric Switch.**

- 🏠 Component = House
- ⚡ `useEffect` = Switch
- 💡 After the house is built (rendered), turn on the electricity (side effects).

```text
Component Renders
        ↓
useEffect
        ↓
Run Side Effect
```
