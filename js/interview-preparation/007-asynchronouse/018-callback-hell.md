# 📚 What is Callback Hell?

## 📖 Simple English Explanation

**Callback Hell** is a situation where **callbacks are nested inside other callbacks**, making the code difficult to read, understand, and maintain.

It is also called the **"Pyramid of Doom"** because the code keeps moving to the right.

---

## 🤔 Why is it Needed?

Before Promises and `async/await`, callbacks were the main way to handle asynchronous operations.

When multiple asynchronous tasks had to run one after another, developers nested callbacks, leading to Callback Hell.

---

## 🌊 Flow

```text
Login User
     │
     ▼
Get User Profile
     │
     ▼
Get User Orders
     │
     ▼
Get Payment Details
     │
     ▼
Display Data
```

Without Promises, each step is written inside the previous callback.

---

## ✍️ Syntax

### Callback Hell

```javascript
loginUser(function (user) {
  getProfile(user, function (profile) {
    getOrders(profile, function (orders) {
      console.log(orders);
    });
  });
});
```

---

## 💻 Example

### Example 1: Callback Hell

```javascript
setTimeout(() => {
  console.log("Step 1");

  setTimeout(() => {
    console.log("Step 2");

    setTimeout(() => {
      console.log("Step 3");
    }, 1000);
  }, 1000);
}, 1000);
```

**Output**

```text
Step 1
Step 2
Step 3
```

---

### Example 2: Using Promises (Better)

```javascript
doStep1().then(doStep2).then(doStep3).catch(console.error);
```

---

### Example 3: Using `async/await` (Best Readability)

```javascript
async function runSteps() {
  try {
    await doStep1();
    await doStep2();
    await doStep3();
  } catch (error) {
    console.log(error);
  }
}
```

---

## 🎤 Interview Answer (30 Seconds)

Callback Hell is a situation where multiple callbacks are nested inside one another, making the code difficult to read, debug, and maintain. It usually happens when several asynchronous operations depend on each other. Modern JavaScript solves this problem using Promises and `async/await`.

---

## 🧠 Memory Trick

```text
Callback
   │
   ▼
Callback
   │
   ▼
Callback
   │
   ▼
😵 Callback Hell
```

Easy Rule:

> **More nested callbacks = Callback Hell**

---

## ⭐ Keywords

- Callback Hell
- Pyramid of Doom
- Nested Callbacks
- Asynchronous
- Promise
- async/await
- Readability
