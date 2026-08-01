# Implement Debounce

🎯 Pattern
Closures + setTimeout

💡 Insight
Delay function execution until the user stops triggering the event.
Clear the previous timer and create a new timer every time.

🧠 Memory
Cancel Previous → Wait → Execute

⏱ Complexity
Time: O(1) per call
Space: O(1)

💻 Code

```js
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);

    timer = setTimeout(() => {
      fn.apply(this, args);
    }, delay);
  };
}
```

🧪 Example

```text
Input:

User types:
H

Start timer (500ms)


User types:
He

Clear old timer
Start new timer


User types:
Hel

Clear old timer
Start new timer


User stops typing...

After 500ms:

Execute function


Output:
Search API call happens once
```
