# useEffect Execution Order

## 📖 Simple English Explanation

### **What is it?**

When a component has multiple `useEffect`s, React executes them **in the order they are declared in the component**.

All normal `useEffect`s run **after the browser paints the updated UI**.

If an effect updates state, React schedules another render, and the dependency arrays determine which effects run again.

### **Why do we need to understand it?**

- To understand how multiple effects work.
- To predict which effect runs first.
- To debug effect-related problems.
- To understand state updates and re-renders.
- To avoid depending on accidental effect ordering.

---

## 🌊 Flow

Consider:

```jsx
useEffect(() => {
  console.log("Effect 1");
}, []);

useEffect(() => {
  console.log("Effect 2");
}, []);

useEffect(() => {
  console.log("Effect 3");
}, []);
```

Execution:

```text
Component Renders
       ↓
React Updates DOM
       ↓
Browser Paints
       ↓
Effect 1
       ↓
Effect 2
       ↓
Effect 3
```

So the order is:

```text
Effect 1 → Effect 2 → Effect 3
```

---

## 💻 Example

```jsx
import { useEffect } from "react";

function App() {
  useEffect(() => {
    console.log("Effect 1");
  }, []);

  useEffect(() => {
    console.log("Effect 2");
  }, []);

  useEffect(() => {
    console.log("Effect 3");
  }, []);

  return <h1>Hello</h1>;
}
```

### Console Output

```text
Effect 1
Effect 2
Effect 3
```

They execute in the **same order in which they appear in the component**.

---

## 🔄 Execution During Re-render

Consider:

```jsx
function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log("Effect 1");
  }, []);

  useEffect(() => {
    console.log("Effect 2");
  }, [count]);

  return <button onClick={() => setCount(count + 1)}>{count}</button>;
}
```

### Initial Render

```text
Render
  ↓
Browser Paint
  ↓
Effect 1
  ↓
Effect 2
```

### Click Button

```text
setCount()
    ↓
Re-render
    ↓
Browser Paint
    ↓
Effect 1 → Does NOT run
    ↓
Effect 2 → Runs
```

Why?

```text
Effect 1 → []
          ↓
No dependencies changed
          ↓
Doesn't run again


Effect 2 → [count]
          ↓
count changed
          ↓
Runs again
```

---

## 💻 Example — Effects Depending on Each Other

Consider:

```jsx
function App() {
  const [count, setCount] = useState(0);
  const [message, setMessage] = useState("");

  useEffect(() => {
    console.log("Effect 1");

    if (count > 0) {
      setMessage(`Count is ${count}`);
    }
  }, [count]);

  useEffect(() => {
    console.log("Effect 2");
  }, [message]);

  return (
    <>
      <h2>{count}</h2>
      <p>{message}</p>

      <button onClick={() => setCount(count + 1)}>Increase</button>
    </>
  );
}
```

When the button is clicked:

```text
count changes
     ↓
Re-render
     ↓
Effect 1 runs
     ↓
setMessage()
     ↓
message changes
     ↓
Another re-render
     ↓
Effect 2 runs
```

The important point is:

> A state update inside an effect causes another render. That render can cause other effects to run if their dependencies changed.

---

## 🧹 Cleanup Execution Order

Cleanup runs **before an effect runs again** when its dependencies change.

Example:

```jsx
useEffect(() => {
  console.log("Effect");

  return () => {
    console.log("Cleanup");
  };
}, [count]);
```

When `count` changes:

```text
count changes
     ↓
Re-render
     ↓
Previous Effect Cleanup
     ↓
New Effect Runs
```

So:

```text
Cleanup
   ↓
Effect
```

For unmounting:

```text
Component Unmounts
       ↓
Cleanup Runs
```

---

## 🧠 Important Point

Do not use multiple effects just because you want to create a sequence like:

```text
Effect 1
   ↓
Effect 2
   ↓
Effect 3
```

If the logic is truly dependent on a previous operation, it is often better to make that relationship explicit rather than relying only on effect order.

For example, this:

```jsx
useEffect(() => {
  // Step 1
}, []);

useEffect(() => {
  // Step 2
}, []);
```

does **not automatically mean**:

```text
Step 1 finishes
      ↓
Step 2 starts
```

It only means the effects are scheduled according to React's effect processing.

If Step 2 depends on the result of Step 1, model that dependency explicitly.

---

## 🎤 Interview Answer (30 Seconds)

When a component contains multiple `useEffect`s, React runs the effects in the order they are declared after the component has been committed and the browser has painted. On subsequent renders, React checks each effect's dependencies and runs only the effects whose dependencies changed. If an effect has a cleanup function, the previous cleanup runs before that effect runs again.

---

## 🧠 Memory Trick

Remember:

```text
Render
  ↓
DOM Update
  ↓
Browser Paint
  ↓
Effect 1
  ↓
Effect 2
  ↓
Effect 3
```

On dependency change:

```text
Dependency Changes
       ↓
Re-render
       ↓
Cleanup
       ↓
Effect Runs Again
```

👉 **Multiple effects → Declaration order**

👉 **Dependency change → Relevant effect runs**
