# Count Character Frequency

🎯 Pattern
Hash Map (Object)

💡 Insight
Loop through each character.
Store the character as a key and increment its count.

🧠 Memory
Character → Count++

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function countCharacterFrequency(str) {
  const frequency = {};

  for (const char of str) {
    frequency[char] = (frequency[char] || 0) + 1;
  }

  return frequency;
}
```

🧪 Example

```text
Input:
"hello"

Initial:
{}

Step 1:
h → { h: 1 }

Step 2:
e → { h: 1, e: 1 }

Step 3:
l → { h: 1, e: 1, l: 1 }

Step 4:
l → { h: 1, e: 1, l: 2 }

Step 5:
o → { h: 1, e: 1, l: 2, o: 1 }

Output:
{
  h: 1,
  e: 1,
  l: 2,
  o: 1
}
```
