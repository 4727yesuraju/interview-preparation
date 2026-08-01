# Deep Clone an Object

🎯 Pattern
Recursion

💡 Insight
Create a completely new object.
Copy nested objects recursively so changes in the clone don't affect the original.

🧠 Memory
New Object → Copy Values → Go Deeper

⏱ Complexity
Time: O(n)
Space: O(n)

💻 Code

```js
function deepClone(obj) {
  if (obj === null || typeof obj !== "object") {
    return obj;
  }

  const clone = Array.isArray(obj) ? [] : {};

  for (const key in obj) {
    clone[key] = deepClone(obj[key]);
  }

  return clone;
}
```

🧪 Example

```text
Input:

const original = {
  name: "John",
  address: {
    city: "Chennai"
  }
};


Step 1:
Create new empty object

clone = {}


Step 2:
Copy primitive value

name → "John"


Step 3:
Find nested object

address → Go deeper


Step 4:
Create new address object

{
  city: "Chennai"
}


Output:

clone = {
  name: "John",
  address: {
    city: "Chennai"
  }
}


Change:

clone.address.city = "Delhi"


Original remains:

{
  name: "John",
  address: {
    city: "Chennai"
  }
}
```
