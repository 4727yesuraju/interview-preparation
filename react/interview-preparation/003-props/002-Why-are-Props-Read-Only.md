# Why are Props Read-only?

## 📖 Simple English Explanation

**What is it?**

**Props are read-only**, which means a child component can **use** the props but **cannot change** them.

**Why do we need it?**

- To keep the data predictable and consistent.
- To ensure only the **parent component** controls and updates the data.
- If child components could change props, it would become difficult to track where the data changed, leading to bugs.

---

## 🌊 Flow

```text
Parent Component
        ↓
Passes Props
        ↓
Child Component Reads Props
        ↓
Cannot Modify Props
        ↓
If Data Needs to Change
        ↓
Parent Updates Props
```

---

## ✍️ Syntax

```jsx
function Child(props) {
  return <h1>{props.name}</h1>;
}

function Parent() {
  return <Child name="Yesu" />;
}
```

❌ **Don't do this:**

```jsx
props.name = "Raju"; // Error (Never modify props)
```

---

## 💻 Example

```jsx
function Greeting(props) {
  return <h2>Hello, {props.name}</h2>;
}

function App() {
  return <Greeting name="Yesu" />;
}
```

If you want to display `"Raju"` instead, **change it in the parent**:

```jsx
<Greeting name="Raju" />
```

---

## 🎤 Interview Explanation

Props are **read-only** because React follows **one-way data flow**. The **parent component owns the data** and passes it to the child through props. The child can only read and use the props, not modify them. This keeps the application predictable, easier to debug, and easier to maintain.

---

## 🧠 Memory Trick

📚 **Think of borrowing a library book.**

- 📖 You can **read** the book.
- ❌ You cannot **rewrite** its contents.

**Props = Read Only, Not Edit**
