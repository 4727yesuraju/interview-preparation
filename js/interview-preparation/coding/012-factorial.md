# Factorial

🎯 Pattern
Iteration

💡 Insight
Multiply all numbers from 1 to n.
Start with result as 1 and keep multiplying.

🧠 Memory
Result × Current Number

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function factorial(n) {
  let result = 1;

  for (let i = 1; i <= n; i++) {
    result *= i;
  }

  return result;
}
```

🧪 Example

```text
Input:
5

Initial:
result = 1

Step 1:
1 × 1 = 1

Step 2:
1 × 2 = 2

Step 3:
2 × 3 = 6

Step 4:
6 × 4 = 24

Step 5:
24 × 5 = 120

Output:
120
```
