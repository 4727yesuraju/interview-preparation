# What are Props?

## 📖 Simple English Explanation

**What is it?**

**Props (Properties)** are used to **pass data from a parent component to a child component**. They make components reusable by allowing the same component to display different data.

**Why do we need it?**

- To send data from one component to another.
- To make components reusable.
- To avoid creating multiple similar components with different hardcoded values.

---

## 🌊 Flow

```text
Parent Component
        ↓
Pass Data using Props
        ↓
Child Component Receives Props
        ↓
Display the Data
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

---

## 💻 Example

```jsx
function Student(props) {
  return <h2>Name: {props.name}</h2>;
}

function App() {
  return (
    <>
      <Student name="Raju" />
      <Student name="Kiran" />
      <Student name="Anil" />
    </>
  );
}
```

**Output:**

```text
Name: Raju
Name: Kiran
Name: Anil
```

---

## 🎤 Interview Explanation

**Props (Properties)** are used to **pass data from a parent component to a child component** in React. They make components **reusable** because the same component can display different data. Props are **read-only**, which means a child component cannot modify the props it receives.

---

## 🧠 Memory Trick

📦 **Think of Props as a gift box.**

- 👨 Parent = Sends the gift 🎁
- 👶 Child = Receives the gift 🎁

**Parent → Props → Child**

👉 **Props = Pass Data Down**
