# 📚 Types of Components (Functional vs Class)

## 📖 Simple English Explanation

React has **two types of components**: **Functional Components** and **Class Components**. Today, **Functional Components** are the recommended way because they are **simpler** and support **Hooks** like `useState` and `useEffect`. **Class Components** are the older way of writing React components and are mostly found in older projects.

---

## 🤔 Why is it Needed?

- To create reusable UI components.
- Functional Components are easier to write and maintain.
- Class Components were used before Hooks were introduced.
- Today, most new React applications use Functional Components.

---

## 🌊 Flow

```text
Need a Component
        ↓
Choose Functional Component ✅ (Recommended)
        ↓
OR
        ↓
Choose Class Component (Older Approach)
        ↓
Render UI
```

---

## ✍️ Syntax

### Functional Component

```jsx
function Welcome() {
  return <h1>Hello React!</h1>;
}
```

### Class Component

```jsx
import React, { Component } from "react";

class Welcome extends Component {
  render() {
    return <h1>Hello React!</h1>;
  }
}
```

---

## 💻 Example

### Functional Component

```jsx
function Button() {
  return <button>Click Me</button>;
}
```

### Class Component

```jsx
class Button extends React.Component {
  render() {
    return <button>Click Me</button>;
  }
}
```

---

## 🎤 Interview Answer (30 Seconds)

React has **Functional Components** and **Class Components**. Functional Components are simple JavaScript functions that return JSX and support **Hooks** like `useState` and `useEffect`. Class Components are ES6 classes that extend `React.Component` and use lifecycle methods. Today, **Functional Components are preferred** because they are simpler, cleaner, and easier to maintain.

---

## 🧠 Memory Trick

👨‍💻 **Think of old phones vs smartphones.**

- 📱 **Functional Component** = Modern smartphone (recommended)
- ☎️ **Class Component** = Old phone (still works, but rarely used)

**Interview Tip:** Always say **"Functional Components are the standard in modern React."**

---

## ⭐ Keywords

- Functional Component
- Class Component
- Hooks
- JSX
- React.Component
- Lifecycle Methods
- Modern React
- Reusable Components

---

## 📌 Quick Comparison

| Functional Component                 | Class Component                                    |
| ------------------------------------ | -------------------------------------------------- |
| JavaScript function                  | ES6 class                                          |
| Simple and concise                   | More code                                          |
| Uses Hooks (`useState`, `useEffect`) | Uses lifecycle methods (`componentDidMount`, etc.) |
| Recommended for new projects ✅      | Mostly used in legacy projects                     |
| Easier to read and maintain          | Harder to maintain                                 |
