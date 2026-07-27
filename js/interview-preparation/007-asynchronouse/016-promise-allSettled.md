# 📚 What is `Promise.allSettled()`?

## 📖 Simple English Explanation

`Promise.allSettled()` is a Promise method used to **run multiple Promises in parallel**.

- It **waits for all Promises to finish**, whether they are:
  - ✅ Fulfilled (Resolved)
  - ❌ Rejected
- It **never fails because one Promise is rejected**.
- It returns the **status and result of every Promise**.

---

## 🤔 Why is it Needed?

- Get the result of every Promise.
- Continue even if some Promises fail.
- Useful when all task results are important.

---

## 🌊 Flow

```text
Promise 1 ──┐
            │
Promise 2 ──┼──► Promise.allSettled()
            │
Promise 3 ──┘
            │
            ▼
Wait for ALL Promises
            │
            ▼
Return Results
            │
            ▼
[
  Fulfilled ✅,
  Rejected ❌,
  Fulfilled ✅
]
```

---

## ✍️ Syntax

```javascript
Promise.allSettled([promise1, promise2, promise3]).then((results) => {
  console.log(results);
});
```

---

## 💻 Example

### Example 1: Mixed Results

```javascript
const p1 = Promise.resolve("HTML");
const p2 = Promise.reject("Network Error");
const p3 = Promise.resolve("JavaScript");

Promise.allSettled([p1, p2, p3]).then((results) => {
  console.log(results);
});
```

**Output**

```text
[
  { status: "fulfilled", value: "HTML" },
  { status: "rejected", reason: "Network Error" },
  { status: "fulfilled", value: "JavaScript" }
]
```

---

### Example 2: Using `async/await`

```javascript
async function loadData() {
  const results = await Promise.allSettled([
    Promise.resolve("User"),
    Promise.reject("Orders Failed"),
    Promise.resolve("Products"),
  ]);

  console.log(results);
}

loadData();
```

**Output**

```text
[
  { status: "fulfilled", value: "User" },
  { status: "rejected", reason: "Orders Failed" },
  { status: "fulfilled", value: "Products" }
]
```

---

## 🎤 Interview Answer (30 Seconds)

`Promise.allSettled()` runs multiple Promises in parallel and waits until all of them finish, regardless of whether they are fulfilled or rejected. It returns an array of objects containing the status and result of each Promise. Unlike `Promise.all()`, it does not stop if one Promise fails.

---

## 🧠 Memory Trick

```text
Promise 1
Promise 2
Promise 3
     │
     ▼
Promise.allSettled()

Wait for Everyone
      │
      ▼
✅ Success
❌ Failure
✅ Success

Return All Results
```

Easy Rule:

> **`Promise.allSettled()` = Wait for Everyone**

---

## ⭐ Keywords

- Promise.allSettled()
- Parallel Execution
- Wait for All
- Fulfilled
- Rejected
- Status
- Result
- Asynchronous
