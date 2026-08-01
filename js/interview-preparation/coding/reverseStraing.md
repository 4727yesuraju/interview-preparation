# Reverse a String

🎯 Pattern
Two Pointers

💡 Insight
Swap the first and last characters.
Move both pointers toward the center until they meet.

🧠 Memory
Outside → Inside

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function reverseString(str) {
  const arr = str.split("");
  let left = 0;
  let right = arr.length - 1;

  while (left < right) {
    [arr[left], arr[right]] = [arr[right], arr[left]];
    left++;
    right--;
  }

  return arr.join("");
}
```

🧪 Example

```text
Input:
"hello"

Initial:
h e l l o
↑       ↑

Step 1 (Swap):
o e l l h

Step 2 (Swap):
o l l e h
  ↑   ↑

Output:
"olleh"
```
