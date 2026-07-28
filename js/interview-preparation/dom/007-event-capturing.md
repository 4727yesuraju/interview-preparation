# 📚 What is Event Capturing?

## 📖 Simple English Explanation

**Event Capturing** (also called **Event Trickling**) is the process where an event **starts from the outermost parent element and moves down to the target element**.

For example, if you click a button inside a `div`, the event travels like this:

```text
Document → HTML → Body → Div → Button
```

Unlike Event Bubbling, **Event Capturing goes from top to bottom**.

---

## 🤔 Why is it Needed?

- Handle an event before it reaches the target element.
- Control the order of event execution.
- Useful in special cases where parent elements should react first.

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

Document
   │
   ▼
HTML
   │
   ▼
Body
   │
   ▼
Div
   │
   ▼
Button
```

---

## ✍️ Syntax

To enable event capturing, pass `true` (or `{ capture: true }`) as the third argument to `addEventListener()`.

```javascript
element.addEventListener("click", callback, true);
```

or

```javascript
element.addEventListener("click", callback, {
  capture: true,
});
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

parent.addEventListener(
  "click",
  () => {
    console.log("Parent Clicked");
  },
  true,
);

child.addEventListener("click", () => {
  console.log("Button Clicked");
});
```

**Output (Click the button)**

```text
Parent Clicked
Button Clicked
```

**Why?**

1. The click starts from the outer parent.
2. The parent's capturing listener runs first.
3. Then the event reaches the button.
4. The button's listener runs.

---

## 📋 Event Capturing vs Event Bubbling

| Feature          | Event Capturing | Event Bubbling |
| ---------------- | --------------- | -------------- |
| Direction        | Parent → Child  | Child → Parent |
| Also Called      | Trickling       | Bubbling       |
| Default Behavior | ❌ No           | ✅ Yes         |
| Enable           | `capture: true` | Default        |

---

## 🎤 Interview Answer (30 Seconds)

Event Capturing is the event propagation phase where an event travels from the outermost parent element down to the target element. It is not the default behavior in JavaScript. To use it, we pass `true` or `{ capture: true }` as the third argument to `addEventListener()`. It is useful when parent elements need to handle an event before the child element.

---

## 🧠 Memory Trick

```text
Click Button 👆

Document
   │
   ▼
HTML
   │
   ▼
Body
   │
   ▼
Div
   │
   ▼
Button
```

Easy Rule:

> **Event Capturing = Parent → Child (Top → Bottom)**

---

## ⭐ Keywords

- Event Capturing
- Event Trickling
- Event Propagation
- Parent Element
- Child Element
- addEventListener()
- capture: true
- DOM Events
