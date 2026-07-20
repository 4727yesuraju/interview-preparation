# 📚 Drizzle E-Commerce Database Schema

## 📖 Simple English Explanation

This file defines the **database schema** of an e-commerce application using **Drizzle ORM**. It describes what tables exist, what data each table stores, and how the tables are related to each other. Instead of creating tables manually in PostgreSQL, we define everything in TypeScript, and Drizzle generates the SQL automatically.

---

## 🤔 Why is it Needed?

- Defines the structure of the database.
- Keeps the database and application code in sync.
- Maintains relationships between tables.
- Ensures data integrity using primary keys, foreign keys, and constraints.
- Without this schema, the application wouldn't know how to store or retrieve data.

---

## 🌊 Flow

```text
Business Requirements
        ↓
Design Database Tables
        ↓
Define Tables using Drizzle ORM
        ↓
Define Relationships
        ↓
Run Drizzle Migration/Push
        ↓
Tables Created in PostgreSQL
        ↓
Application Performs CRUD Operations
```

---

## ✍️ Overall Structure

```text
Schema File
      │
      ├── Type Definitions
      │
      ├── Users Table
      │
      ├── Products Table
      │
      ├── Checkout Sessions Table
      │
      ├── Orders Table
      │
      ├── Order Items Table
      │
      └── Table Relationships
```

---

## 💻 Example (Real World)

Imagine an online shopping application.

```text
User
 ↓
Login
 ↓
Browse Products
 ↓
Add Products to Checkout
 ↓
Complete Payment
 ↓
Create Order
 ↓
Store Order Items
```

Each step stores data in a different table.

| Feature                  | Table             |
| ------------------------ | ----------------- |
| User Account             | users             |
| Product Catalog          | products          |
| Shopping Cart / Checkout | checkout_sessions |
| Orders                   | orders            |
| Purchased Products       | order_items       |

---

# 🌊 Complete Database Flow

```text
User Registers
       │
       ▼
users Table
       │
       ▼
User Browses Products
       │
       ▼
products Table
       │
       ▼
User Starts Checkout
       │
       ▼
checkout_sessions Table
       │
       ▼
Payment Successful
       │
       ▼
orders Table
       │
       ▼
Purchased Products
       │
       ▼
order_items Table
```

---

# 📚 Table Relationships

```text
               Users
                 │
          One User
                 │
           Many Orders
                 │
                 ▼
              Orders
                 │
          One Order
                 │
       Many Order Items
                 │
                 ▼
           Order Items
                 │
           One Product
                 │
                 ▼
             Products
```

Relationship Summary

```
User (1)
   │
   ├──────────────► Orders (Many)
                         │
                         ├────────────► Order Items (Many)
                                               │
                                               └────────► Product (1)
```

---

# 📚 Business Logic

## 1. Users

Stores customer information.

Examples:

- Login
- Email
- Role
- Account Details

---

## 2. Products

Stores products available for purchase.

Examples:

- Shoes
- Laptop
- Mobile
- Price
- Image

---

## 3. Checkout Sessions

Stores temporary checkout information before payment.

Example:

```text
Nike Shoes
2 Qty

iPhone
1 Qty
```

If payment succeeds →

Create an Order.

---

## 4. Orders

Stores completed purchases.

Example:

```text
Order #1001

Status:
Paid

Customer:
John
```

---

## 5. Order Items

Stores individual products inside an order.

Example

```text
Order #1001

Nike Shoes
Qty = 2

T-shirt
Qty = 1
```

Instead of storing everything in one row, each product becomes an order item.

---

# 📚 Why Relationships?

Relationships prevent duplicate data.

Example

Instead of

```text
Order

Customer Name
Customer Email
Customer Address
```

We simply store

```text
userId
```

Then retrieve customer information from the **users** table.

This follows **Database Normalization**.

---

## 🎤 Interview Answer (30 Seconds)

"This file defines the complete database schema for an e-commerce application using Drizzle ORM. It creates tables like Users, Products, Checkout Sessions, Orders, and Order Items, and defines the relationships between them using primary keys and foreign keys. Drizzle uses this schema to generate SQL and create the database automatically. It keeps the application and database synchronized while ensuring data consistency and integrity."

---

## 🧠 Memory Trick

Think of an **Amazon Order**.

```text
Customer
    ↓
Products
    ↓
Checkout
    ↓
Order
    ↓
Order Items
```

Remember:

**UPCO**

- **U** → Users
- **P** → Products
- **C** → Checkout
- **O** → Orders

Every e-commerce database follows this flow.

---

## ⭐ Keywords

- Drizzle ORM
- Database Schema
- PostgreSQL
- Tables
- Primary Key
- Foreign Key
- Relations
- One-to-Many
- CRUD
- Migration
- Normalization
- Data Integrity
