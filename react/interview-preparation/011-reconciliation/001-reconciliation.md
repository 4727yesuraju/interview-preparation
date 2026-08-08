# Reconciliation

## 📖 Simple English Explanation

### **What is it?**

**Reconciliation** is the process React uses to **compare the previous Virtual DOM with the new Virtual DOM** after a component re-renders.

React finds **what actually changed** and updates only the necessary parts of the real DOM.

This helps React update the UI efficiently instead of rebuilding the entire DOM.

### **Why do we need it?**

Without reconciliation, React could update the entire DOM whenever state or props change.

Instead, React:

```text
Old Virtual DOM
       ↓
New Virtual DOM
       ↓
Compare
       ↓
Find Changes
       ↓
Update Required DOM
```

This makes UI updates more efficient.

---

## 🌊 Flow

```text
State / Props Change
        ↓
Component Re-renders
        ↓
New Virtual DOM Created
        ↓
Compare with Previous Virtual DOM
        ↓
Find Differences
        ↓
React Updates Required DOM
        ↓
Browser Displays Updated UI
```

---

## ✍️ Syntax

There is **no specific syntax** for reconciliation.

React performs reconciliation automatically when a component re-renders.

For example:

```jsx
function App() {
  const [count, setCount] = useState(0);

  return (
    <>
      <h1>Hello</h1>
      <h2>{count}</h2>

      <button onClick={() => setCount(count + 1)}>Increase</button>
    </>
  );
}
```

When `count` changes, React automatically performs reconciliation.

---

## 💻 Example

Initial UI:

```jsx
<h1>Hello</h1>
<h2>Count: 0</h2>
```

Virtual DOM:

```text
div
├── h1 → Hello
└── h2 → Count: 0
```

After clicking the button:

```jsx
<h1>Hello</h1>
<h2>Count: 1</h2>
```

New Virtual DOM:

```text
div
├── h1 → Hello
└── h2 → Count: 1
```

React compares them:

```text
Old Virtual DOM          New Virtual DOM
      ↓                        ↓
   h1: Hello                h1: Hello
   h2: 0                    h2: 1
      \________________________/
                 ↓
              Compare
                 ↓
        h1 → No Change
        h2 → Changed
                 ↓
       Update only h2
```

So React does **not need to recreate the `<h1>`**.

It updates only the part that changed.

---

## 🔑 Role of `key` in Reconciliation

Keys are especially important when rendering lists.

Example:

```jsx
const users = [
  { id: 1, name: "John" },
  { id: 2, name: "Sam" },
  { id: 3, name: "Alex" },
];

users.map((user) => <li key={user.id}>{user.name}</li>);
```

The `key` helps React identify which list item is which.

For example:

```text
Before:

1 → John
2 → Sam
3 → Alex


After:

1 → John
3 → Alex
4 → David
```

React can understand:

```text
1 → Same item
2 → Removed
3 → Same item
4 → New item
```

Without stable keys, React can have difficulty correctly matching list items.

---

## 🆚 Re-render vs Reconciliation

These two terms are related but different.

### Re-render

React **runs the component function again**.

```text
State changes
    ↓
Component function runs again
    ↓
New JSX generated
```

### Reconciliation

React **compares the previous result with the new result** to determine what needs to change in the DOM.

```text
Old Virtual DOM
      ↓
Compare
      ↑
New Virtual DOM
      ↓
Determine Changes
```

### Easy Difference

```text
Re-render
   ↓
Create new UI description

Reconciliation
   ↓
Compare old vs new
   ↓
Find what changed
```

---

## 🆚 Reconciliation vs DOM Update

```text
State Changes
      ↓
Re-render
      ↓
Reconciliation
      ↓
Determine Changes
      ↓
DOM Update
```

So reconciliation happens **before React applies the required DOM changes**.

---

## 🎤 Interview Answer (30 Seconds)

Reconciliation is the process React uses to compare the previous Virtual DOM with the new Virtual DOM after a component re-renders. React determines what has changed and updates only the necessary parts of the real DOM. React uses techniques such as element comparison and keys for lists to efficiently determine which elements can be reused, updated, or removed.

---

## 🧠 Memory Trick

Think of reconciliation as a **Spot the Difference game** 🔍.

```text
Old UI 🖼️
   ↓
Compare
   ↕
New UI 🖼️
   ↓
Find Differences
   ↓
Update Only Differences
```

👉 **Reconciliation = Compare old UI with new UI and update what changed.**
