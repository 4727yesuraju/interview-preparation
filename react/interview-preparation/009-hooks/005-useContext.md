# useContext

## 📖 Simple English Explanation

### **What is it?**

`useContext` is a **React Hook** that allows a component to **access shared data from a Context** without passing props through every intermediate component.

It helps different components share the same data easily.

### **Why do we need it?**

- To avoid **Prop Drilling**.
- To share common data across multiple components.
- To make the code cleaner and easier to maintain.
- To provide global data like user information, theme, or language.

---

## 🌊 Flow

```text
Create Context
      ↓
Provide Value using Context.Provider
      ↓
Child Component
      ↓
useContext()
      ↓
Access Shared Data
```

---

## ✍️ Syntax

```jsx
import { createContext, useContext } from "react";

const UserContext = createContext();

function Child() {
  const user = useContext(UserContext);

  return <h2>{user}</h2>;
}

function App() {
  return (
    <UserContext.Provider value="Yesu">
      <Child />
    </UserContext.Provider>
  );
}
```

---

## 💻 Example

```jsx
import { createContext, useContext } from "react";

const ThemeContext = createContext();

function Header() {
  const theme = useContext(ThemeContext);

  return <h2>Theme: {theme}</h2>;
}

function App() {
  return (
    <ThemeContext.Provider value="Dark">
      <Header />
    </ThemeContext.Provider>
  );
}
```

**Output:**

```text
Theme: Dark
```

---

## 🎤 Interview Explanation

`useContext` is a React Hook used to **consume data from a Context**. It allows components to access shared data directly without passing props through multiple levels of components, a problem known as **Prop Drilling**. It is commonly used for global data such as authenticated users, themes, language preferences, and application settings.

---

## 🧠 Memory Trick

📢 **Think of Context as a Loudspeaker.**

- 📢 Context = Loudspeaker
- 👨‍👩‍👧‍👦 Components = People in a building
- Everyone can hear the same announcement without someone passing the message room by room.

```text
Context
   ↓
Provider
   ↓
useContext()
   ↓
All Required Components Get Data
```
