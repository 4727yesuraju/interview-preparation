# 📚 What are Rest Parameters?

## 📖 Simple English Explanation

**Rest parameters** allow a function to accept **any number of arguments**.

They collect all the remaining arguments into a **single array** using the **`...` (spread/rest) operator**.

---

## 🤔 Why is it Needed?

- Allows functions to accept multiple arguments.
- Eliminates the need to know the exact number of arguments.
- Makes functions more flexible and reusable.

---

## 🌊 Flow

```text
Function Called
        │
        ▼
Multiple Arguments Passed
        │
        ▼
... Rest Parameter
        │
        ▼
Collects Remaining Arguments
into an Array
```

---

## ✍️ Syntax

```javascript
function functionName(...args) {
  // args is an array
}
```

---

## 💻 Example

### Example 1: Collect All Arguments

```javascript
function sum(...numbers) {
  console.log(numbers);
}

sum(10, 20, 30);
```

**Output**

```text
[10, 20, 30]
```

---

### Example 2: Calculate Sum

```javascript
function sum(...numbers) {
  let total = 0;

  for (let num of numbers) {
    total += num;
  }

  return total;
}

console.log(sum(10, 20, 30));
```

**Output**

```text
60
```

---

### Example 3: Fixed + Rest Parameters

```javascript
function introduce(name, ...hobbies) {
  console.log(name);
  console.log(hobbies);
}

introduce("John", "Cricket", "Coding", "Music");
```

**Output**

```text
John
["Cricket", "Coding", "Music"]
```

---

## 🎤 Interview Answer (30 Seconds)

Rest parameters are an ES6 feature that allows a function to accept any number of arguments. They use the `...` syntax to collect the remaining arguments into a single array, making functions more flexible and easier to work with.

---

## 🧠 Memory Trick

```text
Many Arguments
       │
       ▼
...args
       │
       ▼
Array
```

Easy Rule:

> **Rest = Collect Remaining Arguments into an Array**

---

## ⭐ Keywords

- Rest Parameters
- `...`
- ES6
- Array
- Function Arguments
- Variable Arguments
