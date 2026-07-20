# 📚 What is Reconciliation?

## 📖 Simple English Explanation

**Reconciliation** is the process React uses to **update the Real DOM efficiently**. When the **state** or **props** change, React creates a **new Virtual DOM** and compares it with the old Virtual DOM. It finds the differences and updates **only the changed parts** of the Real DOM instead of reloading the entire page. This makes React applications fast.

---

## 🤔 Why is it Needed?

- To improve application performance.
- To avoid updating the entire Real DOM.
- To update only the elements that have changed.
- Without Reconciliation, every change would reload the whole UI, making applications slower.

---

## 🌊 Flow

```text
State/Props Change
        ↓
Create New Virtual DOM
        ↓
Compare with Old Virtual DOM
        ↓
Find Differences (Diffing)
        ↓
Update Only Changed Parts
        ↓
Real DOM Updated
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

> When `setCount()` is called, React performs **Reconciliation** to update only the changed button text.

---

## 💻 Example

```jsx
// Before
<h1>Hello</h1>

// After State Change
<h1>Hello React</h1>
```

**What React does:**

```text
Old Virtual DOM
        ↓
New Virtual DOM
        ↓
Compare Both (Diffing)
        ↓
Only update:
<h1>Hello React</h1>
```

---

## 🎤 Interview Answer (30 Seconds)

**Reconciliation** is React's process of updating the **Real DOM efficiently**. When the **state** or **props** change, React creates a new **Virtual DOM**, compares it with the previous Virtual DOM using the **Diffing Algorithm**, and updates only the changed elements in the Real DOM. This improves performance by avoiding unnecessary DOM updates.

---

## 🧠 Memory Trick

📝 **Think of correcting an exam paper.**

- Old paper = **Old Virtual DOM**
- New paper = **New Virtual DOM**
- Teacher compares both papers and marks **only the changed answers**, not the whole paper.

**Reconciliation = Compare → Find Changes → Update Only Changes**

---

## ⭐ Keywords

- Reconciliation
- Virtual DOM
- Real DOM
- Diffing Algorithm
- State Change
- Props Change
- Efficient DOM Updates
- Performance
