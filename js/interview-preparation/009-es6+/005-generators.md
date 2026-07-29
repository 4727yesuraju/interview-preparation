# 📚 What are Generators?

## 📖 Simple English Explanation

A **Generator** is a special type of function that **can pause and resume its execution**.

Unlike a normal function, which runs from start to finish in one go, a generator can return one value at a time and continue from where it stopped.

Generators are created using the `function*` syntax, and they use the `yield` keyword.

> **Simple Definition:**
>
> **A Generator is a function that can pause and resume, producing one value at a time.**

---

## 🤔 Why is it Needed?

- Generate values one by one.
- Handle large datasets efficiently.
- Create custom iterators.
- Pause and resume execution when needed.

---

## 🌊 Flow

```text
Call Generator
       │
       ▼
Start Function
       │
       ▼
yield 1
(Pause)
       │
next()
       ▼
yield 2
(Pause)
       │
next()
       ▼
yield 3
(Pause)
       │
next()
       ▼
Function Ends
```

---

## ✍️ Syntax

```javascript
function* generatorName() {
  yield value1;
  yield value2;
  yield value3;
}

const generator = generatorName();

generator.next();
```

---

## 💻 Example

### Example 1: Basic Generator

```javascript
function* numbers() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = numbers();

console.log(gen.next());
console.log(gen.next());
console.log(gen.next());
console.log(gen.next());
```

**Output**

```text
{ value: 1, done: false }
{ value: 2, done: false }
{ value: 3, done: false }
{ value: undefined, done: true }
```

---

### Example 2: Using `for...of`

```javascript
function* colors() {
  yield "Red";
  yield "Green";
  yield "Blue";
}

for (const color of colors()) {
  console.log(color);
}
```

**Output**

```text
Red
Green
Blue
```

---

### Example 3: Infinite Generator

```javascript
function* counter() {
  let i = 1;

  while (true) {
    yield i++;
  }
}

const gen = counter();

console.log(gen.next().value);
console.log(gen.next().value);
console.log(gen.next().value);
```

**Output**

```text
1
2
3
```

---

## 📋 Normal Function vs Generator

| Normal Function   | Generator                          |
| ----------------- | ---------------------------------- |
| Runs completely   | Can pause and resume               |
| Uses `return`     | Uses `yield`                       |
| Returns one value | Produces multiple values over time |
| Cannot resume     | Resumes from the last `yield`      |

---

## 🎤 Interview Answer (30 Seconds)

A generator is a special JavaScript function that can pause and resume its execution. It is created using `function*` and uses the `yield` keyword to return values one at a time. Each call to `next()` resumes execution from the previous `yield`. Generators are useful for creating iterators and processing large or infinite sequences efficiently.

---

## 🧠 Memory Trick

```text
Generator
    │
    ▼
yield 1
(Pause)
    │
next()
    ▼
yield 2
(Pause)
    │
next()
    ▼
yield 3
```

Easy Rule:

> **Generator = Pause → Resume → Pause → Resume**

---

## ⭐ Keywords

- Generator
- function\*
- yield
- next()
- Iterator
- Pause
- Resume
- for...of
