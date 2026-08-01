# Prime Number Check

🎯 Pattern
Loop + Math Optimization

💡 Insight
A prime number has only two factors: 1 and itself.
Check if any number from 2 to √n divides the number.
If divisible, it is not prime.

🧠 Memory
Divide → Find Factor → Not Prime

⏱ Complexity
Time: O(√n)
Space: O(1)

💻 Code

```js
function isPrime(n) {
  if (n <= 1) return false;

  for (let i = 2; i <= Math.sqrt(n); i++) {
    if (n % i === 0) {
      return false;
    }
  }

  return true;
}
```

🧪 Example

```text
Input:
29

Check factors:

√29 ≈ 5

Try dividing:

29 % 2 → Not divisible
29 % 3 → Not divisible
29 % 4 → Not divisible
29 % 5 → Not divisible

No factors found ✅

Output:
true
```
