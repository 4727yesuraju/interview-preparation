# 📚 What is a Primary Key?

## 📖 Simple English Explanation

A **Primary Key (PK)** is a column (or combination of columns) that **uniquely identifies each row** in a table. A primary key **cannot contain duplicate values** and **cannot be NULL**. Every table should have one primary key to uniquely identify its records.

---

## 🤔 Why is it Needed?

- To uniquely identify each record in a table.
- To prevent duplicate records.
- To create relationships between tables using foreign keys.
- Without a primary key, it becomes difficult to identify or update a specific record.

---

## 🌊 Flow

```text
Create Table
      ↓
Choose Unique Column
      ↓
Set as Primary Key
      ↓
Each Row Gets a Unique ID
```

---

## ✍️ Syntax

```sql
CREATE TABLE Employees (
    id INT PRIMARY KEY,
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
| 3  | David  | 55000  |
+----+--------+--------+
```

✅ Valid:

- IDs: **1, 2, 3** (All unique)

❌ Invalid:

```text
+----+--------+
| ID | Name   |
+----+--------+
| 1  | John   |
| 1  | Alice  | ❌ Duplicate
|NULL| David  | ❌ NULL
+----+--------+
```

---

## 🎤 Interview Answer (30 Seconds)

A Primary Key is a column or combination of columns that uniquely identifies each row in a table. It does not allow duplicate values or NULL values. It ensures data integrity and is commonly used to create relationships between tables through foreign keys.

---

## 🧠 Memory Trick

Think of an **Aadhaar Number** 🆔.

- Every person has **one unique Aadhaar number**.
- No two people can have the same Aadhaar number.
- It cannot be empty.

Similarly,

- **Primary Key = Unique Identity of a Row**

**Shortcut:** **PK = Unique + Not NULL**

---

## ⭐ Keywords

- Primary Key
- Unique
- NOT NULL
- Record Identifier
- Data Integrity
- Foreign Key Reference
