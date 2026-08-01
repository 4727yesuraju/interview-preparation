# Check Anagram

🎯 Pattern
Hash Map (Frequency Counter)

💡 Insight
Count the frequency of each character in the first string.
Decrease the count using the second string.
If all counts become zero, the strings are anagrams.

🧠 Memory
Count → Reduce → Check Zero

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function isAnagram(str1, str2) {
  if (str1.length !== str2.length) return false;

  const count = {};

  for (const char of str1) {
    count[char] = (count[char] || 0) + 1;
  }

  for (const char of str2) {
    if (!count[char]) return false;
    count[char]--;
  }

  return true;
}
```

🧪 Example

```text
Input:
str1 = "listen"
str2 = "silent"

Step 1:
Count characters from "listen"

{
  l:1,
  i:1,
  s:1,
  t:1,
  e:1,
  n:1
}

Step 2:
Reduce counts using "silent"

s → 0
i → 0
l → 0
e → 0
n → 0
t → 0

All counts are 0 ✅

Output:
true
```
