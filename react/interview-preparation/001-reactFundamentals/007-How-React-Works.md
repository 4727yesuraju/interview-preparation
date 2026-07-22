# 📚 How Does React Work?

## 📖 Simple English Explanation

React works by building the UI using **components**. When the **state** or **props** change, React creates a **new Virtual DOM** and compares it with the previous Virtual DOM. It finds the differences and updates **only the changed parts** of the **Real DOM**, making the application fast and efficient.

---

## 🤔 Why is it Needed?

- To build fast and interactive web applications.
- To avoid updating the entire webpage for every change.
- To improve performance using the Virtual DOM.
- Without React, developers would need to manually update the DOM, making applications slower and harder to maintain.

---

## 🌊 Flow

```text
User Interacts with UI
          ↓
State/Props Change
          ↓
React Creates New Virtual DOM
          ↓
Compares with Old Virtual DOM (Diffing)
          ↓
Finds Changed Elements
          ↓
Updates Only Changed Parts in Real DOM
          ↓
Browser Displays Updated UI
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
function App() {
  const [name, setName] = useState("Yesu");

  return (
    <>
      <h1>{name}</h1>
      <button onClick={() => setName("React")}>Change Name</button>
    </>
  );
}
```

**What happens?**

- User clicks the button.
- State changes from `"Yesu"` to `"React"`.
- React creates a new Virtual DOM.
- React compares it with the old Virtual DOM.
- Only the `<h1>` text is updated in the Real DOM.

---

## 🎤 Interview Answer (30 Seconds)

React works using a **component-based architecture** and a **Virtual DOM**. When the **state** or **props** change, React creates a new Virtual DOM and compares it with the previous one using the **Diffing Algorithm**. It then updates only the changed parts of the **Real DOM** through **Reconciliation**, making React applications fast and efficient.

---

## 🧠 Memory Trick

🏠 **Think of repainting one room in a house.**

- ❌ Traditional approach = Repaint the **entire house**.
- ✅ React = Repaint **only the room that changed**.

**React = Compare → Update Only Changes**

---

## ⭐ Keywords

- Components
- State
- Props
- Virtual DOM
- Real DOM
- Diffing Algorithm
- Reconciliation
- Rendering
- Efficient Updates
