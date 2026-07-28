# 📚 What is Event Delegation?

## 📖 Simple English Explanation

**Event Delegation** is a technique where you **attach one event listener to a parent element instead of adding listeners to every child element**.

When a child element is clicked, the event **bubbles up** to the parent, and the parent handles the event.

> **Simple Definition:**
>
> **Event Delegation means using one parent event listener to handle events for its child elements.**

---

## 🤔 Why is it Needed?

- Improves performance by reducing the number of event listeners.
- Handles dynamically added elements automatically.
- Makes code cleaner and easier to maintain.

---

## 🌊 Flow

```text
User Clicks <li>
        │
        ▼
Clicked <li>
        │
(Event Bubbling)
        ▼
<ul> Parent
        │
        ▼
Parent Checks
Which <li> Was Clicked
        │
        ▼
Execute Logic
```

---

## ✍️ Syntax

```javascript
parentElement.addEventListener("click", (event) => {
  if (event.target.matches("childSelector")) {
    // Handle child click
  }
});
```

---

## 💻 Example

### HTML

```html
<ul id="fruits">
  <li>Apple</li>
  <li>Mango</li>
  <li>Orange</li>
</ul>
```

---

### ❌ Without Event Delegation

```javascript
const items = document.querySelectorAll("li");

items.forEach((item) => {
  item.addEventListener("click", () => {
    console.log(item.textContent);
  });
});
```

> One event listener is added to **every `<li>`**.

---

### ✅ With Event Delegation

```javascript
const list = document.getElementById("fruits");

list.addEventListener("click", (event) => {
  if (event.target.tagName === "LI") {
    console.log(event.target.textContent);
  }
});
```

**Output (Click "Mango")**

```text
Mango
```

> Only **one event listener** is attached to the `<ul>`.

---

### Example: Dynamic Elements

```javascript
const newItem = document.createElement("li");
newItem.textContent = "Banana";

list.appendChild(newItem);
```

Now clicking **Banana** also works **without adding another event listener**, because the parent `<ul>` is already listening for click events.

---

## 📋 Without vs With Event Delegation

| Without Event Delegation                  | With Event Delegation              |
| ----------------------------------------- | ---------------------------------- |
| Event listener on every child             | One listener on parent             |
| More memory usage                         | Less memory usage                  |
| Doesn't handle new elements automatically | Handles new elements automatically |
| More code                                 | Cleaner code                       |

---

## 🎤 Interview Answer (30 Seconds)

Event Delegation is a technique where a single event listener is attached to a parent element instead of multiple child elements. It works because of **event bubbling**, where events travel from the child to the parent. The parent uses `event.target` to identify which child triggered the event. This improves performance, reduces memory usage, and automatically supports dynamically added elements.

---

## 🧠 Memory Trick

```text
Many Buttons
     │
     ▼
One Parent
     │
     ▼
One Event Listener
     │
     ▼
event.target
     │
     ▼
Find Clicked Child
```

Easy Rule:

> **Many Children → One Parent Listener**

---

## ⭐ Keywords

- Event Delegation
- Event Bubbling
- event.target
- Parent Element
- Child Element
- addEventListener()
- Dynamic Elements
- Performance
- DOM Events
