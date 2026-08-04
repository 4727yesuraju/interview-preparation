# Passing Data Between Components

## 📖 Simple English Explanation

### What is it?

**Passing Data Between Components** means **sending data from one component to another**.

In React, data is usually passed:

- **Parent → Child** using **Props** ✅
- **Child → Parent** using a **Function (Callback)** passed through Props ✅

This helps components communicate with each other.

### Why do we need it?

- To share data between components.
- To make components reusable.
- To keep data organized.
- To allow components to communicate.

---

## 🌊 Flow

### Parent → Child

```text
Parent Component
        ↓
Pass Data (Props)
        ↓
Child Component
        ↓
Display Data
```

### Child → Parent

```text
Parent Component
        ↓
Pass Function (Callback)
        ↓
Child Calls Function
        ↓
Parent Receives Data
```

---

## ✍️ Syntax

### Parent → Child

```jsx
<Child name="Yesu" />
```

```jsx
function Child(props) {
  return <h1>{props.name}</h1>;
}
```

---

### Child → Parent

```jsx
<Child sendData={handleData} />
```

```jsx
props.sendData("Hello Parent");
```

---

## 💻 Example

### Parent → Child (Using Props)

```jsx
function Child({ name }) {
  return <h2>Hello {name}</h2>;
}

function App() {
  return <Child name="Yesu" />;
}
```

**Output**

```text
Hello Yesu
```

---

### Child → Parent (Using Callback)

```jsx
function Child({ sendMessage }) {
  return <button onClick={() => sendMessage("Hello Parent")}>Send</button>;
}

function App() {
  function handleMessage(message) {
    alert(message);
  }

  return <Child sendMessage={handleMessage} />;
}
```

**What happens?**

1. Parent passes `handleMessage` to Child.
2. Child clicks the button.
3. Child calls `sendMessage("Hello Parent")`.
4. Parent receives `"Hello Parent"`.

---

## 🎤 Interview Explanation

React components communicate by passing data between them. A **Parent Component** sends data to a **Child Component** using **Props**. If a **Child Component** wants to send data back, the parent passes a **callback function** as a prop, and the child calls that function with the required data. This follows React's **one-way data flow**.

---

## 🧠 Memory Trick

📦 **Think of a family.**

**Parent → Child**

🎁 Parent gives a gift (**Props**) to the child.

```text
Parent
   ↓
 Props
   ↓
Child
```

**Child → Parent**

📞 Child cannot directly give data to the parent.

Instead, the parent gives the child a **phone number (callback function)**.

The child calls that number to send the message.

```text
Parent gives Phone Number
           ↓
Child Calls Parent
           ↓
Parent Gets Message
```

**Remember:**

- **Props = Parent → Child**
- **Callback Function = Child → Parent**
