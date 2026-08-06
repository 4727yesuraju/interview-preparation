# Switch Statement in React

## 📖 Simple English Explanation

### What is it?

A **switch statement** is a JavaScript feature used to **check multiple conditions**.

In React, it is used to **render different UI based on different values**.

### Why do we need it?

- To handle multiple conditions more clearly.
- To avoid writing many `if...else if` statements.
- To display different UI based on a value.

---

## 🌊 Flow

```text
Check Value
      ↓
Matches Case?
      ↓
Yes → Execute Matching Case
      ↓
No Match
      ↓
Execute Default Case
```

---

## ✍️ Syntax

```jsx
switch (value) {
  case "A":
    return <ComponentA />;

  case "B":
    return <ComponentB />;

  default:
    return <DefaultComponent />;
}
```

---

## 💻 Example

```jsx
function App() {
  const role = "admin";

  switch (role) {
    case "admin":
      return <h1>Admin Dashboard</h1>;

    case "user":
      return <h1>User Dashboard</h1>;

    default:
      return <h1>Guest Dashboard</h1>;
  }
}
```

**Output**

```text
Admin Dashboard
```

If:

```jsx
const role = "user";
```

**Output**

```text
User Dashboard
```

If:

```jsx
const role = "guest";
```

**Output**

```text
Guest Dashboard
```

---

## 🎤 Interview Explanation

A **switch statement** is used to check **multiple possible values** of a variable. In React, it helps render different UI based on different conditions. It is a cleaner alternative to using many `if...else if` statements when there are multiple cases.

---

## 🧠 Memory Trick

🚦 **Think of a railway track.**

```text
Value
  ↓
Switch
 ├── admin → Admin Dashboard
 ├── user → User Dashboard
 └── default → Guest Dashboard
```

**Remember:**

**One Value → Many Cases → One Matching Result**
