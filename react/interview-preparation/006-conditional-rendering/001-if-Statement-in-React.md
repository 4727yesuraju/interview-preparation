# if Statement in React

## 📖 Simple English Explanation

### What is it?

An **if statement** is a JavaScript feature used to **check a condition** and execute code only if the condition is `true`.

In React, we use `if` statements to **conditionally render (show or hide) UI**.

### Why do we need it?

- To display different UI based on a condition.
- To show or hide components.
- To render different content depending on data or user actions.

---

## 🌊 Flow

```text
Check Condition
      ↓
Is it True?
   ↓        ↓
 Yes        No
 ↓          ↓
Show UI   Show Other UI / Nothing
```

---

## ✍️ Syntax

```jsx
if (condition) {
  // code
}
```

---

## 💻 Example

```jsx
function App() {
  const isLoggedIn = true;

  if (isLoggedIn) {
    return <h1>Welcome!</h1>;
  }

  return <h1>Please Login</h1>;
}
```

**Output**

```text
Welcome!
```

If:

```jsx
const isLoggedIn = false;
```

Output:

```text
Please Login
```

---

## 🎤 Interview Explanation

The **if statement** is used in React to **conditionally render UI**. It checks whether a condition is `true` or `false`. If the condition is `true`, one UI is rendered; otherwise, a different UI (or nothing) is rendered. It is commonly used for authentication, loading screens, and error messages.

---

## 🧠 Memory Trick

🚦 **Think of a traffic signal.**

```text
Condition
    ↓
Green? → Go
Red?   → Stop
```

**Remember:**

**Condition True → Show UI**

**Condition False → Show Other UI**
