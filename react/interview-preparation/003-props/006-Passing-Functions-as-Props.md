# Passing Functions as Props

## 📖 Simple English Explanation

### What is it?

**Passing Functions as Props** means a **parent component sends a function to a child component through props**.

The child component can **call that function** whenever needed (for example, when a button is clicked).

### Why do we need it?

- To allow a **child component to communicate with its parent**.
- To let the **parent control and update its own state**.
- This follows React's **one-way data flow**.

---

## 🌊 Flow

```text
Parent Creates Function
        ↓
Pass Function as Prop
        ↓
Child Receives Function
        ↓
Child Calls Function
        ↓
Parent Function Executes
```

---

## ✍️ Syntax

### Parent Component

```jsx
function Parent() {
  function handleClick() {
    console.log("Button Clicked!");
  }

  return <Child onClick={handleClick} />;
}
```

### Child Component

```jsx
function Child({ onClick }) {
  return <button onClick={onClick}>Click Me</button>;
}
```

---

## 💻 Example

```jsx
function Child({ greet }) {
  return <button onClick={greet}>Say Hello</button>;
}

function App() {
  function sayHello() {
    alert("Hello!");
  }

  return <Child greet={sayHello} />;
}
```

### What happens?

1. Parent creates `sayHello()`.
2. Parent passes it to `Child` as the `greet` prop.
3. User clicks the button.
4. Child calls `greet()`.
5. Parent's `sayHello()` function runs.

---

## 🎤 Interview Explanation

Passing functions as props means a **parent component passes a function to a child component through props**. The child can call that function whenever an event occurs, such as a button click. This is the standard React pattern for allowing a **child component to trigger actions in the parent** while maintaining **one-way data flow**.

---

## 🧠 Memory Trick

📞 **Think of giving someone your phone number.**

- 👨 Parent gives **phone number (function)**.
- 👶 Child receives the phone number.
- 📲 Child calls the number when needed.
- 👨 Parent answers and performs the action.

```text
Parent
   │
 Gives Function 📞
   ↓
Child
   │
Calls Function
   ↓
Parent Executes
```

**Remember:**

- **Data → Props**
- **Action → Function as Prop**
