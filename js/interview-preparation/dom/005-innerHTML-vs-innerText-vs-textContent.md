# 📚 `innerHTML` vs `innerText` vs `textContent`

## 📖 Simple English Explanation

These three properties are used to **read or change the content of an HTML element**, but they behave differently.

- **`innerHTML`** → Gets or sets **HTML content** (including tags).
- **`innerText`** → Gets or sets **only the visible text**.
- **`textContent`** → Gets or sets **all text**, including hidden text, but ignores HTML tags.

---

## 🤔 Why is it Needed?

- **`innerHTML`** → Add or read HTML elements.
- **`innerText`** → Work with only the text visible to users.
- **`textContent`** → Work with all text quickly and safely.

---

## 🌊 Flow

```text
Element
   │
   ├── innerHTML
   │      ▼
   │   HTML + Text
   │
   ├── innerText
   │      ▼
   │   Visible Text Only
   │
   └── textContent
          ▼
      All Text
(Hidden + Visible)
```

---

## ✍️ Syntax

### `innerHTML`

```javascript
element.innerHTML = "<b>Hello</b>";
```

### `innerText`

```javascript
element.innerText = "Hello";
```

### `textContent`

```javascript
element.textContent = "Hello";
```

---

## 💻 Example

### HTML

```html
<div id="box">
  <b>Hello</b>
  <span style="display:none">Hidden</span>
</div>
```

---

### Example 1: `innerHTML`

```javascript
const box = document.getElementById("box");

console.log(box.innerHTML);
```

**Output**

```html
<b>Hello</b> <span style="display:none">Hidden</span>
```

> Returns the HTML inside the element.

---

### Example 2: `innerText`

```javascript
console.log(box.innerText);
```

**Output**

```text
Hello
```

> Returns only the text visible on the page.

---

### Example 3: `textContent`

```javascript
console.log(box.textContent);
```

**Output**

```text
Hello
Hidden
```

> Returns all text, including hidden text.

---

### Example 4: Setting Values

```javascript
box.innerHTML = "<h1>Welcome</h1>";
```

**Result**

```html
<div id="box">
  <h1>Welcome</h1>
</div>
```

```javascript
box.innerText = "<h1>Welcome</h1>";
```

**Result**

```text
<h1>Welcome</h1>
```

```javascript
box.textContent = "<h1>Welcome</h1>";
```

**Result**

```text
<h1>Welcome</h1>
```

---

## 📋 Comparison

| Feature            | `innerHTML`          | `innerText`                | `textContent`              |
| ------------------ | -------------------- | -------------------------- | -------------------------- |
| Reads HTML tags    | ✅ Yes               | ❌ No                      | ❌ No                      |
| Reads visible text | ✅ Yes               | ✅ Yes                     | ✅ Yes                     |
| Reads hidden text  | ✅ Yes (inside HTML) | ❌ No                      | ✅ Yes                     |
| Can insert HTML    | ✅ Yes               | ❌ No (shows tags as text) | ❌ No (shows tags as text) |
| Performance        | Slowest              | Slower                     | Fastest                    |

---

## 🎤 Interview Answer (30 Seconds)

`innerHTML` reads or writes HTML content, so it can create new HTML elements. `innerText` reads or writes only the text visible to the user and ignores hidden text. `textContent` reads or writes all text, including hidden text, without interpreting HTML tags. For plain text updates, `textContent` is usually preferred because it is faster and safer.

---

## 🧠 Memory Trick

```text
innerHTML
     │
     ▼
HTML + Text

innerText
     │
     ▼
Visible Text

textContent
     │
     ▼
All Text
(Hidden + Visible)
```

Easy Rule:

> **`innerHTML` → HTML**

> **`innerText` → Visible Text**

> **`textContent` → All Text**

---

## ⭐ Keywords

- innerHTML
- innerText
- textContent
- HTML
- Visible Text
- Hidden Text
- DOM
- Element
- Content Manipulation
