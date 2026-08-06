# Why shouldn't Index be used as Key?

## 📖 Simple English Explanation

### What is it?

In React, every item in a list needs a **key**. Some developers use the **array index** (`0`, `1`, `2`, ...) as the key.

This is **not recommended** because the index can change when items are **added, removed, or reordered**.

### Why do we need to avoid it?

- React may identify the wrong item.
- The UI may update incorrectly.
- Input values or component state may be lost.
- Using a unique ID gives better performance and correct updates.

---

## 🌊 Flow

### ❌ Using Index as Key

```text
Before
0 → Apple
1 → Mango
2 → Orange
        ↓
Remove Apple
        ↓
0 → Mango
1 → Orange
        ↓
Indexes Change
        ↓
React Gets Confused
        ↓
Wrong UI Updates
```

### ✅ Using Unique ID as Key

```text
Before
101 → Apple
102 → Mango
103 → Orange
        ↓
Remove Apple
        ↓
102 → Mango
103 → Orange
        ↓
IDs Stay the Same
        ↓
React Correctly Identifies Items
        ↓
Correct UI Updates
```

---

## ✍️ Syntax

### ❌ Wrong

```jsx
{
  users.map((user, index) => <li key={index}>{user.name}</li>);
}
```

### ✅ Correct

```jsx
{
  users.map((user) => <li key={user.id}>{user.name}</li>);
}
```

---

## 💻 Example

### ❌ Using Index

```jsx
const fruits = ["Apple", "Mango", "Orange"];

{
  fruits.map((fruit, index) => <li key={index}>{fruit}</li>);
}
```

If **Apple** is removed:

```text
Before

0 → Apple
1 → Mango
2 → Orange

After

0 → Mango
1 → Orange
```

React may think:

```text
Apple became Mango ❌
Mango became Orange ❌
```

This can cause incorrect UI updates.

---

### ✅ Using Unique ID

```jsx
const fruits = [
  { id: 1, name: "Apple" },
  { id: 2, name: "Mango" },
  { id: 3, name: "Orange" },
];

{
  fruits.map((fruit) => <li key={fruit.id}>{fruit.name}</li>);
}
```

Now, even if **Apple** is removed:

```text
2 → Mango
3 → Orange
```

The IDs stay the same, so React updates the UI correctly.

---

## 🎤 Interview Explanation

Using the **array index as a key** is not recommended because indexes change when list items are added, removed, or reordered. React may incorrectly identify list items, causing wrong UI updates or lost component state. A **unique and stable ID** is the best choice because it allows React to correctly track each item.

---

## 🧠 Memory Trick

🏷️ **Think of roll numbers in a classroom.**

```text
Student Leaves
      ↓
Seat Numbers Change ❌
Roll Numbers Stay Same ✅
```

- **Seat Number = Array Index**
- **Roll Number = Unique ID**

**Remember:**

**Use Roll Number (ID), not Seat Number (Index).**
