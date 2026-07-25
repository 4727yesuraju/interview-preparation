# 📚 How does `reduce()` work?

## 📖 Simple English Explanation

`reduce()` is used to **reduce multiple array elements into a single value**.

The final value can be:

- A number (sum, average)
- A string
- An object
- Another array

---

## 🤔 Why is it Needed?

- Calculate total price.
- Find the sum or average.
- Count occurrences.
- Convert an array into an object.

---

## 🌊 Flow

```text
Array

[10, 20, 30, 40]
      │
      ▼
acc = 0

0 + 10 = 10
10 + 20 = 30
30 + 30 = 60
60 + 40 = 100

      │
      ▼
Final Result = 100
```

---

## ✍️ Syntax

```javascript
array.reduce((accumulator, currentValue) => {
  return updatedValue;
}, initialValue);
```

### Parameters

- **accumulator** → Stores the previous result.
- **currentValue** → Current array element.
- **initialValue** → Starting value of the accumulator.

---

## 💻 Example

### Example 1: Sum of Numbers

```javascript
const numbers = [10, 20, 30, 40];

const total = numbers.reduce((acc, num) => acc + num, 0);

console.log(total);
```

**Output**

```text
100
```

---

### Example 2: Multiply Numbers

```javascript
const numbers = [2, 3, 4];

const result = numbers.reduce((acc, num) => acc * num, 1);

console.log(result);
```

**Output**

```text
24
```

---

### Example 3: Count Occurrences

```javascript
const fruits = ["Apple", "Mango", "Apple"];

const count = fruits.reduce((acc, fruit) => {
  acc[fruit] = (acc[fruit] || 0) + 1;
  return acc;
}, {});

console.log(count);
```

**Output**

```text
{
  Apple: 2,
  Mango: 1
}
```

---

## 🎤 Interview Answer (30 Seconds)

`reduce()` iterates through an array and combines all elements into a single value. It uses an accumulator to store the result after each iteration. It is commonly used for calculating sums, averages, totals, counting items, and transforming arrays into objects.

---

## 🧠 Memory Trick

```text
Many Values
     │
     ▼
reduce()
     │
     ▼
One Value
```

Easy Rule:

> **reduce() = Many → One**

---

## ⭐ Keywords

- reduce()
- Accumulator
- Current Value
- Initial Value
- Single Value
- Array
