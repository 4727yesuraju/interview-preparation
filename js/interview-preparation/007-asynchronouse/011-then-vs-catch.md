# 📚 `then()` vs `catch()`

## 📖 Simple English Explanation

Both `then()` and `catch()` are Promise methods used to handle the result of an asynchronous operation.

- **`then()`** → Executes when the Promise is **fulfilled (resolved successfully)**.
- **`catch()`** → Executes when the Promise is **rejected (an error occurs)**.

---

## 🤔 Why is it Needed?

- **`then()`** → Handle successful results.
- **`catch()`** → Handle errors without crashing the application.

---

## 🌊 Flow

```text
Promise
   │
   ▼
Pending
   │
   ├──────────────┐
   ▼              ▼
Resolved ✅    Rejected ❌
   │              │
   ▼              ▼
then()        catch()
```

---

## ✍️ Syntax

### `then()`

```javascript
promise.then((result) => {
  console.log(result);
});
```

### `catch()`

```javascript
promise.catch((error) => {
  console.log(error);
});
```

---

## 💻 Example

### Example 1: `then()`

```javascript
const promise = Promise.resolve("Data Loaded");

promise.then((result) => {
  console.log(result);
});
```

**Output**

```text
Data Loaded
```

---

### Example 2: `catch()`

```javascript
const promise = Promise.reject("Network Error");

promise.catch((error) => {
  console.log(error);
});
```

**Output**

```text
Network Error
```

---

### Example 3: Using Both

```javascript
const promise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Success");
  } else {
    reject("Failed");
  }
});

promise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

**Output**

```text
Success
```

---

## 🎤 Interview Answer (30 Seconds)

`then()` is used to handle the successful result of a fulfilled Promise, while `catch()` is used to handle errors from a rejected Promise. In a Promise chain, `.catch()` can handle errors from any previous `.then()`, making error handling simple and clean.

---

## 🧠 Memory Trick

```text
Promise
   │
   ├── ✅ Success
   │      │
   │      ▼
   │    then()
   │
   └── ❌ Error
          │
          ▼
       catch()
```

Easy Rule:

> **`then()` = Success**

> **`catch()` = Error**

---

## ⭐ Keywords

- Promise
- then()
- catch()
- Resolved
- Fulfilled
- Rejected
- Error Handling
- Asynchronous
