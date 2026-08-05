# Lifting State Up

## 📖 Simple English Explanation

### What is it?

**Lifting State Up** means **moving the state from a child component to their common parent component**.

The parent becomes the **owner of the state** and passes the data to child components using **props**.

### Why do we need it?

- To share the same data between multiple child components.
- To keep data synchronized.
- To avoid each child having its own separate state.

---

## 🌊 Flow

```text
Child A Needs Data
        ↓
Child B Needs Same Data
        ↓
Move State to Parent
        ↓
Parent Passes Data as Props
        ↓
Both Children Use the Same Data
```

---

## ✍️ Syntax

```jsx
function Parent() {
  const [count, setCount] = useState(0);

  return (
    <>
      <ChildA count={count} />
      <ChildB count={count} />
    </>
  );
}
```

---

## 💻 Example

```jsx
import { useState } from "react";

function ChildA({ count }) {
  return <h2>Count: {count}</h2>;
}

function ChildB({ count }) {
  return <p>Current Count: {count}</p>;
}

function App() {
  const [count, setCount] = useState(0);

  return (
    <>
      <button onClick={() => setCount(count + 1)}>Increment</button>

      <ChildA count={count} />
      <ChildB count={count} />
    </>
  );
}
```

**Output**

```text
Count: 0
Current Count: 0

Click Increment

Count: 1
Current Count: 1
```

Both child components display the **same updated value** because the **parent owns the state**.

---

## 🎤 Interview Explanation

**Lifting State Up** is the process of **moving state from child components to their common parent component**. The parent manages the state and passes it to the children using **props**. This allows multiple components to share the same data and stay synchronized.

---

## 🧠 Memory Trick

👨‍👧‍👦 **Think of a family.**

- 👶 Child A wants information.
- 👶 Child B wants the same information.
- 👨 Parent keeps the information and shares it with both children.

```text
      Parent (State)
      /          \
     ↓            ↓
 Child A      Child B
```

**Remember:**

**Shared Data → Move State Up → Parent → Props → Children**
