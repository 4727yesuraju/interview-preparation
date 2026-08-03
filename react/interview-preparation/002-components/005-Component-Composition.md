# Component Composition

## 📖 Simple English Explanation

**What is it?**

**Component Composition** means **combining small components to build a bigger component or a complete application**.

**Why do we need it?**

- To make the UI reusable and organized.
- To avoid writing the same code multiple times.
- To build large applications using small, independent components.

---

## 🌊 Flow

```text
Create Small Components
        ↓
Combine Components
        ↓
Build Bigger Component
        ↓
Build Complete Application
```

---

## ✍️ Syntax

```jsx
function App() {
  return (
    <>
      <Navbar />
      <Home />
      <Footer />
    </>
  );
}
```

---

## 💻 Example

```jsx
function Header() {
  return <h1>My Website</h1>;
}

function Footer() {
  return <footer>Copyright 2026</footer>;
}

function App() {
  return (
    <>
      <Header />
      <p>Welcome to my website!</p>
      <Footer />
    </>
  );
}
```

**Output:**

```text
My Website

Welcome to my website!

Copyright 2026
```

---

## 🎤 Interview Explanation

**Component Composition** is the process of **combining multiple small, reusable components to build a larger component or a complete application**. It helps keep the code **modular**, **reusable**, and **easy to maintain**, which is one of the core principles of React.

---

## 🧠 Memory Trick

🧩 **Think of a jigsaw puzzle.**

- 🧩 Each puzzle piece = **Component**
- 🖼️ All pieces together = **Complete Application**

**Small Components + Combine = Component Composition**
