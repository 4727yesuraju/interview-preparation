# Implement Throttle

🎯 Pattern
Closures + Time Control

💡 Insight
Allow a function to execute only once within a fixed time interval.
Ignore extra calls until the waiting time is completed.

🧠 Memory
First Call → Wait → Ignore Extra Calls

⏱ Complexity
Time: O(1) per call
Space: O(1)

💻 Code

```js
function throttle(fn, delay) {
  let lastCall = 0;

  return function (...args) {
    const now = Date.now();

    if (now - lastCall >= delay) {
      lastCall = now;
      fn.apply(this, args);
    }
  };
}
```

🧪 Example

```text
Input:

User scrolls page continuously


0ms:
Scroll event
Execute function ✅


100ms:
Scroll event
Ignore ❌


200ms:
Scroll event
Ignore ❌


500ms:
Scroll event
Execute function ✅


Output:

Function runs once every delay period
```
