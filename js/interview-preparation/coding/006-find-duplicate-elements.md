# Find Duplicate Elements

🎯 Pattern
Hash Set

💡 Insight
Use one Set to track seen elements.
If an element already exists in the Set, it's a duplicate.

🧠 Memory
Seen? → Duplicate

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function findDuplicates(arr) {
  const seen = new Set();
  const duplicates = new Set();

  for (const num of arr) {
    if (seen.has(num)) {
      duplicates.add(num);
    } else {
      seen.add(num);
    }
  }

  return [...duplicates];
}
```

🧪 Example

```text
Input:
[1, 2, 3, 2, 4, 5, 1]

Initial:
seen = {}
duplicates = {}

Step 1:
1 → Add to seen

Step 2:
2 → Add to seen

Step 3:
3 → Add to seen

Step 4:
2 → Already seen ✅
duplicates = {2}

Step 5:
4 → Add to seen

Step 6:
5 → Add to seen

Step 7:
1 → Already seen ✅
duplicates = {2, 1}

Output:
[2, 1]
```
