# 📚 Promise States

## 📖 Simple English Explanation

A **Promise** has **three states** that describe its current status.

1. **Pending** ⏳ → The asynchronous operation is still running.
2. **Fulfilled (Resolved)** ✅ → The operation completed successfully.
3. **Rejected** ❌ → The operation failed.

A Promise starts in the **Pending** state and then changes to either **Fulfilled** or **Rejected**. Once it changes, its state **cannot change again**.

---

## 🤔 Why is it Needed?

- Know whether an asynchronous operation is complete.
- Handle success and errors separately.
- Make asynchronous code more predictable.

---

## 🌊 Flow

```text
Create Promise
      │
      ▼
 Pending ⏳
      │
      ├──────────────┐
      ▼              ▼
Fulfilled ✅      Rejected ❌
      │              │
      ▼              ▼
   then()         catch()
         │
         ▼
     finally()
```

---

## ✍️ Syntax

```javascript
const promise = new Promise((resolve, reject) => {
  // Async operation

  if (success) {
    resolve("Success");
  } else {
    reject("Error");
  }
});
```

---

## 💻 Example

### Example 1: Fulfilled (Resolved)

```javascript
const promise = new Promise((resolve) => {
  resolve("Data Loaded");
});

promise.then((result) => {
  console.log(result);
});
```

**Output**

```text
Data Loaded
```

---

### Example 2: Rejected

```javascript
const promise = new Promise((resolve, reject) => {
  reject("Network Error");
});

promise.catch((error) => {
  console.log(error);
});
```

**Output**

```text
Network Error
```

---

### Example 3: Pending

```javascript
const promise = new Promise((resolve) => {
  setTimeout(() => {
    resolve("Done");
  }, 2000);
});
```

**Flow**

```text
Immediately after creation
        │
        ▼
Pending ⏳

After 2 seconds
        │
        ▼
Fulfilled ✅
```

---

## 🎤 Interview Answer (30 Seconds)

A Promise has three states: **Pending**, **Fulfilled (Resolved)**, and **Rejected**. It starts in the Pending state while the asynchronous operation is running. If the operation succeeds, it becomes Fulfilled; if it fails, it becomes Rejected. Once a Promise is fulfilled or rejected, its state cannot change again.

---

## 🧠 Memory Trick

```text
Promise

⏳ Pending
     │
     ├── ✅ Success
     │      │
     │      ▼
     │    Fulfilled
     │
     └── ❌ Failure
            │
            ▼
         Rejected
```

Easy Rule:

> **Pending → Fulfilled OR Rejected (Only Once)**

---

## ⭐ Keywords

- Promise
- Pending
- Fulfilled
- Resolved
- Rejected
- then()
- catch()
- finally()
- Asynchronous

```

```
