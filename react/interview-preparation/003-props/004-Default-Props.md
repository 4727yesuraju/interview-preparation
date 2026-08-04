# Default Props

## 📖 Simple English Explanation

### What is it?

**Default Props** are **backup values** for props.

If the **parent component does not pass a prop**, React uses the **default value** instead.

Think like this:

> "If no value comes from the parent, use this value."

---

### Why do we need it?

Suppose your component expects a `name`.

If the parent forgets to send `name`, then:

```jsx
<Greeting />
```

Inside the component:

```jsx
props.name; // undefined
```

Output:

```text
Hello, undefined
```

This doesn't look good.

So we provide a **default value**.

Now if `name` is missing,

React automatically uses:

```text
Hello, Guest
```

---

## 🌊 Flow

```text
Parent Component
        ↓
Does it pass "name"?
        ↓
     Yes         No
      ↓           ↓
Use "Yesu"   Use "Guest"
      ↓           ↓
Display Greeting
```

---

## ✍️ Syntax

### ✅ Modern React (Recommended)

```jsx
function Greeting({ name = "Guest" }) {
  return <h1>Hello {name}</h1>;
}
```

Here,

```jsx
name = "Guest";
```

means

> "If `name` is not passed, use `"Guest"`."

This is called a **default parameter value**.

---

### Older React (defaultProps)

Before React introduced Hooks and modern JavaScript features, developers wrote:

```jsx
function Greeting(props) {
  return <h1>Hello {props.name}</h1>;
}

Greeting.defaultProps = {
  name: "Guest",
};
```

Here,

```jsx
Greeting.defaultProps;
```

means

> "If no `name` prop is passed, use `"Guest"`."

This is called **defaultProps**.

Today, we usually **don't write this for Functional Components**.

---

## 💻 Example

### Without Default Value

```jsx
function Greeting({ name }) {
  return <h1>Hello {name}</h1>;
}

function App() {
  return <Greeting />;
}
```

Output

```text
Hello undefined
```

---

### With Default Parameter Value ✅

```jsx
function Greeting({ name = "Guest" }) {
  return <h1>Hello {name}</h1>;
}

function App() {
  return <Greeting />;
}
```

Output

```text
Hello Guest
```

---

### Passing a Value

```jsx
function Greeting({ name = "Guest" }) {
  return <h1>Hello {name}</h1>;
}

function App() {
  return <Greeting name="Yesu" />;
}
```

Output

```text
Hello Yesu
```

Notice:

Since `"Yesu"` is passed,

React **does not use** `"Guest"`.

---

## 🎤 Interview Explanation

**Default Props** are backup values used when a parent component does not pass a prop. In modern React, we use **JavaScript default parameter values**, such as `name = "Guest"`, instead of `defaultProps` for Functional Components. This prevents `undefined` values and makes components more reliable.

---

## 🧠 Memory Trick

Think of ordering food.

🍔 You order a burger.

Restaurant asks:

> "Do you want a drink?"

If you don't choose one,

they automatically give you **Water**.

```text
Your Choice?
      ↓
Yes  → Use Your Choice
No   → Use Default
```

**Default Props = Backup Value**
