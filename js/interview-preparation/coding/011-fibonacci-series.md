# Fibonacci Series

🎯 Pattern
Iteration

💡 Insight
Start with the first two numbers (0 and 1).
Each next number is the sum of the previous two numbers.

🧠 Memory
Next = Previous + Current

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function fibonacci(n) {
  let first = 0;
  let second = 1;

  for (let i = 0; i < n; i++) {
    console.log(first);

    let next = first + second;
    first = second;
    second = next;
  }
}
```

🧪 Example

```text
Input:
7

Initial:
first = 0
second = 1

Step 1:
Print 0
Next = 0 + 1 = 1

Step 2:
Print 1
Next = 1 + 1 = 2

Step 3:
Print 1
Next = 1 + 2 = 3

Step 4:
Print 2
Next = 2 + 3 = 5

Step 5:
Print 3
Next = 3 + 5 = 8

Step 6:
Print 5
Next = 5 + 8 = 13

Step 7:
Print 8

Output:
0 1 1 2 3 5 8
```
