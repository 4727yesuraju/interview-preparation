# Controlled vs Uncontrolled Components

## 📖 Simple English Explanation

### What is it?

React provides **two ways to handle form inputs**:

- **Controlled Component** → React **controls** the input value using **State**.
- **Uncontrolled Component** → The **browser (DOM)** controls the input value. React reads the value using a **ref**.

### Why do we need it?

- **Controlled Components** are best when React needs to manage and validate the input.
- **Uncontrolled Components** are useful for simple forms or when working with existing HTML forms.

---

## 🌊 Flow

### Controlled Component

```text
User Types
      ↓
State Updates
      ↓
React Updates Input
```

### Uncontrolled Component

```text
User Types
      ↓
Browser Stores Value
      ↓
React Reads Value using Ref
```

---

## ✍️ Syntax

### Controlled Component

```jsx
const [name, setName] = useState("");

<input value={name} onChange={(e) => setName(e.target.value)} />;
```

### Uncontrolled Component

```jsx
const inputRef = useRef();

<input ref={inputRef} />;
```

---

## 💻 Example

### Controlled Component

```jsx
import { useState } from "react";

function App() {
  const [name, setName] = useState("");

  return (
    <input
      value={name}
      onChange={(e) => setName(e.target.value)}
      placeholder="Enter your name"
    />
  );
}
```

---

### Uncontrolled Component

```jsx
import { useRef } from "react";

function App() {
  const inputRef = useRef();

  function showValue() {
    alert(inputRef.current.value);
  }

  return (
    <>
      <input ref={inputRef} />
      <button onClick={showValue}>Show</button>
    </>
  );
}
```

---

## 🎤 Interview Explanation

A **Controlled Component** is a form input whose value is managed by **React State** using `useState`. An **Uncontrolled Component** is a form input whose value is managed by the **browser's DOM**, and React accesses the value using **`useRef`**. In modern React, **Controlled Components are recommended** because they make form handling, validation, and UI updates easier.

---

## 🧠 Memory Trick

🎮 **Controlled = Remote Control**

- 📺 React holds the remote.
- React controls the input.

🚗 **Uncontrolled = Manual Car**

- Driver (Browser) controls the car.
- React checks the value only when needed.

```text
Controlled → React Controls ✅

Uncontrolled → Browser Controls
```
