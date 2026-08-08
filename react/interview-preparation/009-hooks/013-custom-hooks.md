# Custom Hooks

## 📖 Simple English Explanation

### **What is it?**

A **Custom Hook** is a JavaScript function that lets us **reuse React logic** between multiple components.

A Custom Hook usually starts with the word **`use`**, such as `useFetch`, `useAuth`, or `useForm`.

It can use built-in React Hooks like `useState`, `useEffect`, and `useRef`.

### **Why do we need it?**

- To reuse the same logic in multiple components.
- To avoid writing duplicate code.
- To keep components clean and simple.
- To separate **logic** from **UI**.
- To make code easier to maintain and test.

> ⚠️ A Custom Hook shares **logic**, not the actual state between components. Each component calling the Custom Hook gets its own state.

---

## 🌊 Flow

```text
Component A
     ↓
Calls Custom Hook
     ↓
Custom Hook
     ↓
Contains Reusable Logic
     ↓
Returns Data / Functions
     ↓
Component A Uses Them
```

The same Custom Hook can be reused:

```text
Component A ──┐
              ↓
         Custom Hook
              ↑
Component B ──┘
```

Each component gets its **own state**.

---

## ✍️ Syntax

```jsx
function useCustomHook() {
  // React Hooks
  // Reusable logic

  return value;
}
```

Use it inside a component:

```jsx
const value = useCustomHook();
```

---

## 💻 Example

### Without Custom Hook

Suppose two components need to fetch users.

We might write the same `useState` and `useEffect` logic in both components:

```jsx
function Users() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    fetch("/api/users")
      .then((res) => res.json())
      .then((data) => setUsers(data));
  }, []);

  return <div>...</div>;
}
```

Another component may need the same logic:

```jsx
function AdminUsers() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    fetch("/api/users")
      .then((res) => res.json())
      .then((data) => setUsers(data));
  }, []);

  return <div>...</div>;
}
```

This creates **duplicate logic**.

---

### With Custom Hook

Create a reusable Hook:

```jsx
import { useEffect, useState } from "react";

function useUsers() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    fetch("/api/users")
      .then((res) => res.json())
      .then((data) => setUsers(data));
  }, []);

  return users;
}
```

Now use it in multiple components:

```jsx
function Users() {
  const users = useUsers();

  return (
    <div>
      {users.map((user) => (
        <p key={user.id}>{user.name}</p>
      ))}
    </div>
  );
}
```

Another component can reuse the same logic:

```jsx
function AdminUsers() {
  const users = useUsers();

  return (
    <div>
      {users.map((user) => (
        <p key={user.id}>{user.name}</p>
      ))}
    </div>
  );
}
```

### Flow

```text
Users Component
      ↓
  useUsers()
      ↓
Fetch Users
      ↓
Return Users
      ↓
Display Users
```

```text
AdminUsers Component
      ↓
  useUsers()
      ↓
Fetch Users
      ↓
Return Users
      ↓
Display Users
```

The **fetching logic is reused**, while each component controls its own usage.

---

## 🧠 Important Rule — Hooks Rules Apply

Custom Hooks must follow the **Rules of Hooks**.

### ✅ Correct

```jsx
function useCounter() {
  const [count, setCount] = useState(0);

  return {
    count,
    setCount,
  };
}
```

### ❌ Wrong

```jsx
function useCounter() {
  if (someCondition) {
    const [count, setCount] = useState(0);
  }
}
```

Hooks should not be called inside:

- `if` statements
- `for` loops
- Nested functions
- Conditions

---

## 🆚 Custom Hook vs Normal Function

| Feature                | Custom Hook | Normal Function |
| ---------------------- | ----------- | --------------- |
| Starts with `use`      | ✅          | Not required    |
| Can use React Hooks    | ✅          | ❌              |
| Reuses React logic     | ✅          | Usually ❌      |
| Can use `useState`     | ✅          | ❌              |
| Can use `useEffect`    | ✅          | ❌              |
| Used inside components | ✅          | Depends         |

Example:

```jsx
function calculateTotal(price, quantity) {
  return price * quantity;
}
```

This is a **normal function**.

```jsx
function useUser() {
  const [user, setUser] = useState(null);

  return user;
}
```

This is a **Custom Hook**.

---

## 🎤 Interview Answer (30 Seconds)

A Custom Hook is a reusable JavaScript function that allows us to share React logic between multiple components. Custom Hooks usually start with `use` and can use other React Hooks such as `useState`, `useEffect`, and `useRef`. They help avoid duplicate logic and keep components clean. Each component that calls a Custom Hook gets its own state and Hook lifecycle.

---

## 🧠 Memory Trick

Think of a **Custom Hook as a Logic Box** 📦.

```text
Custom Hook
     ↓
Reusable React Logic 📦
     ↓
     ├── Component A
     ├── Component B
     └── Component C
```

👉 **Custom Hook = Reuse React Logic**
