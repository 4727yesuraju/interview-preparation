# 📚 What are Components?

## 📖 Simple English Explanation

A **Component** is a **small, reusable piece of UI** in React. Each component has its own **HTML (JSX), CSS, and JavaScript logic**. We combine multiple components to build a complete application. This makes the code **clean, reusable, and easy to maintain**.

> **Examples:** Navbar, Button, Header, Footer, Product Card, Login Form.

---

## 🤔 Why is it Needed?

- To break a large UI into small, manageable pieces.
- To reuse the same UI in multiple places.
- To make code easier to read, maintain, and test.
- Without components, the entire UI would be written in one file, making it difficult to manage.

---

## 🌊 Flow

```text
Build Small Components
          ↓
Reuse Components
          ↓
Combine Components
          ↓
Create Complete Application
```

---

## ✍️ Syntax

```jsx
function Header() {
  return <h1>Welcome</h1>;
}

export default Header;
```

---

## 💻 Example

```jsx
function Navbar() {
  return <nav>Navbar</nav>;
}

function Footer() {
  return <footer>Footer</footer>;
}

function App() {
  return (
    <>
      <Navbar />
      <h1>Home Page</h1>
      <Footer />
    </>
  );
}
```

**Output:**

```text
Navbar
Home Page
Footer
```

---

## 🎤 Interview Answer (30 Seconds)

A **Component** is a **reusable building block** in React used to create the user interface. Each component contains its own **JSX, logic, and styling**, and can be reused throughout the application. React follows a **component-based architecture**, making applications easier to develop, maintain, and scale.

---

## 🧠 Memory Trick

🧱 **Think of building a house with LEGO blocks.**

- 🧱 One LEGO block = One **Component**
- 🏠 Many LEGO blocks = Complete **Application**

**React = Build UI with reusable LEGO blocks.**

---

## ⭐ Keywords

- Component
- Reusable UI
- Component-Based Architecture
- JSX
- Reusability
- Maintainability
- Building Blocks
- React
