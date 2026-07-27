# 📚 Reverse a String

## 📖 Simple English Explanation

Reversing a string means **changing the order of its characters from last to first**.

Example:

```javascript
"hello";
```

becomes

```javascript
"olleh";
```

---

## 🤔 Why is it Needed?

- Reverse text.
- Solve coding interview questions.
- Work with string manipulation problems.

---

## 🌊 Flow

```text
Original String

"hello"
    │
    ▼
split("")
    │
    ▼
["h","e","l","l","o"]
    │
    ▼
reverse()
    │
    ▼
["o","l","l","e","h"]
    │
    ▼
join("")
    │
    ▼
"olleh"
```

---

## ✍️ Syntax

```javascript
string.split("").reverse().join("");
```

---

## 💻 Example

### Example 1: Reverse a String

```javascript
const str = "hello";

const reversed = str.split("").reverse().join("");

console.log(reversed);
```

**Output**

```text
olleh
```

---

### Example 2: Reverse Another String

```javascript
const str = "JavaScript";

console.log(str.split("").reverse().join(""));
```

**Output**

```text
tpircSavaJ
```

---

## 🎤 Interview Answer (30 Seconds)

To reverse a string in JavaScript, first convert the string into an array using `split("")`, then reverse the array using `reverse()`, and finally convert it back to a string using `join("")`.

---

## 🧠 Memory Trick

```text
String
  │
  ▼
split("")
  │
  ▼
Array
  │
  ▼
reverse()
  │
  ▼
Array
  │
  ▼
join("")
  │
  ▼
Reversed String
```

Easy Rule:

> **Split → Reverse → Join**

---

## ⭐ Keywords

- split()
- reverse()
- join()
- String
- Array
- Reverse

```

```
