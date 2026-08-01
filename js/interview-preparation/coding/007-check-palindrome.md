# Check Palindrome

🎯 Pattern
Two Pointers

💡 Insight
Compare the first and last characters.
If they are equal, move both pointers toward the center.
If any pair is different, it's not a palindrome.

🧠 Memory
Compare Ends → Move Inside

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function isPalindrome(str) {
  let left = 0;
  let right = str.length - 1;

  while (left < right) {
    if (str[left] !== str[right]) {
      return false;
    }

    left++;
    right--;
  }

  return true;
}
```

🧪 Example

```text
Input:
"madam"

Initial:
m a d a m
↑       ↑

Step 1:
m === m ✅

 a d a
 ↑   ↑

Step 2:
a === a ✅

  d
  ↑

Pointers meet.

Output:
true
```
