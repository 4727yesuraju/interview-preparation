# 📚 What is Nullish Coalescing (`??`)?

## 📖 Simple English Explanation

The **Nullish Coalescing (`??`)** operator is used to provide a **default value** when the left-side value is **`null` or `undefined`**.

If the left-side value is **not** `null` or `undefined`, JavaScript returns that value.

---

## 🤔 Why is it Needed?

- Provides default values safely.
- Avoids replacing valid values like `0`, `false`, or `""`.
- Makes the code cleaner and easier to read.

---

## 🌊 Flow

```text
Left Value
     │
     ▼
Is it null or undefined?
     │
 ┌───┴────┐
 │        │
Yes       No
 │        │
 ▼        ▼
Return    Return
Right     Left
Value     Value
```

---

## ✍️ Syntax

```javascript
let result = value ?? defaultValue;
```

---

## 💻 Example

### Example 1: `null`

```javascript
let name = null;

console.log(name ?? "Guest");
```

**Output**

```text
Guest
```

---

### Example 2: `undefined`

```javascript
let age;

console.log(age ?? 18);
```

**Output**

```text
18
```

---

### Example 3: `0` and `false`

```javascript
console.log(0 ?? 100);
console.log(false ?? true);
console.log("" ?? "Default");
```

**Output**

```text
0
false

```

> `0`, `false`, and `""` are **valid values**, so `??` returns them instead of the default value.

---

## 🎤 Interview Answer (30 Seconds)

The **Nullish Coalescing (`??`)** operator returns the **right-side value only when the left-side value is `null` or `undefined`**. Otherwise, it returns the left-side value. It is commonly used to provide default values without replacing valid values like `0`, `false`, or an empty string.

---

## 🧠 Memory Trick

```text
Left Value
    │
    ▼
null / undefined ?
    │
 ┌──┴──┐
 │     │
Yes    No
 │     │
 ▼     ▼
Default Original
Value   Value
```

Easy Rule:

> **`??` = Use the default value only for `null` or `undefined`.**

---

## ⭐ Keywords

- Nullish Coalescing
- `??`
- ES2020
- Default Value
- `null`
- `undefined`
- Fallback Value
