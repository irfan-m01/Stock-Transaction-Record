# 📌 Stock Portfolio Management System

This project demonstrates the implementation of a **Stock Portfolio Management System** using **MySQL Command Line Client**.

The system manages users, stocks, transactions (BUY/SELL), and portfolio holdings using relational database concepts such as **Primary Keys, Foreign Keys, UNIQUE constraints, and ENUM data types**.

The entire project is implemented using SQL commands executed through the MySQL Command Line Client.

---

## 🎯 Objectives

* To understand relational database design
* To implement primary and foreign key relationships
* To manage stock buy and sell transactions
* To maintain accurate portfolio records
* To practice SQL table creation and data manipulation

---

## 🛠 Tools Used

* MySQL Server
* MySQL Command Line Client
* SQL

---

## 🗂 Project Structure

### 1️⃣ Database Creation

A new database is created to store all tables related to the stock management system.

---

### 2️⃣ User Table

Stores user information.

* `User_id` – Primary Key (Auto Increment)
* `Name` – User’s full name
* `Email` – Unique email address
* `Phone` – Contact number

Each user is uniquely identified using `User_id`.

---

### 3️⃣ Stock Table

Stores stock details.

* `Stock_id` – Primary Key (Auto Increment)
* `Stock_name` – Name of the stock
* `Symbol` – Unique stock symbol
* `Price` – Current stock price

Each stock has a unique trading symbol.

---

### 4️⃣ Transactions Table

Stores buy and sell transaction records.

* `Transaction_id` – Primary Key (Auto Increment)
* `User_id` – Foreign Key (references User table)
* `Stock_id` – Foreign Key (references Stock table)
* `Transaction_type` – ENUM ('BUY', 'SELL')
* `Quantity` – Number of shares
* `Transaction_date` – Date of transaction

This table establishes relationships between users and stocks.

---

### 5️⃣ Portfolio Table

Stores the current stock balance of each user.

* `Portfolio_id` – Primary Key (Auto Increment)
* `User_id` – Foreign Key
* `Stock_id` – Foreign Key
* `Total_quantity` – Total shares owned

The `UNIQUE(User_id, Stock_id)` constraint ensures that a user can have only one portfolio entry per stock.

---

## 📥 Data Insertion

Sample data is inserted into:

* User Table
* Stock Table

This allows testing of relationships and transaction queries.

---

## 🔎 Data Retrieval Queries

The project includes:

* View all users
* View all stocks
* View all transactions
* Join Query (User + Stock + Transactions)

The JOIN query retrieves:

* User Name
* Stock Name
* Transaction Type
* Quantity
* Transaction Date

This demonstrates relational data linking and SQL JOIN operations.

---

## ▶ How to Execute

1. Install MySQL on your system.
2. Open MySQL Command Line Client.
3. Enter your MySQL root password to log in.
4. Create a new database.
5. Select the created database.
6. Execute the SQL table creation queries.
7. Insert sample data into the tables.
8. Run SELECT queries to verify records.
9. Execute JOIN queries to test relationships.
10. Use `SHOW TABLES;` to confirm successful table creation.

---

## 📚 Learning Outcomes

* Understanding relational database concepts
* Implementation of Primary and Foreign Keys
* Usage of UNIQUE and ENUM constraints
* Writing JOIN queries
* Managing transaction records
* Practical SQL implementation

---

## 👩‍💻 Author

**Irfan Kayum Maniyar**
SYIT – DBMS Mini Project
Academic Year: 2025–2026
