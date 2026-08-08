# useId

## 📖 Simple English Explanation

### **What is it?**

`useId` is a React Hook used to generate a **unique ID** for a component.

It is mainly useful for connecting **form elements with their labels** and for accessibility.

The generated ID is stable across re-renders and is designed to work correctly with **Server-Side Rendering (SSR)** and hydration.

### **Why do we need it?**

- To generate unique IDs for HTML elements.
- To connect `<label>` with `<input>`.
- To improve accessibility.
- To avoid manually creating IDs that might conflict.
- Works correctly with SSR and hydration.

> ⚠️ `useId` should **not** be used to generate IDs for list keys. Use your data's unique ID for `key`.

---

## 🌊 Flow

```text
Component Renders
       ↓
useId() Generates Unique ID
       ↓
React Keeps ID Stable
       ↓
Use ID in HTML Elements
       ↓
Label ↔ Input Connected
```

---

## ✍️ Syntax

```jsx
import { useId } from "react";

const id = useId();
```

Use it:

```jsx
<label htmlFor={id}>
  Email
</label>

<input id={id} />
```

---

## 💻 Example

```jsx
import { useId } from "react";

function SignupForm() {
  const emailId = useId();

  return (
    <div>
      <label htmlFor={emailId}>Email</label>

      <input id={emailId} type="email" />
    </div>
  );
}

export default SignupForm;
```

### What happens?

```text
SignupForm Renders
       ↓
useId() generates unique ID
       ↓
Example:
:Riql:
       ↓
<label htmlFor=":Riql:">
       ↓
<input id=":Riql:">
       ↓
Label and Input are connected
```

When the user clicks the **Email** label, the corresponding input can receive focus.

---

## 💻 Example — Multiple Fields

```jsx
import { useId } from "react";

function SignupForm() {
  const id = useId();

  return (
    <form>
      <label htmlFor={`${id}-name`}>Name</label>

      <input id={`${id}-name`} />

      <label htmlFor={`${id}-email`}>Email</label>

      <input id={`${id}-email`} />
    </form>
  );
}
```

Here, `useId()` gives us a unique base ID.

We can create related IDs from it:

```text
id
 ↓
 ├── id-name
 └── id-email
```

---

## 🆚 useId vs useRef

| Feature                       | useId | useRef |
| ----------------------------- | ----- | ------ |
| Generates unique ID           | ✅    | ❌     |
| Stores mutable value          | ❌    | ✅     |
| Access DOM element            | ❌    | ✅     |
| Persists between renders      | ✅    | ✅     |
| Mainly used for accessibility | ✅    | ❌     |
| Used for form element IDs     | ✅    | ❌     |

---

## ⚠️ Important: Don't Use `useId` for Keys

❌ Wrong:

```jsx
const id = useId();

items.map((item) => <div key={id}>{item.name}</div>);
```

For list keys, use a unique ID from your data:

✅ Correct:

```jsx
items.map((item) => <div key={item.id}>{item.name}</div>);
```

### Why?

`key` is used by React to identify list items, while `useId` is designed mainly for **accessibility and unique HTML IDs**.

---

## 🎤 Interview Answer (30 Seconds)

`useId` is a React Hook used to generate unique and stable IDs for HTML elements. It is mainly useful for accessibility, such as connecting labels with form inputs. The generated IDs are designed to work correctly with Server-Side Rendering and hydration. It should not be used for list keys because React keys should come from the application's data.

---

## 🧠 Memory Trick

Think of **`useId` as an ID Generator** 🪪.

```text
Component
    ↓
  useId()
    ↓
Unique ID 🪪
    ↓
HTML Elements
    ↓
Connect Related Elements
```

👉 **useId = Generate a unique ID**
