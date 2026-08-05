# How does State work?

## 📖 Simple English Explanation

### What is it?

State works by **storing data inside a component**. When the state changes, React **automatically re-renders (runs) the component again** and updates only the changed part of the UI.

### Why do we need it?

- To update the UI automatically.
- To make the application interactive.
- Without state, changing data would **not** update what the user sees.

---

## 🌊 Flow

```text
Component Creates State
        ↓
User Performs an Action
        ↓
State Updates (setState / setCount)
        ↓
React Re-renders the Component
        ↓
Virtual DOM is Updated
        ↓
Real DOM is Updated
        ↓
User Sees the New UI
```

---

## ✍️ Syntax

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return <button onClick={() => setCount(count + 1)}>{count}</button>;
}
```

---

## 💻 Example

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <>
      <h2>{count}</h2>

      <button onClick={() => setCount(count + 1)}>Increment</button>
    </>
  );
}
```

### What happens?

```text
Initial State = 0
        ↓
User Clicks Button
        ↓
setCount(1)
        ↓
State Changes
        ↓
React Re-renders Component
        ↓
UI Changes from 0 → 1
```

---

## 🎤 Interview Explanation

State stores **dynamic data** inside a React component. When the state is updated using `setState` or `setCount`, React **re-renders the component**, creates a new **Virtual DOM**, compares it with the previous Virtual DOM, and updates only the changed parts of the **Real DOM**. This makes React applications fast and interactive.

---

## 🧠 Memory Trick

💡 **Think of a digital scoreboard.**

```text
Score = 0
    ↓
Player Scores
    ↓
Score Changes
    ↓
Scoreboard Updates Automatically
```

**State = Data Changes → React Updates UI**
