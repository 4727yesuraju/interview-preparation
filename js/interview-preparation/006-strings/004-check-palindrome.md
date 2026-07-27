# 📚 Check if a String is a Palindrome

## 📖 Simple English Explanation

A **palindrome** is a string that **reads the same forward and backward**.

Examples:

```text
madam ✅
racecar ✅
level ✅
hello ❌
```

---

## 🤔 Why is it Needed?

- Solve coding interview questions.
- Practice string manipulation.
- Check if a word or sentence is symmetrical.

---

## 🌊 Flow

```text
Original String

"madam"
    │
    ▼
Reverse String

"madam"
    │
    ▼
Compare

Original === Reversed
    │
    ▼
Palindrome ✅
```

---

## ✍️ Syntax

```javascript
const isPalindrome = str === str.split("").reverse().join("");
```

---

## 💻 Example

### Example 1: Palindrome

```javascript
const str = "madam";

const isPalindrome = str === str.split("").reverse().join("");

console.log(isPalindrome);
```

**Output**

```text
true
```

---

### Example 2: Not a Palindrome

```javascript
const str = "hello";

const isPalindrome = str === str.split("").reverse().join("");

console.log(isPalindrome);
```

**Output**

```text
false
```

---

### Example 3: Using a Function

```javascript
function isPalindrome(str) {
  return str === str.split("").reverse().join("");
}

console.log(isPalindrome("level"));
console.log(isPalindrome("world"));
```

**Output**

```text
true
false
```

---

## 🎤 Interview Answer (30 Seconds)

A palindrome is a string that reads the same forward and backward. To check if a string is a palindrome, reverse the string using `split()`, `reverse()`, and `join()`, then compare it with the original string. If both are equal, it is a palindrome.

---

## 🧠 Memory Trick

```text
Original
   │
   ▼
Reverse
   │
   ▼
Compare
   │
   ▼
Same?
   │
   ├── Yes ✅ Palindrome
   └── No ❌ Not Palindrome
```

Easy Rule:

> **Reverse + Compare = Palindrome Check**

---

## ⭐ Keywords

- Palindrome
- split()
- reverse()
- join()
- Compare
- String

```

```
