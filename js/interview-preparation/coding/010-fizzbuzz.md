# FizzBuzz

🎯 Pattern
Conditional Statements

💡 Insight
Check divisibility in the correct order.
First check 3 & 5 together, then 3, then 5.

🧠 Memory
15 → 3 → 5 → Number

⏱ Complexity
Time: O(n)
Space: O(1)

💻 Code

```js
function fizzBuzz(n) {
  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) {
      console.log("FizzBuzz");
    } else if (i % 3 === 0) {
      console.log("Fizz");
    } else if (i % 5 === 0) {
      console.log("Buzz");
    } else {
      console.log(i);
    }
  }
}
```

🧪 Example

```text
Input:
15

Output:
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```
