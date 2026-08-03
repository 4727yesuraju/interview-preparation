# What is a Functional Component?

## 📖 Simple English Explanation

**What is it?**

A **Functional Component** is a **JavaScript function** that returns **JSX** to display the UI.

**Why do we need it?**

- To create reusable UI components.
- It is simple, easy to read, and easy to maintain.
- It supports **Hooks** like `useState` and `useEffect`.
- It is the **recommended way** to write components in modern React.

---

## 🌊 Flow

```text
Create a Function
      ↓
Return JSX
      ↓
React Renders the UI
      ↓
User Sees the Component
```

---

## ✍️ Syntax

```jsx
function Welcome() {
  return <h1>Hello React!</h1>;
}

export default Welcome;
```

---

## 💻 Example

```jsx
function Greeting() {
  return <h2>Welcome to React!</h2>;
}

function App() {
  return <Greeting />;
}
```

**Output:**

```text
Welcome to React!
```

---

## 🎤 Interview Explanation

A **Functional Component** is a **JavaScript function** that returns **JSX** to create the user interface. It is the modern and recommended way to write React components because it is simple, reusable, and supports **Hooks** like `useState` and `useEffect`.

---

## 🧠 Memory Trick

📝 **Function + JSX = Functional Component**

Think of it like a **machine**:

- Input → Props
- Process → Function
- Output → JSX (UI)

**Function → JSX → UI**
