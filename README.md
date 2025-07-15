# 📘 SQL - Structured Query Language

SQL is a standard language used to communicate with relational databases.  
It helps you **Create**, **Read**, **Update**, and **Delete** data effectively.

---

## ❓ What is a Query?

A **query** is a request for data or information from a database.  
It allows users to perform operations such as retrieving, inserting, updating, or deleting data.

---

## 🔁 CRUD Operations in SQL

| Operation | Meaning        | SQL Command Used |
|-----------|----------------|------------------|
| **C**     | Create         | `CREATE`         |
| **R**     | Read / Retrieve| `SELECT`         |
| **U**     | Update         | `UPDATE`         |
| **D**     | Delete         | `DELETE`         |

---

✅ These operations form the foundation of database management.

📌 You'll practice all of these commands in real-world queries throughout this repository.

# 📝 Order of Writing SQL Commands (Syntax Order)

## 📖 Definition:
The order of writing SQL commands refers to the **syntax structure** you follow when writing SQL queries. It tells SQL how to understand your request.

Even if SQL **executes** commands in a different order internally, you must **write** them in the proper order to avoid errors.

---

## 🧱 Syntax Structure (Write in this order):

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition
GROUP BY column
HAVING condition
ORDER BY column [ASC|DESC]
LIMIT number;
SELECT department, COUNT(*) AS employee_count
FROM employees
WHERE status = 'Active'
GROUP BY department
HAVING COUNT(*) > 10
ORDER BY employee_count DESC
LIMIT 5;
 In this example:

SELECT: Chooses department & total employees

FROM: The table used is employees

WHERE: Filters only active employees

GROUP BY: Groups data by department

HAVING: Filters departments with more than 10 employees

ORDER BY: Sorts result from highest to lowest count

LIMIT: Shows only top 5 departments
# 🛠️ Order of Writing SQL Commands (Syntax Order)

When writing a SQL query, follow this sequence:

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition
GROUP BY column
HAVING condition
ORDER BY column [ASC|DESC]
LIMIT number;
SELECT department, COUNT(*) AS total_employees
FROM employees
WHERE active = 1
GROUP BY department
HAVING COUNT(*) > 5
ORDER BY total_employees DESC
LIMIT 3;
🧠 In the above query:

First, SQL looks FROM employees

Filters rows with WHERE active = 1

Groups by department

Filters groups with HAVING

Then SELECTs and ORDERs

Finally LIMITs the result
