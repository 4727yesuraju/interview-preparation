# 📚 What is `async/await`?

## 📖 Simple English Explanation

`async/await` is a modern JavaScript feature used to **handle asynchronous operations in a synchronous-looking way**.

- **`async`** makes a function return a Promise.
- **`await`** pauses the execution of that function until the Promise is resolved or rejected.

It makes asynchronous code **cleaner and easier to read** than Promise chaining.

---

## 🤔 Why is it Needed?

- Makes asynchronous code easier to understand.
- Avoids long `.then()` chains.
- Improves code readability and maintenance.
- Commonly used with API calls, file reading, and database operations.

---

## 🌊 Flow

```text
Call async Function
        │
        ▼
Async Task Starts
        │
        ▼
await Promise
        │
(Promise Pending)
        │
        ▼
Promise Resolved
        │
        ▼
Continue Remaining Code
```

---

## ✍️ Syntax

```javascript
async function functionName() {
  const result = await promise;
  return result;
}
```

---

## 💻 Example

### Example 1: Basic `async/await`

```javascript
function getData() {
  return Promise.resolve("Hello");
}

async function fetchData() {
  const result = await getData();
  console.log(result);
}

fetchData();
```

**Output**

```text
Hello
```

---

### Example 2: Using `fetch()`

```javascript
async function getUsers() {
  const response = await fetch("https://jsonplaceholder.typicode.com/users");
  const users = await response.json();

  console.log(users);
}

getUsers();
```

---

### Example 3: Error Handling

```javascript
async function fetchData() {
  try {
    const result = await Promise.reject("Something went wrong");
    console.log(result);
  } catch (error) {
    console.log(error);
  }
}

fetchData();
```

**Output**

```text
Something went wrong
```

---

## 🎤 Interview Answer (30 Seconds)

`async/await` is a modern way to work with Promises in JavaScript. The `async` keyword makes a function return a Promise, and the `await` keyword pauses the execution of that function until the Promise settles. It makes asynchronous code look like synchronous code, making it easier to read and maintain. Errors are usually handled using `try...catch`.

---

## 🧠 Memory Trick

```text
async
  │
  ▼
Returns Promise

await
  │
  ▼
Wait for Promise

Continue Execution
```

Easy Rule:

> **`async` = Creates a Promise**

> **`await` = Waits for the Promise**

---

## ⭐ Keywords

- async
- await
- Promise
- Asynchronous
- try...catch
- fetch()
- Readable Code
- Modern JavaScript
