# 📚 `preventDefault()` vs `stopPropagation()`

## 📖 Simple English Explanation

Both `preventDefault()` and `stopPropagation()` are methods of the **Event** object, but they do **different jobs**.

- **`preventDefault()`** → Stops the browser's **default action**.
- **`stopPropagation()`** → Stops the event from **moving to parent elements**.

> **Simple Definition:**
>
> - **`preventDefault()` = Stop the browser's default behavior.**
> - **`stopPropagation()` = Stop event bubbling/capturing.**

---

## 🤔 Why is it Needed?

### `preventDefault()`

- Prevent form submission.
- Prevent link navigation.
- Prevent browser's default behavior.

### `stopPropagation()`

- Prevent parent event listeners from executing.
- Control event propagation.
- Avoid unwanted event bubbling.

---

## 🌊 Flow

### `preventDefault()`

```text
User Clicks Link
        │
        ▼
JavaScript
        │
preventDefault()
        │
        ▼
❌ Browser Does NOT Navigate
```

### `stopPropagation()`

```text
Button Click
      │
      ▼
Button Listener
      │
stopPropagation()
      │
      ▼
❌ Parent Listener Does NOT Execute
```

---

## ✍️ Syntax

### `preventDefault()`

```javascript
event.preventDefault();
```

### `stopPropagation()`

```javascript
event.stopPropagation();
```

---

## 💻 Example

### Example 1: `preventDefault()`

**HTML**

```html
<a href="https://google.com">Google</a>
```

**JavaScript**

```javascript
const link = document.querySelector("a");

link.addEventListener("click", (event) => {
  event.preventDefault();

  console.log("Navigation prevented");
});
```

**Output**

```text
Navigation prevented
```

> The browser **does not open Google** because the default action is prevented.

---

### Example 2: `stopPropagation()`

**HTML**

```html
<div id="parent">
  <button id="child">Click</button>
</div>
```

**JavaScript**

```javascript
const parent = document.getElementById("parent");
const child = document.getElementById("child");

parent.addEventListener("click", () => {
  console.log("Parent Clicked");
});

child.addEventListener("click", (event) => {
  event.stopPropagation();

  console.log("Button Clicked");
});
```

**Output**

```text
Button Clicked
```

> The parent's event listener does **not** run because propagation is stopped.

---

### Example 3: Using Both Together

```javascript
form.addEventListener("submit", (event) => {
  event.preventDefault();
  event.stopPropagation();

  console.log("Form handled manually");
});
```

---

## 📋 Comparison

| Feature                      | `preventDefault()` | `stopPropagation()` |
| ---------------------------- | ------------------ | ------------------- |
| Stops browser default action | ✅ Yes             | ❌ No               |
| Stops event bubbling         | ❌ No              | ✅ Yes              |
| Stops event capturing        | ❌ No              | ✅ Yes              |
| Used for forms and links     | ✅ Yes             | ❌ No               |
| Used for parent-child events | ❌ No              | ✅ Yes              |

---

## 🎤 Interview Answer (30 Seconds)

`preventDefault()` stops the browser's default behavior, such as submitting a form or opening a link. `stopPropagation()` stops the event from propagating to parent or ancestor elements during the capturing or bubbling phases. They solve different problems and are often used together when needed.

---

## 🧠 Memory Trick

```text
preventDefault()
        │
        ▼
Stop Browser Action 🚫

stopPropagation()
        │
        ▼
Stop Event Travel 🚫
```

Easy Rule:

> **`preventDefault()` → Stop Browser**

> **`stopPropagation()` → Stop Event**

---

## ⭐ Keywords

- preventDefault()
- stopPropagation()
- Event
- Event Bubbling
- Event Capturing
- Default Action
- Form Submission
- Link Navigation
- DOM Events
