# useRef with Forms

## 📖 Simple English Explanation

### **What is it?**

`useRef` is a React Hook that lets us **access DOM elements directly**. In forms, it is commonly used to **read input values without storing them in React state**.

### **Why do we need it?**

- To access input values directly.
- To avoid re-rendering on every keystroke.
- To work with **Uncontrolled Components**.
- To focus, clear, or manipulate input fields.

---

## 🌊 Flow

```text
User Types
      ↓
DOM Stores Input Value
      ↓
useRef References the Input
      ↓
Read Value When Needed
```

---

## ✍️ Syntax

```jsx
import { useRef } from "react";

function App() {
  const inputRef = useRef();

  function handleSubmit() {
    console.log(inputRef.current.value);
  }

  return (
    <>
      <input ref={inputRef} />
      <button onClick={handleSubmit}>Submit</button>
    </>
  );
}
```

---

## 💻 Example

```jsx
import { useRef } from "react";

function App() {
  const nameRef = useRef();

  function handleSubmit() {
    alert(`Welcome ${nameRef.current.value}`);
  }

  return (
    <>
      <input ref={nameRef} placeholder="Enter your name" />

      <button onClick={handleSubmit}>Submit</button>
    </>
  );
}
```

**Output:**

```text
Input:
Yesu

Click Submit

Alert:
Welcome Yesu
```

---

## 🎤 Interview Explanation

`useRef` with forms is used to **access form input values directly from the DOM** without storing them in React state. It is commonly used with **Uncontrolled Components**, where React does not manage the input value. This reduces unnecessary re-renders and is useful for simple forms, focusing input fields, or integrating with third-party libraries.

---

## 🧠 Memory Trick

📝 **Think of `useRef` as a Bookmark.**

- 📖 The input field is a book.
- 🔖 `useRef` is the bookmark that remembers where the input is.
- 👀 Whenever you need the value, open the bookmarked page and read it.

```text
Input
  ↓
useRef (🔖)
  ↓
Read Value Anytime
```
