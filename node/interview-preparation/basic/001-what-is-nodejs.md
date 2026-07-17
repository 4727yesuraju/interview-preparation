# 📚 What is Node.js?

## 📖 Simple English Explanation

Node.js is an **open-source JavaScript runtime environment** that allows you to run JavaScript outside the browser. It is built on Google's **V8 JavaScript Engine**. Node.js is mainly used to build backend applications, REST APIs, and real-time applications like chat apps. It uses an **event-driven, non-blocking I/O** model, making it fast and scalable.

---

## 🤔 Why is it Needed?

- JavaScript originally worked only inside web browsers.
- Node.js allows JavaScript to run on the server.
- It lets developers use **one language (JavaScript)** for both frontend and backend.
- Without Node.js, you would need another backend language like Java, Python, or PHP.

---

## 🌊 Flow

```text
User Request
      ↓
Node.js receives the request
      ↓
If I/O operation (DB/File/API), send it to libuv
      ↓
Node.js continues handling other requests
      ↓
Operation completes
      ↓
Event Loop executes Callback/Promise
      ↓
Response sent to the user
```

---

## ✍️ Syntax

```javascript
console.log("Hello Node.js");
```

Run the file:

```bash
node app.js
```

---

## 💻 Example

```javascript
const http = require("http");

const server = http.createServer((req, res) => {
  res.end("Hello Node.js");
});

server.listen(3000, () => {
  console.log("Server is running on port 3000");
});
```

---

## 🎤 Interview Answer (30 Seconds)

> "Node.js is an open-source JavaScript runtime environment built on Google's V8 JavaScript Engine. It allows JavaScript to run outside the browser and is mainly used for backend development. It uses an event-driven, non-blocking I/O model, which makes it efficient for handling many concurrent requests. It is widely used for building REST APIs, real-time applications, and scalable server-side applications."

---

## 🧠 Memory Trick

**Node = JavaScript + Server**

Think of **Node.js** as a bridge that takes **JavaScript from the browser to the server**.

**Browser → JavaScript → Node.js → Server**

---

## ⭐ Keywords

- JavaScript Runtime
- V8 Engine
- Backend Development
- Event-Driven
- Non-Blocking I/O
- Server-Side JavaScript
- Scalable
- REST API
