# 📚 What is `Promise.race()`?

## 📖 Simple English Explanation

`Promise.race()` is a Promise method used to **run multiple Promises in parallel**.

It returns the result of the **first Promise that settles**, whether it is:

- ✅ Fulfilled (Resolved)
- ❌ Rejected

It **does not wait** for the remaining Promises.

---

## 🤔 Why is it Needed?

- Get the fastest response.
- Set request timeouts.
- Run multiple tasks and use whichever finishes first.

---

## 🌊 Flow

```text
Promise 1 ──┐
            │
Promise 2 ──┼──► Promise.race()
            │
Promise 3 ──┘
            │
            ▼
 First Promise Finishes
            │
     ┌──────┴──────┐
     ▼             ▼
Resolved ✅     Rejected ❌
```

---

## ✍️ Syntax

```javascript
Promise.race([promise1, promise2, promise3])
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

---

## 💻 Example

### Example 1: Fastest Promise Wins

```javascript
const p1 = new Promise((resolve) => setTimeout(() => resolve("HTML"), 3000));

const p2 = new Promise((resolve) => setTimeout(() => resolve("CSS"), 1000));

const p3 = new Promise((resolve) =>
  setTimeout(() => resolve("JavaScript"), 2000),
);

Promise.race([p1, p2, p3]).then((result) => console.log(result));
```

**Output**

```text
CSS
```

---

### Example 2: First Promise Rejects

```javascript
const p1 = new Promise((resolve, reject) =>
  setTimeout(() => reject("Network Error"), 1000),
);

const p2 = new Promise((resolve) => setTimeout(() => resolve("Success"), 2000));

Promise.race([p1, p2]).catch((error) => console.log(error));
```

**Output**

```text
Network Error
```

---

### Example 3: Using `async/await`

```javascript
async function getFastest() {
  const result = await Promise.race([
    Promise.resolve("User"),
    Promise.resolve("Orders"),
  ]);

  console.log(result);
}

getFastest();
```

**Output**

```text
User
```

---

## 🎤 Interview Answer (30 Seconds)

`Promise.race()` runs multiple Promises in parallel and returns the result of the first Promise that settles, whether it is fulfilled or rejected. It does not wait for the remaining Promises to complete, making it useful for timeouts and selecting the fastest response.

---

## 🧠 Memory Trick

```text
Promise 1 🏃
Promise 2 🏃
Promise 3 🏃
      │
      ▼
Promise.race()

🏆 First to Finish Wins
```

Easy Rule:

> **`Promise.race()` = First Promise Wins**

---

## ⭐ Keywords

- Promise.race()
- Parallel Execution
- First Result
- Fastest Promise
- Resolved
- Rejected
- Asynchronous
