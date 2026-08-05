# What is State?

## 📖 Simple English Explanation

### What is it?

**State** is a **built-in React object** that stores data **inside a component**. When the state changes, React **automatically updates the UI**.

### Why do we need it?

- To store data that changes over time.
- To make the UI interactive.
- Without state, the UI cannot update automatically when data changes.

---

## 🌊 Flow

```text
Component Creates State
        ↓
User Performs an Action
        ↓
State Updates
        ↓
React Re-renders Component
        ↓
Updated UI is Displayed
```

---

## ✍️ Syntax

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);
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

**Output**

```text
0
[Increment]

Click Button

1
[Increment]

Click Again

2
```

---

## 🎤 Interview Explanation

**State** is a built-in React object used to **store and manage data inside a component**. When the state changes using `setState` or `setCount`, React automatically **re-renders the component** and updates the UI. State is mainly used for **dynamic data** such as counters, forms, user input, and API responses.

---

## 🧠 Memory Trick

🏠 **Think of State as your personal notebook.**

- 📖 It belongs to **you (the component)**.
- ✏️ You can **read and update** it anytime.
- 🔄 When you update it, React **refreshes the UI**.

**State = Store Data + Update UI**
