# Controlled & Uncontrolled Components

## 📖 Simple English Explanation

### **What are Controlled Components?**

A **Controlled Component** is a form element whose value is **controlled by React State**.

Whenever the user types something, React updates the state using `setState` (or `useState`), and the input value always comes from the state.

### **Why do we need it?**

- To validate user input.
- To update UI instantly.
- To easily submit form data.
- To keep React as the single source of truth.

---

### **What are Uncontrolled Components?**

An **Uncontrolled Component** is a form element whose value is **controlled by the DOM (browser)** instead of React.

React uses a **ref** to access the value only when needed.

### **Why do we need it?**

- For simple forms.
- When React doesn't need to track every change.
- When integrating with non-React libraries.

---

## 🌊 Flow

### Controlled Component

```text
User Types
      ↓
onChange Event
      ↓
React State Updates
      ↓
Input Value Updates from State
```

### Uncontrolled Component

```text
User Types
      ↓
DOM Stores Value
      ↓
React Uses Ref
      ↓
Read Value When Needed
```

---

## ✍️ Syntax

### Controlled Component

```jsx
import { useState } from "react";

function App() {
  const [name, setName] = useState("");

  return <input value={name} onChange={(e) => setName(e.target.value)} />;
}
```

### Uncontrolled Component

```jsx
import { useRef } from "react";

function App() {
  const inputRef = useRef();

  const showValue = () => {
    alert(inputRef.current.value);
  };

  return (
    <>
      <input ref={inputRef} />
      <button onClick={showValue}>Submit</button>
    </>
  );
}
```

---

## 💻 Example

### Controlled Component

```jsx
import { useState } from "react";

function App() {
  const [username, setUsername] = useState("");

  return (
    <>
      <input value={username} onChange={(e) => setUsername(e.target.value)} />

      <h3>{username}</h3>
    </>
  );
}
```

**Output**

```text
Input: Yesu

Display:
Yesu
```

---

### Uncontrolled Component

```jsx
import { useRef } from "react";

function App() {
  const inputRef = useRef();

  function handleSubmit() {
    alert(inputRef.current.value);
  }

  return (
    <>
      <input ref={inputRef} />
      <button onClick={handleSubmit}>Submit</button>
    </>
  );
}
```

**Output**

```text
Type: Yesu

Click Submit

Alert:
Yesu
```

---

## 📊 Difference Between Controlled & Uncontrolled Components

| Feature        | Controlled    | Uncontrolled |
| -------------- | ------------- | ------------ |
| Data Stored In | React State   | DOM          |
| Controlled By  | React         | Browser      |
| Uses           | useState      | useRef       |
| Re-render      | Yes           | No           |
| Validation     | Easy          | Hard         |
| Best For       | Complex Forms | Simple Forms |

---

## 🎤 Interview Explanation

A **Controlled Component** is a form element whose value is managed by **React State** using `useState`. Every time the user types, React updates the state, making React the **single source of truth**. This approach is ideal for form validation, dynamic UI updates, and controlled user input.

An **Uncontrolled Component** stores its value in the **DOM**, and React accesses it using **useRef** only when needed. It is simpler and can offer slightly better performance for basic forms because React doesn't re-render on every keystroke.

---

## 🧠 Memory Trick

🎮 **Controlled = Remote Control**

- React holds the remote 🎮
- React decides what appears in the input.

```text
React State
      ↓
Input
```

---

📝 **Uncontrolled = Notebook**

- User writes directly in the notebook.
- React reads it only when needed.

```text
DOM
 ↓
Stores Value
 ↓
React Reads using Ref
```

---

## ⭐ Quick Revision

- ✅ Controlled → React State (`useState`)
- ✅ Uncontrolled → DOM (`useRef`)
- ✅ Controlled → Easy validation
- ✅ Controlled → More re-renders
- ✅ Uncontrolled → Less React code
- ✅ Uncontrolled → Better for simple forms
- ✅ React recommends **Controlled Components** for most forms.
