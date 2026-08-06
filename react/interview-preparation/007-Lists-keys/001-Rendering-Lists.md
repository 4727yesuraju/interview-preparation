# Rendering Lists

## 📖 Simple English Explanation

### What is it?

**Rendering Lists** means **displaying multiple items from an array** in React.

React commonly uses the **`map()`** method to convert each item in an array into a JSX element.

### Why do we need it?

- To display dynamic data.
- To avoid writing the same JSX repeatedly.
- To easily render data from APIs or databases.

---

## 🌊 Flow

```text
Array of Data
      ↓
Use map()
      ↓
Create JSX for Each Item
      ↓
React Displays the List
```

---

## ✍️ Syntax

```jsx
array.map((item) => <li>{item}</li>);
```

---

## 💻 Example

```jsx
function App() {
  const fruits = ["Apple", "Mango", "Orange"];

  return (
    <ul>
      {fruits.map((fruit) => (
        <li>{fruit}</li>
      ))}
    </ul>
  );
}
```

**Output**

```text
• Apple
• Mango
• Orange
```

---

## 🎤 Interview Explanation

Rendering Lists means **displaying multiple items from an array** in React. We usually use the **`map()`** method to loop through the array and return JSX for each item. React then renders all the generated elements on the screen.

---

## 🧠 Memory Trick

🖨️ **Think of a printer.**

```text
List of Items
      ↓
Printer (map())
      ↓
Print One by One
      ↓
Display All Items
```

**Remember:**

**Array → `map()` → JSX → UI**
