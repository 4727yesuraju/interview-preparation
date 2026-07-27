# 📚 What is `Promise.all()`?

## 📖 Simple English Explanation

`Promise.all()` is a Promise method used to **run multiple Promises in parallel**.

- It waits until **all Promises are successfully resolved**.
- If **any one Promise is rejected**, `Promise.all()` immediately rejects with that error.

---

## 🤔 Why is it Needed?

- Run multiple asynchronous tasks at the same time.
- Improve performance by executing tasks in parallel.
- Wait until all required data is available.

---

## 🌊 Flow

```text
Promise 1 ──┐
            │
Promise 2 ──┼──► Promise.all()
            │
Promise 3 ──┘
            │
            ▼
 All Resolved?
      │
  ┌───┴────┐
  ▼        ▼
Yes ✅    No ❌
  │         │
  ▼         ▼
Array     Error
```

---

## ✍️ Syntax

```javascript
Promise.all([promise1, promise2, promise3])
  .then((results) => {
    console.log(results);
  })
  .catch((error) => {
    console.log(error);
  });
```

---

## 💻 Example

### Example 1: All Promises Succeed

```javascript
const p1 = Promise.resolve("HTML");
const p2 = Promise.resolve("CSS");
const p3 = Promise.resolve("JavaScript");

Promise.all([p1, p2, p3]).then((result) => {
  console.log(result);
});
```

**Output**

```text
["HTML", "CSS", "JavaScript"]
```

---

### Example 2: One Promise Fails

```javascript
const p1 = Promise.resolve("HTML");
const p2 = Promise.reject("Network Error");
const p3 = Promise.resolve("JavaScript");

Promise.all([p1, p2, p3]).catch((error) => {
  console.log(error);
});
```

**Output**

```text
Network Error
```

---

### Example 3: Using `async/await`

```javascript
async function loadData() {
  const result = await Promise.all([
    Promise.resolve("User"),
    Promise.resolve("Orders"),
    Promise.resolve("Products"),
  ]);

  console.log(result);
}

loadData();
```

**Output**

```text
["User", "Orders", "Products"]
```

---

## 🎤 Interview Answer (30 Seconds)

`Promise.all()` is used to execute multiple Promises in parallel. It waits until all Promises are fulfilled and then returns an array of their results in the same order. If any Promise is rejected, `Promise.all()` immediately rejects with that error.

---

## 🧠 Memory Trick

```text
Promise 1
Promise 2
Promise 3
     │
     ▼
Promise.all()

All Success ✅
     │
     ▼
Array of Results

One Failure ❌
     │
     ▼
Error
```

Easy Rule:

> **`Promise.all()` = All must succeed.**

---

## ⭐ Keywords

- Promise.all()
- Parallel Execution
- Promise
- Array of Results
- Resolved
- Rejected
- Asynchronous
