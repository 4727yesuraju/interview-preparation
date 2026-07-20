# 📚 What is `NaN`?

## 📖 Simple English Explanation

**NaN** stands for **Not a Number**.

It is a special value in JavaScript that represents the result of an **invalid mathematical operation**.

Although its name is **"Not a Number"**, its data type is actually **Number**.

---

## 🤔 Why is it Needed?

- To indicate that a mathematical calculation has failed.
- Helps JavaScript identify invalid numeric operations.
- Prevents the program from crashing when calculations are invalid.

---

## 🌊 Flow

```text
Perform a Mathematical Operation
            │
            ▼
Is the operation valid?
      │
 ┌────┴────┐
 │         │
Yes       No
 │         │
 ▼         ▼
Result    NaN
```

---

## ✍️ Syntax

```javascript
Number("Hello"); // NaN
```

---

## 💻 Example

```javascript
console.log(0 / 0); // NaN

console.log(Number("Hello")); // NaN

console.log(typeof NaN); // "number"
```

---

## 🎤 Interview Answer (30 Seconds)

**NaN** stands for **Not a Number**. It is a special value in JavaScript that represents the result of an invalid mathematical operation. Even though its name is "Not a Number", its data type is **Number**.

---

## 🧠 Memory Trick

```text
NaN

N → Not
a → a
N → Number

Invalid Math
        ↓
      NaN
```

Remember:

> **Invalid Calculation = NaN**

---

## ⭐ Keywords

- NaN
- Not a Number
- Number
- Invalid Math
- Mathematical Operation
- `typeof NaN`
