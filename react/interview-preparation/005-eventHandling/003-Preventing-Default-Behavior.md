# Preventing Default Behavior

## 📖 Simple English Explanation

### What is it?

**Preventing Default Behavior** means **stopping the browser's default action** by using `event.preventDefault()`.

### Why do we need it?

- To stop the browser from performing its default behavior.
- To handle the action ourselves using React.
- Commonly used with **forms** and **links**.

---

## 🌊 Flow

```text
User Performs an Action
        ↓
Browser Tries Default Action
        ↓
event.preventDefault()
        ↓
Default Action Stops
        ↓
React Handles the Action
```

---

## ✍️ Syntax

```jsx
function handleSubmit(event) {
  event.preventDefault();
}

<form onSubmit={handleSubmit}>...</form>;
```

---

## 💻 Example

### Prevent Form Submission

```jsx
function App() {
  function handleSubmit(event) {
    event.preventDefault();
    alert("Form Submitted!");
  }

  return (
    <form onSubmit={handleSubmit}>
      <button type="submit">Submit</button>
    </form>
  );
}
```

### What happens?

Without `preventDefault()`:

```text
Click Submit
      ↓
Browser Refreshes the Page
```

With `preventDefault()`:

```text
Click Submit
      ↓
Page Does NOT Refresh
      ↓
React Executes handleSubmit()
      ↓
Alert: Form Submitted!
```

---

## 🎤 Interview Explanation

`event.preventDefault()` is used to **stop the browser's default behavior**. For example, when a form is submitted, the browser normally refreshes the page. By calling `event.preventDefault()`, React prevents the page refresh and allows us to handle the form submission ourselves.

---

## 🧠 Memory Trick

🚫 **Think of a STOP sign.**

```text
Browser Default Action
        ↓
🛑 preventDefault()
        ↓
Action Stops
        ↓
React Takes Control
```

**Remember:**

**`preventDefault()` = Stop the browser's default action.**
