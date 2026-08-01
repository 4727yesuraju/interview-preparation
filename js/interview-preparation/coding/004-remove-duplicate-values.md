# Remove Duplicate Values

🎯 Pattern
Hash Set

💡 Insight
A Set stores only unique values.
Convert the array to a Set, then back to an array.

🧠 Memory
Array → Set → Array

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function removeDuplicates(arr) {
  return [...new Set(arr)];
}
```

🧪 Example

```text
Input:
[1, 2, 2, 3, 4, 4, 5]

Initial:
Set = {}

Step 1:
Add 1 → {1}

Step 2:
Add 2 → {1, 2}

Step 3:
Add 2 → Already exists ❌

Step 4:
Add 3 → {1, 2, 3}

Step 5:
Add 4 → {1, 2, 3, 4}

Step 6:
Add 4 → Already exists ❌

Step 7:
Add 5 → {1, 2, 3, 4, 5}

Output:
[1, 2, 3, 4, 5]
```
