# Handling Multiple Inputs

## 📖 Simple English Explanation

### **What is it?**

**Handling Multiple Inputs** means **managing multiple form fields using a single state object and one event handler**.

Instead of creating separate state variables and event handlers for each input, we store all form values in one object and update the correct field based on the input's `name` attribute.

### **Why do we need it?**

- To reduce duplicate code.
- To manage large forms easily.
- To make the code cleaner and more maintainable.
- To update multiple input fields using a single function.

---

## 🌊 Flow

```text
User Types
      ↓
onChange Event
      ↓
Get Input Name & Value
      ↓
Update Matching Field in State
      ↓
UI Re-renders with Updated Data
```

---

## ✍️ Syntax

```jsx
import { useState } from "react";

function App() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
  });

  function handleChange(e) {
    setFormData({
      ...formData,
      [e.target.name]: e.target.value,
    });
  }

  return (
    <>
      <input name="name" value={formData.name} onChange={handleChange} />

      <input name="email" value={formData.email} onChange={handleChange} />
    </>
  );
}
```

---

## 💻 Example

```jsx
import { useState } from "react";

function App() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
  });

  function handleChange(e) {
    setFormData({
      ...formData,
      [e.target.name]: e.target.value,
    });
  }

  return (
    <>
      <input
        name="name"
        placeholder="Name"
        value={formData.name}
        onChange={handleChange}
      />

      <input
        name="email"
        placeholder="Email"
        value={formData.email}
        onChange={handleChange}
      />

      <h3>Name: {formData.name}</h3>
      <h3>Email: {formData.email}</h3>
    </>
  );
}
```

**Output:**

```text
Input:
Name: Yesu
Email: yesu@example.com

Display:
Name: Yesu
Email: yesu@example.com
```

---

## 🎤 Interview Explanation

**Handling Multiple Inputs** in React means managing several form fields using a **single state object** and **one `onChange` event handler**. Each input has a unique `name` attribute, and the handler updates the corresponding property in the state using computed property names (`[e.target.name]`). This approach reduces duplicate code and makes large forms easier to maintain.

---

## 🧠 Memory Trick

📝 **Think of the state object as a Registration Form.**

- 📄 Form = One state object
- ✏️ Each input = One field in the form
- 🖊️ One person (event handler) fills in the correct field.

```text
Input
   ↓
handleChange()
   ↓
Check Input Name
   ↓
Update Matching Field
```
