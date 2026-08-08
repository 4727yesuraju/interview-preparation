# useCallback

## 📖 Simple English Explanation

### **What is it?**

`useCallback` is a **React Hook** used to **memoize (cache) a function**.

React remembers the function and returns the **same function reference** until one of its dependencies changes.

### **Why do we need it?**

- To avoid creating a new function on every render.
- To improve performance in some cases.
- Especially useful when passing functions to **memoized child components**.
- Helps prevent unnecessary child re-renders caused by a changed function reference.

---

## 🌊 Flow

```text
Component Renders
        ↓
useCallback Checks Dependencies
        ↓
Dependencies Changed?
    ↓            ↓
   No            Yes
    ↓             ↓
Use Same       Create New
Function       Function
    ↓             ↓
    └──────→ Return Function
```
