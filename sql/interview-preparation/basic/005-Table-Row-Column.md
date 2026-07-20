# 📚 What is a Table?

## 📖 Simple English Explanation

A **Table** is a collection of related data organized into **rows and columns**. Each table stores information about one specific thing, such as Employees, Students, or Products. A database can contain multiple tables.

---

## 🤔 Why is it Needed?

- To organize data in a structured format.
- Makes storing, searching, and updating data easier.
- Without tables, all data would be mixed together and difficult to manage.

---

## 🌊 Flow

```text
Database
     ↓
Table
     ↓
Rows
     ↓
Columns
```

---

## ✍️ Syntax

```sql
CREATE TABLE Employees (
    id INT,
    name VARCHAR(50),
    salary DECIMAL(10,2)
);
```

---

## 💻 Example

```text
Employees Table

+----+--------+--------+
| ID | Name   | Salary |
+----+--------+--------+
| 1  | John   | 50000  |
| 2  | Alice  | 60000  |
+----+--------+--------+
```

---

## 🎤 Interview Answer (30 Seconds)

A table is a database object that stores related data in the form of rows and columns. Each table represents one entity, such as Employees or Students. Tables help organize data efficiently, making it easy to store, retrieve, update, and delete records.

---

## 🧠 Memory Trick

Think of a **Table as an Excel Sheet** 📊.

- Database = Folder 📁
- Table = Excel Sheet 📄

---

## ⭐ Keywords

- Table
- Rows
- Columns
- Records
- Database
- Structured Data
