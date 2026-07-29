# 📚 What is Garbage Collection?

## 📖 Simple English Explanation

**Garbage Collection (GC)** is an automatic memory management process in JavaScript.

When an object or variable is **no longer being used** (no references point to it), the JavaScript engine automatically **removes it from memory** to free up space.

> **Simple Definition:**
>
> **Garbage Collection automatically removes unused memory so your application uses less memory and avoids memory leaks.**

---

## 🤔 Why is it Needed?

- Frees unused memory automatically.
- Prevents memory from filling up.
- Reduces the chance of memory leaks.
- Developers don't need to manually free memory like in languages such as C or C++.

---

## 🌊 Flow

```text
Create Variable
       │
       ▼
Memory Allocated
       │
       ▼
Variable Used
       │
       ▼
Reference Removed
       │
       ▼
No References Left?
       │
   ┌───┴───┐
   ▼       ▼
 Yes       No
   │        │
   ▼        ▼
Garbage     Keep
Collector   in Memory
Removes It
```

---

## ✍️ Syntax

JavaScript does **not** provide a function like:

```javascript
free(memory); ❌
```

Garbage Collection happens **automatically**.

---

## 💻 Example

### Example 1: Variable Becomes Unused

```javascript
let user = {
  name: "John",
};

user = null;
```

**Flow**

```text
Create Object
      │
      ▼
user → Object

user = null
      │
      ▼
No References Left
      │
      ▼
Garbage Collector Removes Object
```

---

### Example 2: Unused Local Variable

```javascript
function test() {
  let message = "Hello";
}

test();
```

After `test()` finishes:

```text
message
   │
   ▼
No Longer Accessible
   │
   ▼
Garbage Collector Removes It
```

---

### Example 3: Still Referenced

```javascript
let person = {
  name: "Alice",
};

let anotherRef = person;

person = null;
```

```text
anotherRef ─────► Object
```

The object is **not removed**, because `anotherRef` still points to it.

---

## 📋 When Does Garbage Collection Remove Memory?

| Situation                                             | Garbage Collected? |
| ----------------------------------------------------- | ------------------ |
| Variable becomes `null` and no other references exist | ✅ Yes             |
| Function local variable after function ends           | ✅ Yes             |
| Object still has a reference                          | ❌ No              |
| Global variable still in use                          | ❌ No              |

---

## 🎤 Interview Answer (30 Seconds)

Garbage Collection is JavaScript's automatic memory management system. It identifies objects that are no longer reachable because nothing references them anymore and frees their memory automatically. This helps prevent memory leaks and allows developers to focus on writing code instead of manually managing memory.

---

## 🧠 Memory Trick

```text
Object Created
      │
      ▼
Memory Allocated
      │
      ▼
No References?
      │
      ▼
🗑️ Garbage Collector
      │
      ▼
Memory Freed
```

Easy Rule:

> **No References = Garbage Collector Removes It**

---

## ⭐ Keywords

- Garbage Collection
- GC
- Memory Management
- References
- Unused Objects
- Memory Leak
- Automatic Cleanup
- JavaScript Engine
