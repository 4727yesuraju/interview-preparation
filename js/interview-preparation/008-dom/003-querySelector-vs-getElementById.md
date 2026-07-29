querySelector-vs-getElementById.md

# 📚 `querySelector()` vs `getElementById()`

## 📖 Simple English Explanation

Both methods are used to **select elements from the DOM**, but they work differently.

- **`getElementById()`** → Selects an element **only by its `id`**.
- **`querySelector()`** → Selects the **first element** that matches any valid **CSS selector** (id, class, tag, attribute, etc.).

---

## 🤔 Why is it Needed?

- Use **`getElementById()`** when you know the element's **id**.
- Use **`querySelector()`** when you need the flexibility of **CSS selectors**.

---

## 🌊 Flow

```text
Need an Element
       │
       ▼
Do you know the ID?
       │
   ┌───┴───┐
   ▼       ▼
 Yes       No
   │        │
   ▼        ▼
getElementById()   querySelector()
                   (#id, .class, tag...)
```

---

## ✍️ Syntax

### `getElementById()`

```javascript
document.getElementById("title");
```

### `querySelector()`

```javascript
document.querySelector("#title");
document.querySelector(".box");
document.querySelector("button");
```

---

## 💻 Example

### HTML

```html
<h1 id="title">Hello</h1>

<p class="text">Paragraph</p>

<button>Click Me</button>
```

---

### Example 1: `getElementById()`

```javascript
const heading = document.getElementById("title");

console.log(heading.textContent);
```

**Output**

```text
Hello
```

---

### Example 2: `querySelector()`

```javascript
const heading = document.querySelector("#title");
const paragraph = document.querySelector(".text");
const button = document.querySelector("button");

console.log(heading.textContent);
console.log(paragraph.textContent);
console.log(button.textContent);
```

**Output**

```text
Hello
Paragraph
Click Me
```

---

## 📋 Comparison

| Feature                | `getElementById()` | `querySelector()`                        |
| ---------------------- | ------------------ | ---------------------------------------- |
| Select by ID           | ✅ Yes             | ✅ Yes (`#id`)                           |
| Select by Class        | ❌ No              | ✅ Yes (`.class`)                        |
| Select by Tag          | ❌ No              | ✅ Yes (`div`, `button`)                 |
| Select by CSS Selector | ❌ No              | ✅ Yes                                   |
| Returns                | One element        | First matching element                   |
| Performance            | Slightly faster    | Slightly slower (supports CSS selectors) |

---

## 🎤 Interview Answer (30 Seconds)

`getElementById()` selects an element only by its unique ID and is slightly faster because it performs a direct lookup. `querySelector()` is more flexible because it accepts any valid CSS selector, such as an ID, class, tag, or attribute, but it returns only the first matching element.

---

## 🧠 Memory Trick

```text
Need Only ID?
      │
      ▼
getElementById()

Need CSS Selector?
(#id, .class, tag)
      │
      ▼
querySelector()
```

Easy Rule:

> **Only ID → `getElementById()`**

> **Any CSS Selector → `querySelector()`**

---

## ⭐ Keywords

- DOM
- querySelector()
- getElementById()
- CSS Selector
- ID
- Class
- Tag
- First Match
- Element
