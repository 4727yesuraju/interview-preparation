# Find the Second Largest Number

🎯 Pattern
Linear Traversal

💡 Insight
Keep track of the largest and second largest numbers.
Update both values whenever a larger number is found.

🧠 Memory
Two Variables → Compare → Update

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function findSecondLargest(arr) {
  let largest = -Infinity;
  let secondLargest = -Infinity;

  for (let num of arr) {
    if (num > largest) {
      secondLargest = largest;
      largest = num;
    } else if (num > secondLargest && num !== largest) {
      secondLargest = num;
    }
  }

  return secondLargest;
}
```

🧪 Example

```text
Input:
[12, 45, 7, 89, 23]

Initial:
largest = -∞
secondLargest = -∞

Step 1:
12 > -∞ ✅
largest = 12
secondLargest = -∞

Step 2:
45 > 12 ✅
secondLargest = 12
largest = 45

Step 3:
7 > 12 ❌

Step 4:
89 > 45 ✅
secondLargest = 45
largest = 89

Step 5:
23 > 45 ❌

Output:
45
```
