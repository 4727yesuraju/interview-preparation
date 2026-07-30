# 📚 What is the Prototype Chain?

## 📖 Simple English Explanation

The **Prototype Chain** is the sequence JavaScript follows to **find a property or method**.

When you access a property or method:

1. JavaScript first checks the **current object**.
2. If it is **not found**, it checks the object's **prototype**.
3. If it is still **not found**, it checks the **next prototype**.
4. This continues until it reaches **`null`**.

> **Simple Definition:**
>
> **The Prototype Chain is JavaScript's process of searching for a property or method through an object's prototypes until it is found or `null` is reached.**

---

## 🤔 Why is it Needed?

- Reuse methods without copying them.
- Save memory by sharing methods.
- Enable inheritance between objects.
- Make JavaScript's object system work.

---

## 🌊 Flow

```text
Access dog.speak()
        │
        ▼
Is speak() in dog?
        │
   ┌────┴────┐
   │         │
 Yes         No
   │         │
   ▼         ▼
 Return   Check Prototype
               │
               ▼
        Is speak() Found?
               │
          ┌────┴────┐
          │         │
         Yes        No
          │         │
          ▼         ▼
      Return    Next Prototype
                    │
                    ▼
              Object.prototype
                    │
                    ▼
                  null
```

---

## ✍️ Syntax

### Create a Prototype Relationship

```javascript
const parent = {
  greet() {
    console.log("Hello");
  },
};

const child = Object.create(parent);
```

---

## 💻 Example

### Example 1: Prototype Chain

```javascript
const animal = {
  speak() {
    console.log("Animal speaks");
  },
};

const dog = Object.create(animal);

dog.speak();
```

**Output**

```text
Animal speaks
```

**How JavaScript Finds `speak()`**

```text
dog
 │
 ▼
Not Found
 │
 ▼
animal
 │
 ▼
Found ✅
```

---

### Example 2: Multiple Levels

```javascript
const grandParent = {
  country: "India",
};

const parent = Object.create(grandParent);

const child = Object.create(parent);

console.log(child.country);
```

**Output**

```text
India
```

**Prototype Chain**

```text
child
 │
 ▼
parent
 │
 ▼
grandParent
 │
 ▼
Object.prototype
 │
 ▼
null
```

---

### Example 3: Method from `Object.prototype`

```javascript
const user = {
  name: "John",
};

console.log(user.toString());
```

**Output**

```text
[object Object]
```

`toString()` is **not** inside `user`.

JavaScript finds it in:

```text
user
 │
 ▼
Object.prototype
 │
 ▼
toString() ✅
```

---

## 📋 Property Lookup Order

```text
Current Object
      │
      ▼
Prototype
      │
      ▼
Next Prototype
      │
      ▼
Object.prototype
      │
      ▼
null
```

---

## 📋 Real-World Uses

| Example            | Why?                          |
| ------------------ | ----------------------------- |
| `array.map()`      | Comes from `Array.prototype`  |
| `array.filter()`   | Comes from `Array.prototype`  |
| `toString()`       | Comes from `Object.prototype` |
| `hasOwnProperty()` | Comes from `Object.prototype` |

---

## 🎤 Interview Answer (30 Seconds)

The Prototype Chain is JavaScript's mechanism for looking up properties and methods. When a property isn't found on the current object, JavaScript searches its prototype, then the prototype's prototype, and continues until it reaches `Object.prototype` or `null`. This enables inheritance, code reuse, and shared methods.

---

## 🧠 Memory Trick

```text
Object
  │
Not Found
  │
  ▼
Prototype
  │
Not Found
  │
  ▼
Prototype
  │
Not Found
  │
  ▼
Object.prototype
  │
  ▼
null
```

Easy Rule:

> **Own Object → Prototype → Prototype → Object.prototype → null**

---

## ⭐ Keywords

- Prototype Chain
- Prototype
- Object.prototype
- Property Lookup
- Inheritance
- Object.create()
- Code Reuse
- null
