# Best Practices for Keys

## 📖 Simple English Explanation

### What is it?

**Keys** help React uniquely identify each item in a list.

Using the **correct key** helps React update the UI efficiently and prevents rendering bugs.

### Why do we need it?

- To help React identify each list item.
- To improve rendering performance.
- To avoid incorrect UI updates and lost component state.

---

## 🌊 Flow

```text
Render List
      ↓
Assign Unique Key
      ↓
List Changes
      ↓
React Compares Keys
      ↓
Update Only Changed Items
```

---

## ✍️ Syntax

### ✅ Best Practice

```jsx
{
  users.map((user) => <li key={user.id}>{user.name}</li>);
}
```

---

## 💻 Example

### ✅ Use a Unique ID

```jsx
const users = [
  { id: 101, name: "Yesu" },
  { id: 102, name: "Raju" },
  { id: 103, name: "Kiran" },
];

function App() {
  return (
    <ul>
      {users.map((user) => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}
```

### ❌ Avoid Using Index

```jsx
{
  users.map((user, index) => <li key={index}>{user.name}</li>);
}
```

If the list changes, React may update the wrong items.

---

## 🎤 Interview Explanation

The best practice is to use a **unique and stable key**, such as an item's **ID**, when rendering lists in React. Avoid using the array index as a key for dynamic lists because indexes can change when items are added, removed, or reordered. Using proper keys helps React efficiently update only the changed items and prevents rendering issues.

---

## 🧠 Memory Trick

🏷️ **Think of an Aadhaar Number.**

```text
Person
   ↓
Unique Aadhaar Number
   ↓
Easy to Identify
```

- **Aadhaar Number = React Key**
- **Unique ID = Best Key**

**Remember:**

**Unique ID → Best Key → Correct UI Updates**
