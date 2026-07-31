# 📚 What is Memoization?

## 📖 Simple English Explanation

**Memoization** is an optimization technique where the **result of an expensive function is stored (cached)**.

If the function is called again with the **same input**, JavaScript returns the **cached result** instead of calculating it again.

This makes the application **faster** and avoids unnecessary work.

> **Simple Definition:**
>
> **Memoization is storing a function's result so repeated calls with the same input return the cached result instead of recalculating it.**

---

## 🤔 Why is it Needed?

- Improve performance.
- Avoid repeating expensive calculations.
- Reduce execution time.
- Useful for recursive functions and API-like computations.

---

## 🌊 Flow

```text
Function Call (5)
        │
        ▼
Already Cached?
        │
   ┌────┴────┐
   │         │
 No         Yes
   │         │
   ▼         ▼
Calculate   Return Cached Result
   │
   ▼
Store in Cache
```

---

## ✍️ Syntax

```javascript
const cache = {};

function memoizedFunction(value) {
  if (cache[value]) {
    return cache[value];
  }

  const result = expensiveCalculation(value);

  cache[value] = result;

  return result;
}
```

---

## 💻 Example

### Example 1: Without Memoization

```javascript
function square(n) {
  console.log("Calculating...");
  return n * n;
}

console.log(square(5));
console.log(square(5));
```

**Output**

```text
Calculating...
25

Calculating...
25
```

The calculation runs **twice**.

---

### Example 2: With Memoization

```javascript
const cache = {};

function square(n) {
  if (cache[n]) {
    console.log("From Cache");
    return cache[n];
  }

  console.log("Calculating...");

  const result = n * n;

  cache[n] = result;

  return result;
}

console.log(square(5));
console.log(square(5));
```

**Output**

```text
Calculating...
25

From Cache
25
```

The second call uses the cached result.

---

### Example 3: Recursive Fibonacci

Without memoization:

```javascript
function fib(n) {
  if (n <= 1) return n;

  return fib(n - 1) + fib(n - 2);
}
```

Many values are calculated repeatedly.

With memoization:

```javascript
const cache = {};

function fib(n) {
  if (n in cache) return cache[n];

  if (n <= 1) return n;

  cache[n] = fib(n - 1) + fib(n - 2);

  return cache[n];
}
```

Previously calculated Fibonacci numbers are reused, making the function much faster.

---

## 📋 Without vs With Memoization

| Without Memoization     | With Memoization        |
| ----------------------- | ----------------------- |
| Recalculates every time | Uses cached result      |
| Slower                  | Faster                  |
| More CPU work           | Less CPU work           |
| No cache                | Stores previous results |

---

## 🌍 Real-World Uses

| Example                   | Why Use Memoization?               |
| ------------------------- | ---------------------------------- |
| Fibonacci calculation     | Avoid repeated recursion           |
| Mathematical calculations | Reuse previous results             |
| React (`useMemo`)         | Prevent unnecessary recalculations |
| Dynamic programming       | Improve algorithm performance      |
| Expensive data processing | Cache computed values              |

---

## 🎤 Interview Answer (30 Seconds)

Memoization is an optimization technique that stores the results of expensive function calls in a cache. When the function is called again with the same input, it returns the cached result instead of recalculating it. This improves performance and is commonly used in recursive algorithms, dynamic programming, and React's `useMemo`.

---

## 🧠 Memory Trick

```text
Input = 5
     │
     ▼
Cache Exists?
     │
 ┌───┴───┐
 │       │
 No     Yes
 │       │
 ▼       ▼
Calculate Return Cached Value
 │
 ▼
Save to Cache
```

Easy Rule:

> **First Time → Calculate**

> **Next Time → Cache**

---

## ⭐ Keywords

- Memoization
- Cache
- Optimization
- Performance
- Expensive Function
- Dynamic Programming
- React `useMemo`
- Reuse Results
