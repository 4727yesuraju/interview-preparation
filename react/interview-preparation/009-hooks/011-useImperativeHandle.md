# useImperativeHandle

## 📖 Simple English Explanation

### **What is it?**

`useImperativeHandle` is a React Hook used to **customize what a parent component can access through a ref**.

Normally, a ref gives the parent access to a DOM element or child component's ref.

With `useImperativeHandle`, the child can decide **which methods or values should be exposed to the parent**.

It is commonly used with `forwardRef` when the parent needs to trigger a specific action inside the child.

### **Why do we need it?**

- To expose specific functions from a child component.
- To control what the parent can access through a ref.
- To hide the child's internal implementation.
- Useful for actions like `focus()`, `reset()`, `open()`, or `close()`.

> ⚠️ `useImperativeHandle` should be used carefully. React generally prefers communication through **props** and **state**.

---

## 🌊 Flow

```text
Parent Component
       ↓
Creates Ref
       ↓
Passes Ref to Child
       ↓
Child uses useImperativeHandle
       ↓
Child exposes specific methods
       ↓
Parent calls ref.current.method()
       ↓
Child performs the action
```

---

## ✍️ Syntax

```jsx
useImperativeHandle(ref, () => {
  return {
    method1() {
      // logic
    },

    method2() {
      // logic
    },
  };
}, [dependencies]);
```

---

## 💻 Example

```jsx
import { forwardRef, useImperativeHandle, useRef } from "react";

const Input = forwardRef((props, ref) => {
  const inputRef = useRef(null);

  useImperativeHandle(ref, () => ({
    focus() {
      inputRef.current.focus();
    },

    clear() {
      inputRef.current.value = "";
    },
  }));

  return <input ref={inputRef} />;
});

function App() {
  const inputRef = useRef(null);

  return (
    <>
      <Input ref={inputRef} />

      <button onClick={() => inputRef.current.focus()}>Focus</button>

      <button onClick={() => inputRef.current.clear()}>Clear</button>
    </>
  );
}
```

### What happens?

```text
App
 ↓
Creates inputRef
 ↓
Passes ref to Input
 ↓
Input receives ref
 ↓
useImperativeHandle exposes:
    ├── focus()
    └── clear()
 ↓
Parent can call:
    inputRef.current.focus()
    inputRef.current.clear()
```

The parent **cannot directly access the child's internal `inputRef`**.

The child controls what is exposed:

```text
Child Internal Implementation
        ↓
    inputRef
        ↓
useImperativeHandle
        ↓
Expose Only:
    ├── focus()
    └── clear()
        ↓
Parent
```

---

## 🆚 useRef vs useImperativeHandle

| Feature                     | useRef    | useImperativeHandle |
| --------------------------- | --------- | ------------------- |
| Creates a ref               | ✅        | ❌                  |
| Stores mutable value        | ✅        | ❌                  |
| Access DOM element          | ✅        | Indirectly          |
| Controls exposed methods    | ❌        | ✅                  |
| Used with parent-child refs | Sometimes | Commonly            |
| Customizes `ref.current`    | ❌        | ✅                  |

### Easy Rule

```text
Need to store/access a ref?
        ↓
      useRef

Need to control what
a child exposes through ref?
        ↓
useImperativeHandle
```

---

## 🎤 Interview Answer (30 Seconds)

`useImperativeHandle` is a React Hook used to **customize the value exposed through a ref**. It is commonly used with `forwardRef` when a parent component needs to call specific methods on a child component. For example, a child can expose methods like `focus()`, `clear()`, or `reset()` while keeping its internal implementation private.

---

## 🧠 Memory Trick

Think of `useImperativeHandle` as a **Remote Control** 🎮.

```text
Child
 ├── Internal Logic
 ├── Internal State
 └── Internal DOM
        ↓
useImperativeHandle
        ↓
🎮 Remote Control
        ↓
Parent can use:
 ├── focus()
 ├── clear()
 └── reset()
```

👉 **useImperativeHandle = Decide what the parent can control**
