# 📚 What is `MutationObserver`?

## 📖 Simple English Explanation

`MutationObserver` is a browser API used to **watch for changes in the DOM (HTML page)**.

It automatically notifies you when something changes, such as:

- Adding an element
- Removing an element
- Changing text
- Changing attributes

Its callback is placed in the **Microtask Queue**, so it runs after the current synchronous code finishes but before macrotasks like `setTimeout()`.

---

## 🤔 Why is it Needed?

- Detect DOM changes automatically.
- Update the UI when the page changes.
- Monitor dynamically added or removed elements.
- Avoid continuously checking for changes (polling).

---

## 🌊 Flow

```text
HTML Element
      │
      ▼
MutationObserver
      │
(DOM Changes?)
      │
      ▼
Callback Added to
Microtask Queue
      │
      ▼
Event Loop
      │
      ▼
Execute Callback
```

---

## ✍️ Syntax

```javascript
const observer = new MutationObserver((mutations) => {
  // Code to run when the DOM changes
});

observer.observe(targetElement, {
  childList: true,
  attributes: true,
  subtree: true,
});
```

---

## 💻 Example

```javascript
const div = document.getElementById("box");

const observer = new MutationObserver(() => {
  console.log("DOM changed!");
});

observer.observe(div, {
  childList: true,
});

div.textContent = "Hello";
```

**Output**

```text
DOM changed!
```

---

## 🎤 Interview Answer (30 Seconds)

`MutationObserver` is a browser API that watches for changes in the DOM. When a watched element changes, its callback is added to the **Microtask Queue**. After the current synchronous code finishes, the Event Loop executes the callback before processing macrotasks like `setTimeout()`.

---

## 🧠 Memory Trick

```text
DOM Changes
     │
     ▼
MutationObserver 👀
     │
     ▼
Microtask Queue
     │
     ▼
Execute Callback
```

Easy Rule:

> **MutationObserver = Watch the DOM for changes.**

---

## ⭐ Keywords

- MutationObserver
- DOM
- Browser API
- Microtask Queue
- Event Loop
- Observe
- HTML Changes
