# Find Missing Number

🎯 Pattern
Math Formula

💡 Insight
Find the expected sum of numbers from 1 to n.
Subtract the actual array sum.
The difference is the missing number.

🧠 Memory
Expected Sum − Actual Sum = Missing Number

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function findMissingNumber(arr) {
  const n = arr.length + 1;

  const expectedSum = (n * (n + 1)) / 2;
  const actualSum = arr.reduce((sum, num) => sum + num, 0);

  return expectedSum - actualSum;
}
```

🧪 Example

```text
Input:
[1, 2, 4, 5]

n = 5

Expected Sum:
1 + 2 + 3 + 4 + 5 = 15

Actual Sum:
1 + 2 + 4 + 5 = 12

Missing Number:
15 - 12 = 3

Output:
3
```
