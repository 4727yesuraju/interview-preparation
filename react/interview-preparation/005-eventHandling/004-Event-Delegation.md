# Event Delegation

## 📖 Simple English Explanation

### What is it?

**Event Delegation** is a technique where **one parent element handles events for its child elements** instead of adding an event listener to every child.

React uses **Event Delegation** internally to improve performance.

### Why do we need it?

- To reduce the number of event listeners.
- To improve performance.
- To automatically handle events for dynamically added elements.

---

## 🌊 Flow

```text
User Clicks Child Element
        ↓
Event Bubbles Up
        ↓
Parent Receives the Event
        ↓
Parent Event Handler Executes
```

---

## ✍️ Syntax

### JavaScript Example

```javascript
document.getElementById("list").addEventListener("click", (event) => {
  console.log(event.target.textContent);
});
```

> **Note:** In React, you usually add events directly to JSX elements. React internally uses **Event Delegation**, so you don't need to implement it manually in most cases.

---

## 💻 Example

### JavaScript (Event Delegation)

```html
<ul id="list">
  <li>Apple</li>
  <li>Mango</li>
  <li>Orange</li>
</ul>
```

```javascript
document.getElementById("list").addEventListener("click", (event) => {
  alert(event.target.textContent);
});
```

### What happens?

```text
Click "Mango"
      ↓
Event Bubbles to <ul>
      ↓
<ul> Event Handler Runs
      ↓
Output: Mango
```

Only **one event listener** is attached to the `<ul>`, but it can handle clicks on all `<li>` elements.

---

## 🎤 Interview Explanation

**Event Delegation** is a technique where a **single parent element handles events for its child elements** using **event bubbling**. Instead of attaching an event listener to every child, we attach one listener to the parent. React uses Event Delegation internally to reduce the number of event listeners and improve performance.

---

## 🧠 Memory Trick

👨‍🏫 **Think of a classroom.**

```text
Students Raise Hands
        ↓
Teacher Notices
        ↓
Teacher Responds
```

- 👨‍🏫 **Teacher** = Parent Element
- 👨‍🎓 **Students** = Child Elements

**One Teacher handles many Students.**

**Remember:**

**One Parent → Many Children → One Event Listener**
