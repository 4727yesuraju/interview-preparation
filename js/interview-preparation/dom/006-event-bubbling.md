# 📚 What is Event Bubbling?

## 📖 Simple English Explanation

**Event Bubbling** is the process where an event **starts from the target (clicked) element and moves upward through its parent elements**.

For example, if you click a button inside a `div`, the event happens in this order:

```text
Button → Div → Body → HTML → Document
```

This is the **default event propagation behavior** in JavaScript.

---

## 🤔 Why is it Needed?

- Allows parent elements to respond to child element events.
- Makes **Event Delegation** possible.
- Reduces the number of event listeners needed.

---

## 🌊 Flow

```text
HTML Structure

Document
   │
 HTML
   │
 Body
   │
 Div
   │
Button 👆 Click

Event Flow

Button
   │
   ▼
Div
   │
   ▼
Body
   │
   ▼
HTML
   │
   ▼
Document
```

---

## ✍️ Syntax

```javascript
element.addEventListener("click", callback);
```

---

## 💻 Example

### HTML

```html
<div id="parent">
  <button id="child">Click Me</button>
</div>
```

---

### JavaScript

```javascript
const parent = document.getElementById("parent");
const child = document.getElementById("child");

parent.addEventListener("click", () => {
  console.log("Parent Clicked");
});

child.addEventListener("click", () => {
  console.log("Button Clicked");
});
```

**Output (Click the button)**

```text
Button Clicked
Parent Clicked
```

**Why?**

1. The click happens on the **button**.
2. The button's event listener runs.
3. The event **bubbles up** to the parent `div`.
4. The parent's event listener runs.

---

### Stop Event Bubbling

```javascript
child.addEventListener("click", (event) => {
  event.stopPropagation();
  console.log("Button Clicked");
});
```

**Output**

```text
Button Clicked
```

> `event.stopPropagation()` prevents the event from bubbling to parent elements.

---

## 🎤 Interview Answer (30 Seconds)

Event Bubbling is the default event propagation mechanism in JavaScript. When an event occurs on a child element, it first executes on that element and then propagates upward through its parent elements until it reaches the document. It is useful for event delegation, and it can be stopped using `event.stopPropagation()`.

---

## 🧠 Memory Trick

```text
Click Button 👆
      │
      ▼
Button
      │
      ▼
Div
      │
      ▼
Body
      │
      ▼
HTML
      │
      ▼
Document
```

Easy Rule:

> **Event Bubbling = Child → Parent (Bottom → Top)**

---

## ⭐ Keywords

- Event Bubbling
- Event Propagation
- Parent Element
- Child Element
- addEventListener()
- click
- stopPropagation()
- Event Delegation
