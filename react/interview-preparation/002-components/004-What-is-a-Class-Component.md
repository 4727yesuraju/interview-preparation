# What is a Class Component?

## 📖 Simple English Explanation

**What is it?**

A **Class Component** is an **ES6 class** that extends `React.Component` and returns JSX using a `render()` method.

**Why do we need it?**

- Before **Hooks** were introduced, Class Components were used to manage **state** and **lifecycle methods**.
- Today, they are mostly found in **older (legacy) React projects**.
- In modern React, **Functional Components** are preferred because they are simpler and support Hooks.

---

## 🌊 Flow

```text
Create a Class
      ↓
Extend React.Component
      ↓
Write render() Method
      ↓
Return JSX
      ↓
React Renders the UI
```

---

## ✍️ Syntax

```jsx
import React, { Component } from "react";

class Welcome extends Component {
  render() {
    return <h1>Hello React!</h1>;
  }
}

export default Welcome;
```

---

## 💻 Example

```jsx
import React, { Component } from "react";

class Greeting extends Component {
  render() {
    return <h2>Welcome to React!</h2>;
  }
}

export default Greeting;
```

**Output:**

```text
Welcome to React!
```

---

## 🎤 Interview Explanation

A **Class Component** is a JavaScript class (introduced in ES6) that extends `React.Component` and returns JSX from its `render()` method.. Before Hooks, it was used to manage **state** and **lifecycle methods**. Today, Class Components are mainly used in **legacy React applications**, while **Functional Components** are the recommended approach.

---

## 🧠 Memory Trick

🏫 **Think of two generations of React components.**

- 👴 **Class Component** = Old generation (legacy)
- 👨‍💻 **Functional Component** = New generation (modern)

**Class = Old | Functional = New**
