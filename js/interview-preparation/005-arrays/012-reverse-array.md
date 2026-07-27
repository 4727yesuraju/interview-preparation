# 📚 Reverse an Array

## 📖 Simple English Explanation

Reversing an array means **changing the order of its elements from last to first**.

JavaScript provides the **`reverse()`** method to reverse an array.

---

## 🤔 Why is it Needed?

- Display data in reverse order.
- Show latest items first.
- Reverse the order of elements easily.

---

## 🌊 Flow

```text
Original Array

[10, 20, 30, 40]
      │
      ▼
reverse()
      │
      ▼
[40, 30, 20, 10]
```

---

## ✍️ Syntax

```javascript
array.reverse();
```

---

## 💻 Example

### Example 1: Reverse Numbers

```javascript
const numbers = [10, 20, 30, 40];

numbers.reverse();

console.log(numbers);
```

**Output**

```text
[40, 30, 20, 10]
```

---

### Example 2: Reverse Strings

```javascript
const fruits = ["Apple", "Mango", "Orange"];

fruits.reverse();

console.log(fruits);
```

**Output**

```text
["Orange", "Mango", "Apple"]
```

---

### Example 3: Keep Original Array Unchanged

```javascript
const numbers = [10, 20, 30, 40];

const reversed = [...numbers].reverse();

console.log(reversed);
console.log(numbers);
```

**Output**

```text
[40, 30, 20, 10]
[10, 20, 30, 40]
```

---

## 🎤 Interview Answer (30 Seconds)

`reverse()` is used to reverse the order of elements in an array. It modifies the original array and returns the reversed array. If you want to keep the original array unchanged, create a copy first using the spread operator.

---

## 🧠 Memory Trick

```text
First
 ↓
Last

Last
 ↑
First

reverse()
```

Easy Rule:

> **reverse() = First ↔ Last**

---

## ⭐ Keywords

- reverse()
- Array
- Reverse Order
- Original Array
- Spread Operator (`...`)
