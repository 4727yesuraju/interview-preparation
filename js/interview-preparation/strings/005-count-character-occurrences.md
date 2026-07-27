# 📚 Count Character Occurrences

## 📖 Simple English Explanation

Counting character occurrences means **finding how many times each character appears in a string**.

Example:

```text
"hello"

h → 1
e → 1
l → 2
o → 1
```

---

## 🤔 Why is it Needed?

- Count letter frequency.
- Analyze text.
- Solve coding interview questions.

---

## 🌊 Flow

```text
String

"hello"
    │
    ▼
Loop Through Characters
    │
    ▼
Store Count in Object
    │
    ▼
{
  h: 1,
  e: 1,
  l: 2,
  o: 1
}
```

---

## ✍️ Syntax

```javascript
const result = {};

for (const char of string) {
  result[char] = (result[char] || 0) + 1;
}
```

---

## 💻 Example

### Example 1: Using `for...of`

```javascript
const str = "hello";

const count = {};

for (const char of str) {
  count[char] = (count[char] || 0) + 1;
}

console.log(count);
```

**Output**

```text
{
  h: 1,
  e: 1,
  l: 2,
  o: 1
}
```

---

### Example 2: Using `reduce()`

```javascript
const str = "banana";

const count = str.split("").reduce((acc, char) => {
  acc[char] = (acc[char] || 0) + 1;
  return acc;
}, {});

console.log(count);
```

**Output**

```text
{
  b: 1,
  a: 3,
  n: 2
}
```

---

## 🎤 Interview Answer (30 Seconds)

To count character occurrences in a string, loop through each character and store the count in an object. If the character already exists, increment its count; otherwise, initialize it with `1`.

---

## 🧠 Memory Trick

```text
String
  │
  ▼
Loop
  │
  ▼
Object
  │
  ▼
Increase Count
```

Easy Rule:

> **Character → Object → Count**

---

## ⭐ Keywords

- Character Count
- Frequency
- Object
- for...of
- reduce()
- String

```

```
