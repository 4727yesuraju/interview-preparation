# Flatten Nested Arrays

🎯 Pattern
Recursion

💡 Insight
Check each element.
If the element is an array, go deeper.
Otherwise, add the value to the result.

🧠 Memory
Array Inside Array → Go Deeper

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function flattenArray(arr) {
  const result = [];

  for (const item of arr) {
    if (Array.isArray(item)) {
      result.push(...flattenArray(item));
    } else {
      result.push(item);
    }
  }

  return result;
}
```

🧪 Example

```text
Input:
[1, [2, [3, 4]], 5]

Initial:
result = []

Step 1:
1 → Add
result = [1]

Step 2:
[2, [3, 4]] → Array
Go inside

Step 3:
2 → Add
result = [1, 2]

Step 4:
[3, 4] → Array
Go inside

Step 5:
3 → Add
4 → Add

result = [1, 2, 3, 4]

Step 6:
5 → Add

Output:
[1, 2, 3, 4, 5]
```
