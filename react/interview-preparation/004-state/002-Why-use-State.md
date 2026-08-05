# Why use State?

## 📖 Simple English Explanation

### What is it?

We use **State** to store **data that can change** inside a component. When the state changes, React **automatically updates the UI**.

### Why do we need it?

- To make the UI interactive.
- To update the screen automatically when data changes.
- To store dynamic data like counters, form inputs, and API responses.
- Without state, changing a value **does not update the UI**.

---

## 🌊 Flow

```text
Create State
      ↓
User Performs an Action
      ↓
Update State
      ↓
React Re-renders Component
      ↓
UI Updates Automatically
```

---

## ✍️ Syntax

```jsx
const [count, setCount] = useState(0);
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
↓ Click
1
↓ Click
2
```

---

## 🎤 Interview Explanation

We use **State** to store **dynamic data** inside a component. When the state changes, React automatically **re-renders the component** and updates the UI. State is commonly used for **counters, form inputs, API data, toggles, and user interactions**.

---

## 🧠 Memory Trick

💡 **State = Memory of a Component**

```text
Store Data
     ↓
Data Changes
     ↓
UI Changes
```

**Remember:**

**State Changes → UI Changes**
