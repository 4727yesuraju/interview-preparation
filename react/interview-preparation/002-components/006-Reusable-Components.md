# Reusable Components

## 📖 Simple English Explanation

**What is it?**

A **Reusable Component** is a component that can be **used multiple times** in different parts of an application.

**Why do we need it?**

- To avoid writing the same code again and again.
- To make the code easier to maintain.
- To save development time.
- If a change is needed, update the component once and it updates everywhere it is used.

---

## 🌊 Flow

```text
Create Component Once
        ↓
Reuse It Multiple Times
        ↓
Pass Different Data (Props)
        ↓
Display Different Results
```

---

## ✍️ Syntax

```jsx
function Button({ text }) {
  return <button>{text}</button>;
}
```

---

## 💻 Example

```jsx
function Button({ text }) {
  return <button>{text}</button>;
}

function App() {
  return (
    <>
      <Button text="Login" />
      <Button text="Register" />
      <Button text="Logout" />
    </>
  );
}
```

**Output:**

```text
[Login]

[Register]

[Logout]
```

---

## 🎤 Interview Explanation

A **Reusable Component** is a React component that can be used multiple times in different places. Instead of creating similar UI elements repeatedly, we create the component once and pass different data using **props**. This reduces code duplication and makes applications easier to maintain.

---

## 🧠 Memory Trick

🧱 **Think of a brick mold.**

- Create one mold 🧱
- Produce many bricks 🧱🧱🧱

**One Component → Many Uses**

👉 **Reusable Component = Create Once, Use Many Times**
