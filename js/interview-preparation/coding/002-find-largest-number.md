# Find the Largest Number

🎯 Pattern
Linear Traversal

💡 Insight
Assume the first number is the largest.
Compare it with every other number.
Update the largest value whenever a bigger number is found.

🧠 Memory
Start → Compare → Update

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function findLargest(arr) {
  let largest = arr[0];

  for (let i = 1; i < arr.length; i++) {
    if (arr[i] > largest) {
      largest = arr[i];
    }
  }

  return largest;
}
```

🧪 Example

```text
Input:
[12, 45, 7, 89, 23]

Initial:
largest = 12

Step 1:
45 > 12 ✅
largest = 45

Step 2:
7 > 45 ❌

Step 3:
89 > 45 ✅
largest = 89

Step 4:
23 > 89 ❌

Output:
89
```
