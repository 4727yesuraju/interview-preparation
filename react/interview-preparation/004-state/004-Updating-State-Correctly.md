# Updating State Correctly

## 📖 Simple English Explanation

### What is it?

**Updating State Correctly** means **always using the state update function** (like `setCount`) instead of changing the state variable directly.

### Why do we need it?

- To let React know that the state has changed.
- To automatically update the UI.
- Directly changing the state variable does **not** update the UI.

---

## 🌊 Flow

```text
State Value
      ↓
Call setState / setCount
      ↓
React Updates State
      ↓
Component Re-renders
      ↓
UI Updates
```

---

## ✍️ Syntax

```jsx
const [count, setCount] = useState(0);

// Correct
setCount(count + 1);
```

❌ Don't do this:

```jsx
count = count + 1;
```

---

## 💻 Example

### ❌ Wrong Way

```jsx
function Counter() {
  const [count, setCount] = useState(0);

  function increase() {
    count = count + 1; // ❌ Wrong
  }

  return <button>{count}</button>;
}
```

**Result:**

```text
State changes?
❌ No

UI updates?
❌ No
```

---

### ✅ Correct Way

```jsx
function Counter() {
  const [count, setCount] = useState(0);

  function increase() {
    setCount(count + 1);
  }

  return <button onClick={increase}>{count}</button>;
}
```

**Result:**

```text
State changes?
✅ Yes

UI updates?
✅ Yes
```

---

## 🎤 Interview Explanation

In React, we should **never update state directly**. Instead, we use the **state updater function** like `setCount` or `setState`. This tells React that the state has changed, so React re-renders the component and updates the UI. Directly changing the state variable does not trigger a re-render.

---

## 🧠 Memory Trick

🚪 **Think of a smart door.**

- ❌ Push the wall → Door doesn't open.
- ✅ Press the doorbell → Door opens.

```text
Change Variable Directly
        ↓
React Doesn't Know ❌

Use setCount()
        ↓
React Knows
        ↓
UI Updates ✅
```

**Remember:**

- ❌ `count = count + 1`
- ✅ `setCount(count + 1)`
