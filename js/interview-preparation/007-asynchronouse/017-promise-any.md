# 📚 What is `Promise.any()`?

## 📖 Simple English Explanation

`Promise.any()` is a Promise method used to **run multiple Promises in parallel**.

- It returns the **first fulfilled (resolved) Promise**.
- It **ignores rejected Promises**.
- It **fails only if all Promises are rejected**.

---

## 🤔 Why is it Needed?

- Get the first successful result.
- Ignore failed requests if another request succeeds.
- Useful when you have multiple backup APIs or servers.

---

## 🌊 Flow

```text
Promise 1 ──┐
            │
Promise 2 ──┼──► Promise.any()
            │
Promise 3 ──┘
            │
            ▼
First Promise Resolved?
            │
     ┌──────┴──────┐
     ▼             ▼
Yes ✅         No (Rejected)
     │             │
     ▼             ▼
Return Result   Keep Waiting
                     │
                     ▼
          All Rejected?
                │
           ┌────┴────┐
           ▼         ▼
         Yes ❌     No
           │
           ▼
AggregateError
```

---

## ✍️ Syntax

```javascript
Promise.any([promise1, promise2, promise3])
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

---

## 💻 Example

### Example 1: First Successful Promise

```javascript
const p1 = Promise.reject("Server 1 Failed");
const p2 = Promise.resolve("Server 2 Success");
const p3 = Promise.resolve("Server 3 Success");

Promise.any([p1, p2, p3]).then((result) => {
  console.log(result);
});
```

**Output**

```text
Server 2 Success
```

---

### Example 2: All Promises Rejected

```javascript
const p1 = Promise.reject("Error 1");
const p2 = Promise.reject("Error 2");

Promise.any([p1, p2]).catch((error) => {
  console.log(error);
});
```

**Output**

```text
AggregateError
```

> `Promise.any()` rejects with an **AggregateError** because **all Promises failed**.

---

### Example 3: Using `async/await`

```javascript
async function getFastestSuccess() {
  try {
    const result = await Promise.any([
      Promise.reject("API 1 Failed"),
      Promise.resolve("API 2 Success"),
      Promise.resolve("API 3 Success"),
    ]);

    console.log(result);
  } catch (error) {
    console.log(error);
  }
}

getFastestSuccess();
```

**Output**

```text
API 2 Success
```

---

## 🎤 Interview Answer (30 Seconds)

`Promise.any()` runs multiple Promises in parallel and returns the first Promise that is fulfilled. It ignores rejected Promises and continues waiting for a successful one. If all Promises are rejected, it rejects with an `AggregateError`.

---

## 🧠 Memory Trick

```text
Promise 1 ❌
Promise 2 ❌
Promise 3 ✅
      │
      ▼
Promise.any()

First Success Wins 🎉
```

Easy Rule:

> **`Promise.any()` = First Success Wins**

---

## ⭐ Keywords

- Promise.any()
- Parallel Execution
- First Fulfilled
- Ignore Rejections
- AggregateError
- Promise
- Asynchronous
