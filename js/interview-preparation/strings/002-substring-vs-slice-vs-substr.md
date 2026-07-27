# 📚 `substring()` vs `slice()` vs `substr()`

## 📖 Simple English Explanation

All three methods are used to **extract part of a string**, but they work differently.

- **`slice()`** → Extracts characters using **start and end indexes**. Supports **negative indexes**.
- **`substring()`** → Extracts characters using **start and end indexes**. **Does not support negative indexes**.
- **`substr()`** → Extracts characters using **start index and length**. It is **deprecated** (avoid using it).

---

## 🤔 Why is it Needed?

- Extract a part of a string.
- Display specific text.
- Process user input or file names.

---

## 🌊 Flow

```text
Need Part of String
        │
        ▼
 ┌───────────────┬────────────────┬─────────────────┐
 │               │                │
 ▼               ▼                ▼
slice()     substring()      substr()
Start-End   Start-End        Start-Length
Negative ✔️  Negative ❌      Deprecated ❌
```

---

## ✍️ Syntax

### `slice()`

```javascript
string.slice(start, end);
```

### `substring()`

```javascript
string.substring(start, end);
```

### `substr()` (Deprecated)

```javascript
string.substr(start, length);
```

---

## 💻 Example

### Example 1: `slice()`

```javascript
const str = "JavaScript";

console.log(str.slice(0, 4));
console.log(str.slice(-6));
```

**Output**

```text
Java
Script
```

---

### Example 2: `substring()`

```javascript
const str = "JavaScript";

console.log(str.substring(0, 4));
console.log(str.substring(-6));
```

**Output**

```text
Java
JavaScript
```

> `substring()` treats negative values as `0`.

---

### Example 3: `substr()` (Deprecated)

```javascript
const str = "JavaScript";

console.log(str.substr(4, 6));
```

**Output**

```text
Script
```

---

## 🎤 Interview Answer (30 Seconds)

All three methods extract part of a string. `slice()` supports negative indexes, making it the most flexible. `substring()` does not support negative indexes. `substr()` uses a start index and length, but it is deprecated, so `slice()` is the recommended method in modern JavaScript.

---

## 🧠 Memory Trick

```text
slice()
↓
Start → End ✅
Negative ✅

substring()
↓
Start → End
Negative ❌

substr()
↓
Start → Length
Deprecated ❌
```

Easy Rule:

> **slice = Best Choice**

> **substring = No Negative Index**

> **substr = Deprecated**

---

## ⭐ Keywords

- slice()
- substring()
- substr()
- String
- Start Index
- End Index
- Length
- Negative Index
- Deprecated
