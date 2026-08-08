# useMemo

## 📖 Simple English Explanation

### **What is it?**

`useMemo` is a **React Hook** used to **memoize (cache) the result of a calculation**.

React remembers the calculated value and **reuses it** until one of its dependencies changes.

### **Why do we need it?**

- To avoid expensive calculations on every render.
- To improve performance when calculations are costly.
- To reuse a previously calculated value when the dependencies have not changed.

> ⚠️ `useMemo` should be used for **performance optimization**, not for making code work correctly.

---

## 🌊 Flow

```text
Component Renders
        ↓
useMemo Checks Dependencies
        ↓
Dependencies Changed?
    ↓            ↓
   No            Yes
    ↓             ↓
Use Cached      Run Calculation
Value           Again
    ↓             ↓
    └──────→ Return Value
```

---

## ✍️ Syntax

```jsx
import { useMemo } from "react";

const result = useMemo(() => {
  return expensiveCalculation(data);
}, [data]);
```

---

## 💻 Example

```jsx
import { useMemo, useState } from "react";

function App() {
  const [count, setCount] = useState(0);
  const [number, setNumber] = useState(10);

  const doubledNumber = useMemo(() => {
    console.log("Calculating...");

    return number * 2;
  }, [number]);

  return (
    <>
      <h2>Count: {count}</h2>
      <h2>Doubled: {doubledNumber}</h2>

      <button onClick={() => setCount(count + 1)}>Increase Count</button>

      <button onClick={() => setNumber(number + 1)}>Increase Number</button>
    </>
  );
}
```

**Output:**

```text
Initial:
Count: 0
Doubled: 20

Click "Increase Count":
Count: 1
Doubled: 20

Calculation does NOT run again.

Click "Increase Number":
Count: 1
Doubled: 22

Calculation runs again because
number changed.
```

---

## 🎤 Interview Explanation

`useMemo` is a React Hook used to **cache the result of an expensive calculation** between renders. React recalculates the value only when one of the specified dependencies changes. This can improve performance by avoiding unnecessary calculations, but it should be used only when there is a real performance benefit.

---

## 🧠 Memory Trick

🧠 **Think of `useMemo` as a Calculator with Memory.**

```text
First Calculation
       ↓
Save Result 🧠
       ↓
Render Again
       ↓
Same Dependencies?
   ↓           ↓
  Yes          No
   ↓            ↓
Use Saved     Calculate
Result        Again
```

👉 **useMemo = Remember the calculated value**
