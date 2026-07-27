# 📚 Promises vs Async/Await

## 📖 Simple English Explanation

Both **Promises** and **`async/await`** are used to handle **asynchronous operations** in JavaScript.

- **Promises** use `.then()`, `.catch()`, and `.finally()` to handle results.
- **`async/await`** is built on top of Promises and makes asynchronous code look like synchronous code.

Both achieve the same result, but `async/await` is usually easier to read and write.

---

## 🤔 Why is it Needed?

- Handle asynchronous tasks like API calls, file reading, and database queries.
- Avoid blocking the main thread.
- Write clean and maintainable asynchronous code.

---

## 🌊 Flow

### Promise

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
catch()
```

### Async/Await

```text
async Function
      │
      ▼
await Promise
      │
      ▼
Next Line
      │
      ▼
try...catch
```

---

## ✍️ Syntax

### Promise

```javascript
getData()
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });
```

### Async/Await

```javascript
async function fetchData() {
  try {
    const data = await getData();
    console.log(data);
  } catch (error) {
    console.log(error);
  }
}
```

---

## 💻 Example

### Using Promise

```javascript
function getData() {
  return Promise.resolve("Hello");
}

getData()
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });
```

**Output**

```text
Hello
```

---

### Using Async/Await

```javascript
function getData() {
  return Promise.resolve("Hello");
}

async function fetchData() {
  try {
    const data = await getData();
    console.log(data);
  } catch (error) {
    console.log(error);
  }
}

fetchData();
```

**Output**

```text
Hello
```

---

## 🎤 Interview Answer (30 Seconds)

Both Promises and `async/await` are used to handle asynchronous operations. Promises use `.then()` and `.catch()` to process results, while `async/await` provides a cleaner and more readable syntax by allowing asynchronous code to look like synchronous code. Internally, `async/await` is built on top of Promises.

---

## 🧠 Memory Trick

```text
Promise
   │
   ▼
then()
catch()

async/await
   │
   ▼
await
try...catch
```

Easy Rule:

> **Promise = `.then()` Chain**

> **Async/Await = `await` + `try...catch`**

---

## ⭐ Keywords

- Promise
- async
- await
- then()
- catch()
- try...catch
- Asynchronous
- Readability
