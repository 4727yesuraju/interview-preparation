# When to Create a Custom Hook

## 📖 Simple English Explanation

### **When should we create a Custom Hook?**

We should create a Custom Hook when **the same React logic is needed in multiple components**.

The main purpose is to **reuse logic**, not to share state.

For example, if multiple components need the same:

- API fetching logic
- Form handling logic
- Authentication logic
- Window resize logic
- Local storage logic
- Timer logic
- Event listener logic

we can extract that logic into a Custom Hook.

### Simple Rule

```text
Same React Logic
      ↓
Used in Multiple Components?
      ↓
     Yes
      ↓
Create Custom Hook
```

---

## 🌊 Flow

```text
Component A
     ↓
Uses Some React Logic
     ↓
Component B
     ↓
Uses Same React Logic
     ↓
Duplicate Code ❌
     ↓
Extract Logic
     ↓
Custom Hook
     ↓
Both Components Reuse It ✅
```

---

## 💻 Example

Suppose multiple components need to track the browser window width.

### ❌ Without Custom Hook

```jsx
function ComponentA() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => {
      setWidth(window.innerWidth);
    };

    window.addEventListener("resize", handleResize);

    return () => {
      window.removeEventListener("resize", handleResize);
    };
  }, []);

  return <h2>{width}px</h2>;
}
```

Another component needs the same logic:

```jsx
function ComponentB() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => {
      setWidth(window.innerWidth);
    };

    window.addEventListener("resize", handleResize);

    return () => {
      window.removeEventListener("resize", handleResize);
    };
  }, []);

  return <p>{width}px</p>;
}
```

Now we have **duplicate logic**.

---

### ✅ With Custom Hook

Create:

```jsx
function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => {
      setWidth(window.innerWidth);
    };

    window.addEventListener("resize", handleResize);

    return () => {
      window.removeEventListener("resize", handleResize);
    };
  }, []);

  return width;
}
```

Now both components can reuse it:

```jsx
function ComponentA() {
  const width = useWindowWidth();

  return <h2>{width}px</h2>;
}
```

```jsx
function ComponentB() {
  const width = useWindowWidth();

  return <p>{width}px</p>;
}
```

### Result

```text
Component A ──┐
              ↓
       useWindowWidth()
              ↑
Component B ──┘

        ↓

Same Logic ✅
Different Component State ✅
```

---

## ⚠️ Don't Create a Custom Hook for Everything

Not every piece of code needs a Custom Hook.

### ❌ Don't create one when:

```text
Simple calculation
      ↓
Normal function is enough
```

Example:

```jsx
function calculateTotal(price, quantity) {
  return price * quantity;
}
```

There is no need for:

```jsx
function useCalculateTotal() {
  // unnecessary
}
```

### ✅ Create one when:

```text
Reusable React Logic
        ↓
Uses Hooks / React lifecycle
        ↓
Needed by Multiple Components
        ↓
Custom Hook
```

---

## 🆚 Custom Hook vs Normal Function

| Situation                      | Use             |
| ------------------------------ | --------------- |
| Simple calculation             | Normal Function |
| String formatting              | Normal Function |
| Array manipulation             | Normal Function |
| Reusable `useState` logic      | Custom Hook     |
| Reusable `useEffect` logic     | Custom Hook     |
| Reusable React lifecycle logic | Custom Hook     |
| API fetching logic             | Custom Hook     |
| Event listener logic           | Custom Hook     |

### Easy Rule

> **If it is just JavaScript logic → Normal Function.**

> **If it is reusable React logic → Custom Hook.**

---

## 🎤 Interview Answer (30 Seconds)

We should create a Custom Hook when we have **reusable React logic that is needed by multiple components**. For example, API fetching, form handling, event listeners, timers, or window resize logic. Custom Hooks help us avoid duplicate code and keep components clean. They share the **logic**, but each component gets its **own state and lifecycle**.

---

## 🧠 Memory Trick

Remember:

```text
Duplicate React Logic
        ↓
Extract Logic
        ↓
Custom Hook
        ↓
Reuse Logic
```

👉 **Custom Hook = Reusable React Logic**

And remember:

```text
Custom Hook
     ↓
Shares Logic ❌ State
     ↓
Each Component
     ↓
Own State
```
