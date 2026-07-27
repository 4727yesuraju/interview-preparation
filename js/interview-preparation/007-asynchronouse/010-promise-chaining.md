# 📚 Promise Chaining

## 📖 Simple English Explanation

**Promise Chaining** means **connecting multiple `.then()` methods together**.

The result returned from one `.then()` is automatically passed to the next `.then()`.

This allows you to perform multiple asynchronous operations in sequence without creating nested callbacks.

---

## 🤔 Why is it Needed?

- Avoid Callback Hell.
- Execute asynchronous tasks one after another.
- Make code clean, readable, and maintainable.

---

## 🌊 Flow

```text
Promise
   │
   ▼
then()
   │
   ▼
then()
   │
   ▼
then()
   │
   ▼
catch()
   │
   ▼
finally()
```

---

## ✍️ Syntax

```javascript
promise
  .then((result) => {
    return newResult;
  })
  .then((newResult) => {
    return anotherResult;
  })
  .then((anotherResult) => {
    console.log(anotherResult);
  })
  .catch((error) => {
    console.log(error);
  })
  .finally(() => {
    console.log("Finished");
  });
```

---

## 💻 Example

### Example 1: Basic Promise Chaining

```javascript
Promise.resolve(5)
  .then((num) => {
    return num * 2;
  })
  .then((num) => {
    return num + 10;
  })
  .then((result) => {
    console.log(result);
  });
```

**Output**

```text
20
```

---

### Example 2: Real-World Flow

```javascript
loginUser()
  .then(getUserProfile)
  .then(getUserOrders)
  .then((orders) => {
    console.log(orders);
  })
  .catch((error) => {
    console.log(error);
  });
```

**Flow**

```text
Login
  │
  ▼
Get Profile
  │
  ▼
Get Orders
  │
  ▼
Display Orders
```

---

## 🎤 Interview Answer (30 Seconds)

Promise chaining is the process of connecting multiple `.then()` methods together. Each `.then()` receives the value returned by the previous one, allowing asynchronous tasks to execute sequentially. If an error occurs in any step, it is handled by a single `.catch()`, making the code cleaner and avoiding callback hell.

---

## 🧠 Memory Trick

```text
Promise
   │
   ▼
then()
   │
   ▼
then()
   │
   ▼
then()
```

Easy Rule:

> **One `.then()` passes its result to the next `.then()`.**

---

## ⭐ Keywords

- Promise Chaining
- then()
- catch()
- finally()
- Sequential Execution
- Return Value
- Callback Hell
- Asynchronous

```

```
