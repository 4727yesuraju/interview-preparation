# 📚 What are Default Parameters?

## 📖 Simple English Explanation

**Default parameters** allow you to assign a **default value** to a function parameter.

If no argument (or `undefined`) is passed to the function, JavaScript uses the default value automatically.

---

## 🤔 Why is it Needed?

- Prevents parameters from becoming `undefined`.
- Reduces the need for extra `if` conditions.
- Makes functions easier to use and more reliable.

---

## 🌊 Flow

```text
Function Called
       │
       ▼
Argument Passed?
       │
  ┌────┴────┐
  │         │
 Yes       No
  │         │
  ▼         ▼
Use        Use Default
Argument   Parameter Value
```

---

## ✍️ Syntax

```javascript
function greet(name = "Guest") {
  console.log(`Hello ${name}`);
}
```

---

## 💻 Example

### Example 1: Without Argument

```javascript
function greet(name = "Guest") {
  console.log(`Hello ${name}`);
}

greet();
```

**Output**

```text
Hello Guest
```

---

### Example 2: With Argument

```javascript
function greet(name = "Guest") {
  console.log(`Hello ${name}`);
}

greet("John");
```

**Output**

```text
Hello John
```

---

### Example 3: Passing `undefined`

```javascript
function greet(name = "Guest") {
  console.log(`Hello ${name}`);
}

greet(undefined);
```

**Output**

```text
Hello Guest
```

---

## 🎤 Interview Answer (30 Seconds)

Default parameters are a feature introduced in **ES6** that allow you to assign default values to function parameters. If a function is called without an argument, or with `undefined`, JavaScript automatically uses the default value instead.

---

## 🧠 Memory Trick

```text
Argument Passed?
       │
 ┌─────┴─────┐
 │           │
Yes         No
 │           │
 ▼           ▼
Use         Default Value
Argument
```

Easy Rule:

> **No Argument → Default Value**

---

## ⭐ Keywords

- Default Parameters
- ES6
- Function Parameters
- Default Value
- `undefined`
- Function Arguments
