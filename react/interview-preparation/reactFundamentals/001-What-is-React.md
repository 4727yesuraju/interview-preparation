# 📚 What Is React?

---

# 1️⃣ 📖 What Is It?

- **React is a JavaScript library used to build user interfaces (UI).**
- It helps developers create fast, interactive, and reusable web applications.
- Instead of updating the entire webpage, React updates only the parts that change, making applications faster.

**Simple English:**

Think of React like **LEGO blocks**.

- Each block is called a **Component**.
- You build small pieces (Button, Navbar, Card, Footer) and combine them to create a complete website.
- Instead of writing everything from scratch, you reuse these components wherever needed.

---

# 2️⃣ 🤔 Why Is It Needed?

### What problem does it solve?

Before React:

- Developers used plain JavaScript to update the webpage.
- As applications became larger, managing the UI became difficult.
- A small change often required updating many parts of the code.

React solves this by:

- Breaking the UI into reusable components.
- Automatically updating only the changed parts of the page.
- Making code easier to write, maintain, and reuse.

### Why was it introduced?

React was introduced to make building **large, dynamic, and interactive web applications** easier.

### What happens if we don't use it?

Without React:

- More manual DOM manipulation.
- More repetitive code.
- Harder to maintain large projects.
- Higher chance of bugs.

---

# 3️⃣ 🌍 Where Is It Used?

### Real-world use cases

- Social media websites
- E-commerce websites
- Dashboards
- Admin panels
- Chat applications
- Banking applications

### Which companies/products use it?

- Facebook
- Instagram
- Netflix
- WhatsApp Web
- Airbnb
- Uber

### When should we use it?

Use React when:

- Building Single Page Applications (SPA)
- Creating reusable UI components
- Building dynamic and interactive websites
- Working on medium or large applications

---

# 4️⃣ ⚙️ How Does It Work?

React builds the UI using **Components**.

When data changes:

1. React creates a new Virtual DOM.
2. React compares it with the previous Virtual DOM.
3. React finds only the changed elements.
4. React updates only those parts in the real browser DOM.

```
User Action
     ↓
State Changes
     ↓
React Creates Virtual DOM
     ↓
Compares with Previous Virtual DOM
     ↓
Finds Differences
     ↓
Updates Only Changed Parts
     ↓
Fast UI Update
```

---

# 5️⃣ ✍️ Syntax (If Applicable)

```jsx
function App() {
  return <h1>Hello React!</h1>;
}

export default App;
```

---

# 6️⃣ 💻 Examples

### Basic Example

```jsx
function App() {
  return <h1>Welcome to React</h1>;
}
```

### Intermediate Example

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return <Welcome name="Yesu" />;
}
```

### Real-world Example

```jsx
function ProductCard({ product }) {
  return (
    <div>
      <h2>{product.name}</h2>
      <p>₹{product.price}</p>
    </div>
  );
}

function App() {
  const product = {
    name: "Laptop",
    price: 65000,
  };

  return <ProductCard product={product} />;
}
```

---

# 7️⃣ 👍 Advantages

- Reusable Components
- Faster UI updates using Virtual DOM
- Easy to maintain
- Large community support
- Rich ecosystem of libraries
- Better code organization
- Easy to build large applications

---

# 8️⃣ 👎 Limitations

- Only handles the UI layer
- Requires additional libraries for routing and state management
- JSX may feel unusual for beginners
- React changes frequently, so developers need to keep learning

---

# 9️⃣ 🔄 Comparison

| React                 | Vs  | Plain JavaScript              |
| --------------------- | --- | ----------------------------- |
| Component-based       |     | Mostly manual coding          |
| Uses Virtual DOM      |     | Uses Real DOM directly        |
| Reusable components   |     | More repetitive code          |
| Easier for large apps |     | Harder to maintain large apps |
| Automatic UI updates  |     | Manual DOM updates            |

---

# 🔟 💡 Best Practices

- Build small, reusable components.
- Keep components focused on one responsibility.
- Use meaningful component names.
- Pass data using props.
- Manage data using state when needed.

---

# 1️⃣1️⃣ ⚠️ Common Mistakes

- Creating very large components.
- Mutating state directly.
- Using index as a key in lists unnecessarily.
- Mixing too much business logic inside UI components.

---

# 1️⃣2️⃣ 🚀 Performance Tips (If Applicable)

- Split the UI into reusable components.
- Avoid unnecessary re-renders.
- Use `React.memo`, `useMemo`, and `useCallback` only when needed.
- Lazy load large components using `React.lazy()`.

---

# 1️⃣3️⃣ 🏢 Real Interview Scenario

Example:

"Suppose you're building an e-commerce website."

The page has:

- Navbar
- Product List
- Product Card
- Cart
- Footer

In React, each of these is built as a separate component. If a user adds a product to the cart, React updates only the cart section instead of reloading the entire page. This makes the application faster and easier to maintain.

---

# 1️⃣4️⃣ 🧠 Interview Explanation (30–60 Seconds)

"React is an open-source JavaScript library used to build user interfaces. It follows a component-based architecture, where the UI is divided into reusable components. React uses a Virtual DOM to compare changes and updates only the necessary parts of the real DOM, which improves performance. It is widely used for building fast, scalable, and maintainable Single Page Applications."

---

# 1️⃣5️⃣ ❓ Common Interview Questions

## Basic

- What is React?
- Why is React called a library and not a framework?
- What are the main features of React?

## Intermediate

- How does React improve performance?
- What is the Virtual DOM?
- Why are components reusable?

## Advanced

- Explain React's rendering process.
- How does React update the DOM efficiently?
- How does React differ from Angular or Vue?

---

# 1️⃣6️⃣ 🎯 Interview Follow-up Questions

```
What is React?
      ↓
Why is React a library?
      ↓
What is a Component?
      ↓
What is Virtual DOM?
      ↓
How does Reconciliation work?
      ↓
How does React improve performance?
```

---

# 1️⃣7️⃣ 📝 Practice Exercises

## Easy

- Create a React application.
- Display "Hello React".
- Create a Header component.

## Medium

- Create a Product Card component.
- Pass data using props.
- Display a list of products.

## Hard

- Build a Todo application.
- Build a Shopping Cart.
- Build a Dashboard using reusable components.

---

# 1️⃣8️⃣ 🧩 Related Topics

Learn these next:

- JSX
- Components
- Props
- State
- Virtual DOM
- Reconciliation
- React Rendering
- Hooks
- React Router

---

# 1️⃣9️⃣ 📌 Key Takeaways

- ⭐ React is a JavaScript library for building user interfaces.
- ⭐ It follows a component-based architecture.
- ⭐ Components are reusable.
- ⭐ React uses the Virtual DOM for faster updates.
- ⭐ It is widely used to build modern Single Page Applications (SPAs).

---

# 2️⃣0️⃣ 🔁 Revision Summary

In one minute, you should be able to answer:

- ✅ What is React?
- ✅ Why is it needed?
- ✅ Where is it used?
- ✅ How does it work?
- ✅ Basic syntax
- ✅ Component example
- ✅ Advantages
- ✅ Limitations
- ✅ React vs Plain JavaScript
- ✅ Best practices
- ✅ Common mistakes
- ✅ Interview answer
