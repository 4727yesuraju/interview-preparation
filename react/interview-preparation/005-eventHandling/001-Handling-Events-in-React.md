# Handling Events in React

## 📖 Simple English Explanation

### What is it?

**Handling Events** means **responding to user actions** such as clicking a button, typing in an input, or submitting a form.

React uses **event handlers** (functions) to handle these actions.

### Why do we need it?

- To make the application interactive.
- To respond to user actions.
- To update the UI when an event occurs.

---

## 🌊 Flow

```text
User Performs an Action
        ↓
Event Occurs (Click, Change, Submit)
        ↓
React Calls Event Handler Function
        ↓
Function Executes
        ↓
UI Updates (if state changes)
```

---

## ✍️ Syntax

```jsx
function App() {
  function handleClick() {
    console.log("Button clicked!");
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

---

## 💻 Example

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <>
      <h2>{count}</h2>

      <button onClick={handleClick}>Increment</button>
    </>
  );
}
```

**Output**

```text
Count: 0
      ↓
Click Button
      ↓
Count: 1
```

---

## 🎤 Interview Explanation

Handling events in React means **responding to user actions** like clicks, typing, or form submissions. We attach **event handler functions** to JSX elements using event props such as `onClick`, `onChange`, and `onSubmit`. When the event occurs, React calls the function, and if the function updates the state, React re-renders the component and updates the UI.

---

## 🧠 Memory Trick

🔔 **Think of a doorbell.**

- 👤 User presses the doorbell (Event).
- 🔔 Doorbell rings.
- 🚪 Someone opens the door (Event Handler).

```text
User Action
      ↓
Event
      ↓
Event Handler
      ↓
React Updates UI
```

**Remember:**

**Event → Function → UI Update**
