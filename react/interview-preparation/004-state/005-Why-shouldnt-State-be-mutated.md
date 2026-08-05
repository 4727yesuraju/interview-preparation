# Why shouldn't State be mutated?

## 📖 Simple English Explanation

### What is it?

**Mutating state** means **changing the state value directly** instead of using the state update function (`setState` or `setCount`).

### Why do we need to avoid it?

- React **doesn't know** that the state has changed.
- The UI may **not update**.
- It can cause **unexpected bugs**.
- Always use the state updater function to update state safely.

---

## 🌊 Flow

```text
State
   ↓
Update using setState / setCount
   ↓
React Detects Change
   ↓
Component Re-renders
   ↓
UI Updates
```

❌ Wrong Flow

```text
State
   ↓
Change State Directly
   ↓
React Doesn't Detect Change
   ↓
No Re-render
   ↓
UI Doesn't Update
```

---

## ✍️ Syntax

### ❌ Wrong

```jsx
count = count + 1;
```

### ✅ Correct

```jsx
setCount(count + 1);
```

---

## 💻 Example

### ❌ Wrong

```jsx
function Counter() {
  const [count, setCount] = useState(0);

  function increase() {
    count = count + 1; // Don't do this
  }

  return <button>{count}</button>;
}
```

**Result**

```text
React doesn't know the state changed.
UI does not update.
```

---

### ✅ Correct

```jsx
function Counter() {
  const [count, setCount] = useState(0);

  function increase() {
    setCount(count + 1);
  }

  return <button onClick={increase}>{count}</button>;
}
```

**Result**

```text
React knows the state changed.
UI updates automatically.
```

---

## 🎤 Interview Explanation

State should **not be mutated directly** because React **cannot detect direct changes** to the state variable. Instead, we should use the state updater function like `setState` or `setCount`. This tells React that the state has changed, so it re-renders the component and updates the UI correctly.

---

## 🧠 Memory Trick

🚦 **Think of a traffic signal.**

- ❌ Change the light yourself → Nobody knows.
- ✅ Press the control button → System knows and changes the light.

```text
Direct Change
      ↓
React Doesn't Know ❌

Use setCount()
      ↓
React Knows ✅
      ↓
UI Updates
```

**Remember:**

**Never mutate State. Always use `setState()` or `setCount()`.**
