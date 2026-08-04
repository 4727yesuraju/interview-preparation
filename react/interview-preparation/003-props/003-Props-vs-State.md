# Props vs State

## 📖 Simple English Explanation

**What is it?**

**Props** and **State** are both used to store data in React, but they are used differently.

- **Props** are used to **pass data from a parent component to a child component**.
- **State** is used to **store and manage data inside a component**.

**Why do we need it?**

- Use **Props** to share data between components.
- Use **State** when the data changes over time (like a counter, form input, or toggle).

---

## 🌊 Flow

```text
Props:
Parent
   ↓
Child (Read Only)

State:
Component
   ↓
Stores Data
   ↓
Data Changes
   ↓
UI Updates
```

---

## ✍️ Syntax

### Props

```jsx
function Child(props) {
  return <h1>{props.name}</h1>;
}
```

### State

```jsx
const [count, setCount] = useState(0);
```

---

## 💻 Example

```jsx
import { useState } from "react";

function Counter({ title }) {
  const [count, setCount] = useState(0);

  return (
    <>
      <h2>{title}</h2>
      <p>{count}</p>

      <button onClick={() => setCount(count + 1)}>Increment</button>
    </>
  );
}

function App() {
  return <Counter title="Counter App" />;
}
```

- `title` → **Prop** (comes from parent)
- `count` → **State** (managed inside the component)

---

## 🎤 Interview Explanation

**Props** are used to **pass data from a parent component to a child component**, and they are **read-only**. **State** is used to **store and manage data inside a component**, and it can be updated using functions like `setState` or `useState`. In simple terms, **Props are received, State is managed.**

---

## 🧠 Memory Trick

📦 **Props = Parcel**

- Someone **sends** it to you.
- You can **use** it.
- You **cannot change** it.

🏠 **State = Personal Diary**

- It belongs to **you**.
- You can **read and update** it anytime.

**Props = Receive**

**State = Manage**
