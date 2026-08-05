# Synthetic Events

## 📖 Simple English Explanation

### What is it?

A **Synthetic Event** is **React's wrapper around the browser's native event**.

Instead of using browser events directly, React creates a **Synthetic Event** so that events work the **same way in all browsers**.

### Why do we need it?

- To provide the same event behavior across different browsers.
- To make event handling easier and more consistent.
- Developers don't need to worry about browser differences.

---

## 🌊 Flow

```text
User Clicks Button
        ↓
Browser Creates Native Event
        ↓
React Wraps It as a Synthetic Event
        ↓
Event Handler Executes
```

---

## ✍️ Syntax

```jsx
function App() {
  function handleClick(event) {
    console.log(event.type);
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

---

## 💻 Example

```jsx
function App() {
  function handleClick(event) {
    alert(event.type);
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

**Output**

```text
Click Me
    ↓
Alert: click
```

Here, `event` is a **Synthetic Event**, not the browser's native event.

---

## 🎤 Interview Explanation

A **Synthetic Event** is React's **cross-browser wrapper** around the browser's native event. It provides a **consistent API** for handling events across all browsers. When an event occurs, React creates a Synthetic Event and passes it to the event handler, making event handling simpler and more reliable.

---

## 🧠 Memory Trick

🌍 **Think of a translator.**

```text
Different Browsers
        ↓
React (Translator)
        ↓
Synthetic Event
        ↓
Your Event Handler
```

**Remember:**

**Browser Event → React Wrapper → Synthetic Event**
