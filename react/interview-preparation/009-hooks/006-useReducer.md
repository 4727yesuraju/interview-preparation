# useReducer

## 📖 Simple English Explanation

### **What is it?**

`useReducer` is a **React Hook** used to **manage complex state** in a Functional Component.

Instead of updating the state directly, you **dispatch an action**, and a **reducer function** decides how the state should change.

### **Why do we need it?**

- To manage complex state logic.
- To keep state updates organized.
- To handle multiple related state values.
- To make the code easier to maintain in large applications.

---

## 🌊 Flow

```text
User Action
      ↓
dispatch(action)
      ↓
Reducer Function
      ↓
Update State
      ↓
React Re-renders Component
```

---

## ✍️ Syntax

```jsx
import { useReducer } from "react";

function reducer(state, action) {
  switch (action.type) {
    case "increment":
      return { count: state.count + 1 };

    default:
      return state;
  }
}

function App() {
  const [state, dispatch] = useReducer(reducer, { count: 0 });

  return (
    <>
      <h2>{state.count}</h2>

      <button onClick={() => dispatch({ type: "increment" })}>Increment</button>
    </>
  );
}
```

---

## 💻 Example

```jsx
import { useReducer } from "react";

function reducer(state, action) {
  switch (action.type) {
    case "increment":
      return { count: state.count + 1 };

    case "decrement":
      return { count: state.count - 1 };

    case "reset":
      return { count: 0 };

    default:
      return state;
  }
}

function App() {
  const [state, dispatch] = useReducer(reducer, { count: 0 });

  return (
    <>
      <h2>Count: {state.count}</h2>

      <button onClick={() => dispatch({ type: "increment" })}>+</button>

      <button onClick={() => dispatch({ type: "decrement" })}>-</button>

      <button onClick={() => dispatch({ type: "reset" })}>Reset</button>
    </>
  );
}
```

**Output:**

```text
Initial:
Count: 0

Click +
Count: 1

Click -
Count: 0

Click Reset
Count: 0
```

---

## 🎤 Interview Explanation

`useReducer` is a React Hook used for **managing complex state**. It works by using a **reducer function** that receives the current state and an action, then returns the new state. State updates are performed by calling `dispatch(action)`. It is useful when state logic becomes complex or when multiple state values need to be managed together. It follows the same pattern as Redux but is built into React.

---

## 🧠 Memory Trick

🏢 **Think of `useReducer` as an Office Manager.**

- 👨 Employee = User
- 📝 Action = Request (`increment`, `decrement`, `reset`)
- 👔 Reducer = Manager who decides what to do
- 📦 State = Office Records

```text
User Action
      ↓
dispatch()
      ↓
Reducer
      ↓
Update State
      ↓
React Re-renders
```
