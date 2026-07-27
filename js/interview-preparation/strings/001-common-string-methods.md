# 📚 Common String Methods

## 📖 Simple English Explanation

String methods are built-in JavaScript functions used to **search, modify, extract, split, and combine strings**.

---

## 🤔 Why is it Needed?

- Search text.
- Change letter case.
- Extract part of a string.
- Remove extra spaces.
- Split and join text.

---

## 🌊 Flow

```text
String
   │
   ▼
String Methods
   │
   ├── Search
   ├── Extract
   ├── Replace
   ├── Split
   ├── Join
   └── Change Case
```

---

## ✍️ Syntax

```javascript
string.method();
```

---

## 💻 Example

### 1. `length`

```javascript
const str = "JavaScript";

console.log(str.length);
```

**Output**

```text
10
```

---

### 2. `toUpperCase()`

```javascript
const str = "hello";

console.log(str.toUpperCase());
```

**Output**

```text
HELLO
```

---

### 3. `toLowerCase()`

```javascript
const str = "HELLO";

console.log(str.toLowerCase());
```

**Output**

```text
hello
```

---

### 4. `trim()`

```javascript
const str = "  Hello  ";

console.log(str.trim());
```

**Output**

```text
Hello
```

---

### 5. `includes()`

```javascript
const str = "JavaScript";

console.log(str.includes("Script"));
```

**Output**

```text
true
```

---

### 6. `startsWith()`

```javascript
const str = "JavaScript";

console.log(str.startsWith("Java"));
```

**Output**

```text
true
```

---

### 7. `endsWith()`

```javascript
const str = "JavaScript";

console.log(str.endsWith("Script"));
```

**Output**

```text
true
```

---

### 8. `indexOf()`

```javascript
const str = "JavaScript";

console.log(str.indexOf("Script"));
```

**Output**

```text
4
```

---

### 9. `slice()`

```javascript
const str = "JavaScript";

console.log(str.slice(0, 4));
```

**Output**

```text
Java
```

---

### 10. `replace()`

```javascript
const str = "Hello World";

console.log(str.replace("World", "JavaScript"));
```

**Output**

```text
Hello JavaScript
```

---

### 11. `split()`

```javascript
const str = "HTML,CSS,JavaScript";

console.log(str.split(","));
```

**Output**

```text
["HTML", "CSS", "JavaScript"]
```

---

### 12. `concat()`

```javascript
const first = "Hello";
const second = " World";

console.log(first.concat(second));
```

**Output**

```text
Hello World
```

---

## 🎤 Interview Answer (30 Seconds)

JavaScript provides many built-in string methods to work with text. Common methods include `length`, `toUpperCase()`, `toLowerCase()`, `trim()`, `includes()`, `startsWith()`, `endsWith()`, `indexOf()`, `slice()`, `replace()`, `split()`, and `concat()`. These methods help search, modify, extract, and format strings.

---

## 🧠 Memory Trick

```text
String Methods

📏 length
🔍 includes(), indexOf()
✂️ slice(), split()
🔄 replace(), concat()
🔠 toUpperCase(), toLowerCase()
🧹 trim()
```

Easy Rule:

> **Search → includes(), indexOf()**

> **Extract → slice(), split()**

> **Modify → replace(), concat()**

> **Format → trim(), toUpperCase(), toLowerCase()**

---

## ⭐ Keywords

- length
- toUpperCase()
- toLowerCase()
- trim()
- includes()
- startsWith()
- endsWith()
- indexOf()
- slice()
- replace()
- split()
- concat()

```

```
