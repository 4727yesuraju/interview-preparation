# Form Validation

## 📖 Simple English Explanation

### **What is it?**

**Form Validation** is the process of **checking whether the user's input is correct and valid before submitting the form**.

For example, we can check if:

- A required field is not empty.
- An email has the correct format.
- A password has the required length.

### **Why do we need it?**

- To prevent invalid data from being submitted.
- To improve user experience.
- To reduce errors.
- To ensure the application receives correct data.

---

## 🌊 Flow

```text
User Fills Form
       ↓
Clicks Submit
       ↓
Validate Input
       ↓
Valid?
   ↓        ↓
 Yes       No
  ↓         ↓
Submit    Show Error
Form      Message
```

---

## ✍️ Syntax

```jsx
import { useState } from "react";

function App() {
  const [email, setEmail] = useState("");

  function handleSubmit(e) {
    e.preventDefault();

    if (email === "") {
      alert("Email is required");
      return;
    }

    alert("Form Submitted");
  }

  return (
    <form onSubmit={handleSubmit}>
      <input value={email} onChange={(e) => setEmail(e.target.value)} />

      <button type="submit">Submit</button>
    </form>
  );
}
```

---

## 💻 Example

```jsx
import { useState } from "react";

function App() {
  const [password, setPassword] = useState("");

  function handleSubmit(e) {
    e.preventDefault();

    if (password.length < 6) {
      alert("Password must be at least 6 characters");
      return;
    }

    alert("Form Submitted Successfully");
  }

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="password"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
        placeholder="Enter Password"
      />

      <button type="submit">Submit</button>
    </form>
  );
}
```

**Output:**

```text
Input: 123

Alert:
Password must be at least 6 characters
```

```text
Input: 123456

Alert:
Form Submitted Successfully
```

---

## 🎤 Interview Explanation

**Form Validation** is the process of checking user input before submitting a form. It ensures that the entered data is correct, complete, and follows the required rules, such as required fields, valid email format, or minimum password length. In React, validation is commonly implemented using **Controlled Components** with `useState`, allowing errors to be displayed immediately and preventing invalid data from being submitted.

---

## 🧠 Memory Trick

🛂 **Think of Form Validation as a Security Check.**

- 👤 User = Passenger
- 🛂 Validation = Security Officer
- ✈️ Form Submission = Boarding the Flight

```text
User Input
     ↓
Validation
     ↓
Valid?
 ↓       ↓
Yes      No
 ↓        ↓
Submit   Show Error
```
