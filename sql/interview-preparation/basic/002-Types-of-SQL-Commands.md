# 📚 What are the Different Types of SQL Commands?

## 📖 Simple English Explanation

SQL commands are instructions that tell the database what to do. They are grouped into **5 types** based on their purpose. Some commands create database objects, some modify data, some retrieve data, some control user permissions, and some manage transactions.

There are **5 types of SQL commands**:

1. **DDL (Data Definition Language)** → Defines the database structure.
2. **DML (Data Manipulation Language)** → Inserts, updates, and deletes data.
3. **DQL (Data Query Language)** → Retrieves data.
4. **DCL (Data Control Language)** → Controls user permissions.
5. **TCL (Transaction Control Language)** → Manages transactions.

---

## 🤔 Why is it Needed?

- To organize different database operations into categories.
- Makes SQL easier to learn and use.
- Helps manage database structure, data, security, and transactions separately.
- Without these command types, database operations would become confusing.

---

## 🌊 Flow

```text
Need to Create Table?
        ↓
      DDL
        ↓
Need to Insert/Update/Delete Data?
        ↓
      DML
        ↓
Need to Read Data?
        ↓
      DQL
        ↓
Need to Give Permissions?
        ↓
      DCL
        ↓
Need to Save/Rollback Changes?
        ↓
      TCL
```

---

## ✍️ Syntax

```sql
-- DDL
CREATE TABLE Employees (
    id INT,
    name VARCHAR(50)
);

-- DML
INSERT INTO Employees VALUES (1, 'John');

-- DQL
SELECT * FROM Employees;

-- DCL
GRANT SELECT ON Employees TO user1;

-- TCL
COMMIT;
```

---

## 💻 Example

```sql
-- Create a table (DDL)
CREATE TABLE Students (
    id INT,
    name VARCHAR(50)
);

-- Insert data (DML)
INSERT INTO Students VALUES (1, 'Rahul');

-- Retrieve data (DQL)
SELECT * FROM Students;

-- Save changes (TCL)
COMMIT;
```

---

## 🎤 Interview Answer (30 Seconds)

SQL commands are divided into **five types** based on their purpose. **DDL** is used to create and modify database objects, **DML** is used to insert, update, and delete data, **DQL** is used to retrieve data using the `SELECT` statement, **DCL** is used to control user permissions with commands like `GRANT` and `REVOKE`, and **TCL** is used to manage transactions using `COMMIT`, `ROLLBACK`, and `SAVEPOINT`.

---

## 🧠 Memory Trick

Remember:

**"Define → Modify → Query → Control → Transaction"**

or simply:

**DDL → DML → DQL → DCL → TCL**

**Mnemonic:** **"Don't Make Questions Confuse Teachers"**

- **D**on't → **DDL**
- **M**ake → **DML**
- **Q**uestions → **DQL**
- **C**onfuse → **DCL**
- **T**eachers → **TCL**

---

## ⭐ Keywords

- DDL (Create Structure)
- DML (Modify Data)
- DQL (Read Data)
- DCL (Permissions)
- TCL (Transactions)
- CREATE
- INSERT
- SELECT
- COMMIT

```

```
