# Why useEffect?

## 📖 Simple English Explanation

### **What is it?**

`useEffect` is a React Hook used to perform **side effects** in a component.

A **side effect** is an operation that interacts with something outside the component's normal rendering process.

Examples:

- API calls
- Timers
- Event listeners
- Updating the document title
- Subscribing/unsubscribing to something

### **Why do we need it?**

React's main job is to **render the UI**.

But sometimes our component needs to do something **after rendering**, such as:

```text
Render UI
   ↓
Need to call API
   ↓
Need to add event listener
   ↓
Need to start timer
   ↓
Need to update document title
```

`useEffect` provides a place to handle these side effects.

---

## 🌊 Flow

```text
Component Renders
       ↓
React Updates DOM
       ↓
Browser Paints UI
       ↓
useEffect Runs
       ↓
Side Effect Happens
```

For example:

```text
Component Renders
       ↓
UI appears
       ↓
useEffect
       ↓
API Call
       ↓
Data received
       ↓
setState()
       ↓
Component Renders Again
```

---

## ✍️ Syntax

```jsx
import { useEffect } from "react";

useEffect(() => {
  // Side effect

  return () => {
    // Cleanup
  };
}, [dependencies]);
```

---

## 💻 Example

### API Call

```jsx
import { useEffect, useState } from "react";

function Users() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    fetch("/api/users")
      .then((res) => res.json())
      .then((data) => {
        setUsers(data);
      });
  }, []);

  return (
    <div>
      {users.map((user) => (
        <p key={user.id}>{user.name}</p>
      ))}
    </div>
  );
}
```

### What happens?

```text
Initial Render
      ↓
users = []
      ↓
UI renders
      ↓
useEffect runs
      ↓
API request
      ↓
Response received
      ↓
setUsers(data)
      ↓
Component renders again
      ↓
Users displayed
```

---

## 💻 Example — Event Listener

```jsx
import { useEffect, useState } from "react";

function App() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => {
      setWidth(window.innerWidth);
    };

    window.addEventListener("resize", handleResize);

    return () => {
      window.removeEventListener("resize", handleResize);
    };
  }, []);

  return <h2>{width}px</h2>;
}
```

### Why cleanup?

```text
Component Mounts
      ↓
Add Event Listener
      ↓
Component Works
      ↓
Component Unmounts
      ↓
Remove Event Listener
```

Without cleanup, the event listener could remain active unnecessarily.

---

## 🆚 What happens without useEffect?

Suppose we write:

```jsx
function App() {
  fetch("/api/users");

  return <h1>Hello</h1>;
}
```

Every time the component renders:

```text
Render
 ↓
fetch()
 ↓
State changes
 ↓
Render again
 ↓
fetch()
 ↓
Render again
 ↓
fetch()
 ↓
...
```

This can cause unnecessary API calls or even an infinite loop.

With `useEffect`:

```jsx
useEffect(() => {
  fetch("/api/users");
}, []);
```

The dependency array controls **when the effect should run**.

---

## 🧠 Dependency Array

### No dependency array

```jsx
useEffect(() => {
  console.log("Effect");
});
```

Runs after **every render**.

```text
Render → Effect
Render → Effect
Render → Effect
```

---

### Empty dependency array

```jsx
useEffect(() => {
  console.log("Effect");
}, []);
```

Runs after the **initial render**.

```text
Initial Render
      ↓
Effect
```

---

### With dependencies

```jsx
useEffect(() => {
  console.log("Effect");
}, [count]);
```

Runs after the initial render and when `count` changes.

```text
Initial Render
      ↓
Effect

count changes
      ↓
Render
      ↓
Effect
```

---

## 🧹 Cleanup Function

`useEffect` can return a cleanup function.

```jsx
useEffect(() => {
  // Setup

  return () => {
    // Cleanup
  };
}, []);
```

Common cleanup operations:

- Remove event listeners
- Clear timers
- Cancel subscriptions
- Disconnect connections

Example:

```jsx
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

---

## 🎤 Interview Answer (30 Seconds)

`useEffect` is a React Hook used to handle **side effects** in a component. Side effects include API calls, timers, event listeners, subscriptions, and updating external systems. React runs the effect after rendering, and we can use the dependency array to control when it runs. We can also return a cleanup function to remove resources such as event listeners or timers.

---

## 🧠 Memory Trick

Think of `useEffect` as:

> **"After React renders, do this work."**

```text
React Renders
      ↓
UI Updated
      ↓
useEffect
      ↓
Do Side Effect
```

### Easy Difference

```text
useState
   ↓
Store UI State

useEffect
   ↓
Handle Side Effects

useRef
   ↓
Store Value / Access DOM

useMemo
   ↓
Cache Value

useCallback
   ↓
Cache Function
```

👉 **useEffect = Handle something outside normal rendering**
