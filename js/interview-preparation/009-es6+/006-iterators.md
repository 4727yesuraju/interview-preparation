# 📚 What are Iterators?

## 📖 Simple English Explanation

An **Iterator** is an object that lets you **access one item at a time** from a collection (like an array, string, or generator).

Instead of returning all values at once, an iterator returns **one value each time you call `next()`**.

The `next()` method returns an object with two properties:

- `value` → The current value.
- `done` → `true` if there are no more values, otherwise `false`.

> **Simple Definition:**
>
> **An Iterator is an object that returns one value at a time using the `next()` method.**

---

## 🤔 Why is it Needed?

- Read values one by one.
- Process large collections efficiently.
- Control iteration manually.
- Used internally by `for...of`, generators, `Map`, `Set`, and more.

---

## 🌊 Flow

```text
Array
 │
 ▼
Iterator
 │
 ▼
next()
 │
 ▼
Value 1

next()
 │
 ▼
Value 2

next()
 │
 ▼
Value 3

next()
 │
 ▼
done: true
```

---

## ✍️ Syntax

```javascript
const iterator = collection[Symbol.iterator]();

iterator.next();
```

---

## 💻 Example

### Example 1: Array Iterator

```javascript
const fruits = ["Apple", "Mango", "Orange"];

const iterator = fruits[Symbol.iterator]();

console.log(iterator.next());
console.log(iterator.next());
console.log(iterator.next());
console.log(iterator.next());
```

**Output**

```text
{ value: "Apple", done: false }
{ value: "Mango", done: false }
{ value: "Orange", done: false }
{ value: undefined, done: true }
```

---

### Example 2: String Iterator

```javascript
const str = "Hi";

const iterator = str[Symbol.iterator]();

console.log(iterator.next());
console.log(iterator.next());
console.log(iterator.next());
```

**Output**

```text
{ value: "H", done: false }
{ value: "i", done: false }
{ value: undefined, done: true }
```

---

### Example 3: Iterator from a Generator

```javascript
function* numbers() {
  yield 1;
  yield 2;
  yield 3;
}

const iterator = numbers();

console.log(iterator.next());
console.log(iterator.next());
console.log(iterator.next());
```

**Output**

```text
{ value: 1, done: false }
{ value: 2, done: false }
{ value: 3, done: false }
```

---

## 📋 Iterator vs Iterable

| Iterator                        | Iterable                          |
| ------------------------------- | --------------------------------- |
| Has a `next()` method           | Can create an iterator            |
| Returns one value at a time     | Examples: Array, String, Map, Set |
| Keeps track of current position | Uses `Symbol.iterator`            |

---

## 🌍 Real-World Examples

| Iterable  | Iterator           |
| --------- | ------------------ |
| Array     | Array Iterator     |
| String    | String Iterator    |
| Map       | Map Iterator       |
| Set       | Set Iterator       |
| Generator | Generator Iterator |

---

## 🎤 Interview Answer (30 Seconds)

An iterator is an object that allows you to access elements of a collection one at a time. It provides a `next()` method, which returns an object containing the current `value` and a `done` flag. Iterators are used internally by `for...of` loops and are created from iterable objects such as arrays, strings, maps, sets, and generators.

---

## 🧠 Memory Trick

```text
Collection
    │
    ▼
Iterator
    │
next()
    ▼
Value 1

next()
    ▼
Value 2

next()
    ▼
done: true
```

Easy Rule:

> **Iterable = Can Create an Iterator**

> **Iterator = Gives One Value at a Time**

---

## ⭐ Keywords

- Iterator
- Iterable
- next()
- value
- done
- Symbol.iterator
- Generator
- for...of
