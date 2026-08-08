# useLayoutEffect

## 📖 Simple English Explanation

### **What is it?**

`useLayoutEffect` is a React Hook used to run code **after React updates the DOM but before the browser paints the screen**.

It is similar to `useEffect`, but it runs **synchronously before the browser displays the updated UI**.

It is mainly useful when we need to **measure or modify the DOM before the user sees the screen**.

### **Why do we need it?**

- To measure DOM elements before the browser paints.
- To adjust the DOM before the user sees it.
- To prevent visual flickering.
- Useful for layout-related calculations.

> ⚠️ Prefer `useEffect` for most side effects. Use `useLayoutEffect` only when the work needs to happen before the browser paints.

---

## 🌊 Flow

```text
Component Renders
       ↓
React Updates DOM
       ↓
useLayoutEffect Runs
       ↓
Browser Paints Screen
       ↓
User Sees Updated UI
```

### Difference from `useEffect`

```text
useLayoutEffect:

Render
  ↓
DOM Update
  ↓
useLayoutEffect
  ↓
Browser Paint
  ↓
User sees UI
```

```text
useEffect:

Render
  ↓
DOM Update
  ↓
Browser Paint
  ↓
useEffect
  ↓
User sees updated effect
```

---

## ✍️ Syntax

```jsx
import { useLayoutEffect } from "react";

useLayoutEffect(() => {
  // Code runs before browser paint

  return () => {
    // Cleanup
  };
}, [dependencies]);
```

---

## 💻 Example

```jsx
import { useLayoutEffect, useRef, useState } from "react";

function App() {
  const boxRef = useRef(null);
  const [width, setWidth] = useState(0);

  useLayoutEffect(() => {
    const boxWidth = boxRef.current.getBoundingClientRect().width;

    setWidth(boxWidth);
  }, []);

  return (
    <>
      <div ref={boxRef}>Hello React</div>

      <h2>Width: {width}px</h2>
    </>
  );
}
```

### What happens?

```text
Component Renders
       ↓
<div> is created in DOM
       ↓
useLayoutEffect runs
       ↓
Measure div width
       ↓
setWidth()
       ↓
React updates UI
       ↓
Browser Paints
       ↓
User sees final UI
```

The important point is that `useLayoutEffect` allows React to perform the measurement **before the browser paints**, helping avoid visible layout changes.

---

## 🆚 useEffect vs useLayoutEffect

| Feature                    | useEffect | useLayoutEffect |
| -------------------------- | --------- | --------------- |
| Runs after DOM update      | ✅        | ✅              |
| Runs before browser paint  | ❌        | ✅              |
| Runs after browser paint   | Usually   | ❌              |
| DOM measurement            | Possible  | Better choice   |
| Can prevent visual flicker | ❌        | ✅              |
| Should be default choice   | ✅        | ❌              |

### Easy Rule

```text
Normal side effect?
       ↓
   useEffect

Need DOM measurement
or visual update before paint?
       ↓
useLayoutEffect
```

---

## 🎤 Interview Answer (30 Seconds)

`useLayoutEffect` is a React Hook that runs **synchronously after React updates the DOM but before the browser paints the screen**. It is mainly used for DOM measurements, positioning, or changes that must happen before the user sees the updated UI. Unlike `useEffect`, it can prevent visual flickering, but it should be used carefully because long-running code can block the browser from painting.

---

## 🧠 Memory Trick

Think of `useLayoutEffect` as a **final inspection before showing the UI** 🔍.

```text
React Updates DOM
       ↓
🔍 Check / Measure / Adjust
       ↓
Browser Paint
       ↓
👀 User Sees UI
```

👉 **useLayoutEffect = Do layout work before the screen is painted**
