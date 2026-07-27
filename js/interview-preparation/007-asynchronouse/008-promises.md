# 📚 What are Promises?

## 📖 Simple English Explanation

A **Promise** is a JavaScript object that represents the **result of an asynchronous operation**.

It acts like a **placeholder for a future value**.

The operation may:

- ✅ Complete successfully (**Resolved**)
- ❌ Fail (**Rejected**)
- ⏳ Still be running (**Pending**)

---

## 🤔 Why is it Needed?

- Handle asynchronous operations.
- Avoid Callback Hell.
- Write cleaner and more readable code.
- Commonly used for API calls, file reading, and database operations.

---

## 🌊 Flow

```text
Start Async Task
        │
        ▼
      Promise
        │
        ▼
 ┌───────────────┐
 │               │
 ▼               ▼
Resolved      Rejected
 │               │
 ▼               ▼
then()       catch()
        │
        ▼
    finally()
```

---

## ✍️ Syntax

### Creating a Promise

```javascript
const promise = new Promise((resolve, reject) => {
  // Async operation

  if (success) {
    resolve(result);
  } else {
    reject(error);
  }
});
```

### Using a Promise

```javascript
promise
  .then((result) => {
    // Success
  })
  .catch((error) => {
    // Error
  })
  .finally(() => {
    // Always runs
  });
```

---

## 💻 Example

### Example 1: Promise Resolved

```javascript
const promise = new Promise((resolve, reject) => {
  resolve("Success");
});

promise.then((result) => {
  console.log(result);
});
```

**Output**

```text
Success
```

---

### Example 2: Promise Rejected

```javascript
const promise = new Promise((resolve, reject) => {
  reject("Something went wrong");
});

promise.catch((error) => {
  console.log(error);
});
```

**Output**

```text
Something went wrong
```

---

### Example 3: Using `then()`, `catch()`, and `finally()`

```javascript
const promise = new Promise((resolve) => {
  resolve("Data Loaded");
});

promise
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  })
  .finally(() => {
    console.log("Finished");
  });
```

**Output**

```text
Data Loaded
Finished
```

---

## 🎤 Interview Answer (30 Seconds)

A Promise is a JavaScript object that represents the eventual result of an asynchronous operation. It has three states: **Pending**, **Resolved (Fulfilled)**, and **Rejected**. We use `.then()` to handle success, `.catch()` to handle errors, and `.finally()` to execute code regardless of the result. Promises help avoid callback hell and make asynchronous code easier to read.

---

## 🧠 Memory Trick

```text
Promise
   │
   ▼
Pending ⏳
   │
   ├── Success ✅
   │      │
   │      ▼
   │    then()
   │
   └── Failure ❌
          │
          ▼
       catch()

        ▼
     finally()
```

Easy Rule:

> **Promise = A future result of an asynchronous operation.**

---

## ⭐ Keywords

- Promise
- Asynchronous
- Pending
- Resolved (Fulfilled)
- Rejected
- then()
- catch()
- finally()
- Callback Hell

```

```
