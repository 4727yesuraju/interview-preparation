# Multiple useEffects

## 📖 Simple English Explanation

### **What is it?**

A component can have **multiple `useEffect` Hooks**.

We use multiple effects when a component has **different side effects that are independent of each other**.

For example, one effect can fetch API data, while another effect can update the document title.

Each `useEffect` has its **own dependency array and cleanup function**.

### **Why do we need it?**

- To keep different side effects separate.
- To make code easier to understand.
- Each effect can have its own dependencies.
- Each effect can have its own cleanup logic.
- Avoid putting unrelated logic into one large `useEffect`.

> 🧠 **One effect = One logical side effect** is a good practice.

---

## 🌊 Flow

```text
Component Renders
       ↓
   ┌───┴───────────────┐
   ↓                   ↓
useEffect #1        useEffect #2
   ↓                   ↓
Fetch API          Update Title
   ↓                   ↓
Its Dependencies    Its Dependencies
```

React checks each effect **independently**.

---

## ✍️ Syntax

```jsx
useEffect(() => {
  // Side Effect 1
}, [dependency1]);

useEffect(() => {
  // Side Effect 2
}, [dependency2]);
```

---

## 💻 Example

```jsx
import { useEffect, useState } from "react";

function App() {
  const [users, setUsers] = useState([]);
  const [count, setCount] = useState(0);

  // Effect 1: Fetch users
  useEffect(() => {
    fetch("/api/users")
      .then((response) => response.json())
      .then((data) => {
        setUsers(data);
      });
  }, []);

  // Effect 2: Update document title
  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);

  return (
    <>
      <h2>Count: {count}</h2>

      <button onClick={() => setCount(count + 1)}>Increase</button>

      <h2>Users: {users.length}</h2>
    </>
  );
}
```

---

## 🔄 How Does It Work?

### Initial Render

```text
Component Renders
       ↓
React Updates DOM
       ↓
Browser Paints
       ↓
useEffect #1 runs
       ↓
Fetch Users
       ↓
useEffect #2 runs
       ↓
Update Document Title
```

Both effects run after the initial render because their dependencies allow them to run.

---

### When `count` Changes

```text
Click Increase
      ↓
count changes
      ↓
Component Re-renders
      ↓
React checks dependencies
      ↓
useEffect #1
      ↓
[] → Nothing changed
      ↓
Does NOT run

useEffect #2
      ↓
[count] → count changed
      ↓
Runs
      ↓
Updates document title
```

So only the relevant effect runs.

---

## 🧹 Multiple Cleanup Functions

Each `useEffect` can have its own cleanup.

```jsx
useEffect(() => {
  const timer = setInterval(() => {
    console.log("Timer");
  }, 1000);

  return () => {
    clearInterval(timer);
  };
}, []);

useEffect(() => {
  const handleResize = () => {
    console.log(window.innerWidth);
  };

  window.addEventListener("resize", handleResize);

  return () => {
    window.removeEventListener("resize", handleResize);
  };
}, []);
```

Each effect manages its own resource:

```text
useEffect #1
    ↓
Timer
    ↓
clearInterval()


useEffect #2
    ↓
Event Listener
    ↓
removeEventListener()
```

This makes cleanup easier to understand.

---

## 🆚 One useEffect vs Multiple useEffects

### ❌ One Large Effect

```jsx
useEffect(() => {
  // Fetch users
  // Update document title
  // Start timer
  // Add event listener
  // More unrelated logic...
}, []);
```

This can become difficult to maintain.

### ✅ Multiple Effects

```jsx
useEffect(() => {
  // Fetch users
}, []);

useEffect(() => {
  // Update document title
}, [count]);

useEffect(() => {
  // Start timer
}, []);

useEffect(() => {
  // Add event listener
}, []);
```

Each effect has a **single responsibility**.

---

## ⚠️ Important Point

Multiple `useEffect`s do **not mean multiple components**.

They all belong to the **same component**.

```text
App Component
     │
     ├── useEffect #1
     │
     ├── useEffect #2
     │
     └── useEffect #3
```

React manages each effect separately.

---

## 🎤 Interview Answer (30 Seconds)

A React component can have multiple `useEffect` Hooks. We use them when a component has different and independent side effects, such as fetching data, updating the document title, or adding event listeners. Each effect has its own dependency array and cleanup function, so React can run them independently. This keeps the code easier to understand and maintain.

---

## 🧠 Memory Trick

Think:

> **One `useEffect` = One Job**

```text
Component
   ↓
┌──────────────┐
│ useEffect #1 │ → API
└──────────────┘

┌──────────────┐
│ useEffect #2 │ → Title
└──────────────┘

┌──────────────┐
│ useEffect #3 │ → Timer
└──────────────┘
```

👉 **Multiple side effects → Multiple `useEffect`s**

👉 **Keep unrelated effects separate**
