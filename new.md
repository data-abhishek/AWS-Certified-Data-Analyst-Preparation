
# From Zero to Database Hero: A Beginner's Journey into SQL  
**Unlocking the Power of Databases, One Query at a Time**

## 📋 Agenda
- What is Data?
- Managing Data
- DBMS Concepts
- Introduction to SQL
- SQL Hands-on
- Advanced SQL Concepts

## 🔍 What is Data?
Data refers to raw facts, figures, or statistics collected for analysis or processing. It can be:
- **Structured**: Data organized into tables (e.g., SQL databases).
- **Unstructured**: Data without a predefined format (e.g., images, videos, social posts).
- **Semi-structured**: Partially organized using formats like JSON or XML.

## 💽 What is a Database?
A database is an organized collection of data for easy access and management.
Examples:
- Student records in a school
- Bank customer account records

## 📂 Types of Databases
- **Relational Database**: Table-based with SQL (e.g., MySQL, SQL Server).
- **Non-Relational Database (NoSQL)**: Document, key-value, or graph-based models.
- **Distributed Database**
- **Object-Oriented Database**
- **Hierarchical Database**

## ⚖️ Relational vs. Non-Relational Databases
- **Relational**: Uses tables, supports joins, uses SQL, highly structured.
- **Non-Relational**: More flexible schema, supports unstructured data, scalable.

## 🕰️ History of Databases
- **Flat files** used before databases.
- **1970**: Relational model introduced by Edgar F. Codd.
- **IBM System R**: First RDBMS implementation.
- **SQL** became standard in late 1970s.

## 🧱 Disadvantages of File-Based Systems
- No structure or relationship support
- Redundant and inconsistent data
- Manual querying and updates
- Poor security and recovery

## 🧠 What is DBMS?
A **Database Management System (DBMS)** is software for creating and managing databases.

### DBMS Features:
- **DDL (Data Definition Language)**: `CREATE`, `ALTER`, `DROP`
- **DML (Data Manipulation Language)**: `INSERT`, `UPDATE`, `DELETE`, `SELECT`
- **Security**: Role-based access
- **Integrity**: Constraints, keys, relationships

## 💡 SQL - Structured Query Language
Used to manage and manipulate relational databases.

### SQL Subsets:
- **DDL**: `CREATE`, `ALTER`, `DROP`
- **DML**: `SELECT`, `INSERT`, `UPDATE`, `DELETE`

## 🔑 Types of Keys in SQL
- **Primary Key**: Uniquely identifies each row
- **Unique Key**: Ensures column values are distinct
- **Foreign Key**: Links one table to another

## 🧾 Data Types in SQL
- `INT`: Whole numbers
- `FLOAT`: Decimal values
- `VARCHAR(n)`: Variable-length strings
- `DATETIME`: Date and time values

## 🛠️ Software for Hands-on
- **SSMS (SQL Server Management Studio)**

## ✅ Constraints in SQL
Ensure data validity and consistency:
- `NOT NULL`, `UNIQUE`, `PRIMARY KEY`, `FOREIGN KEY`, `CHECK`, `DEFAULT`

## 🧪 SQL Lab Examples
```sql
CREATE DATABASE Projectdb;

CREATE TABLE table_name (
  col_1 INT,
  col_2 VARCHAR(100),
  col_3 VARCHAR(50)
);

INSERT INTO table_name VALUES (1, 'string1', 'string2');

DROP TABLE table_name;

DROP DATABASE Projectdb;
```

## 📜 Clauses in SQL
```sql
SELECT column1, column2 FROM table_name;
FROM table_name;
WHERE Age >= 18;
GROUP BY column;
HAVING COUNT(*) > 5;
ORDER BY column ASC|DESC;
SELECT * FROM orders LIMIT 5; -- MySQL/PostgreSQL
SELECT TOP 5 * FROM orders; -- SQL Server
```

## 🔢 Operators in SQL
- **Arithmetic**: `+`, `-`, `*`, `/`
- **Comparison**: `=`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical**: `AND`, `OR`, `NOT`

## 🧩 CASE Statement in SQL
```sql
SELECT emp_id, salary,
  CASE 
    WHEN salary > 100000 THEN 'High'
    WHEN salary BETWEEN 50000 AND 100000 THEN 'Medium'
    ELSE 'Low'
  END AS Salary_Level
FROM employees;
```

## 📘 Indexes in SQL
```sql
CREATE INDEX IX_EmpID ON Sudish_Info (Emp_Id);
```

**Benefits:**
- Faster queries
- Enhances filtering, sorting, and joining
- Supports large datasets

## 📊 Aggregate Functions
| Function | Description                | Example       |
|----------|----------------------------|---------------|
| `COUNT()` | Number of records          | `COUNT(*)`    |
| `SUM()`   | Total of numeric column    | `SUM(Salary)` |
| `AVG()`   | Average of values          | `AVG(Age)`    |
| `MIN()`   | Smallest value             | `MIN(Salary)` |
| `MAX()`   | Largest value              | `MAX(Salary)` |

## 🔗 JOINS in SQL
### INNER JOIN
```sql
SELECT t1.name, t2.dept_name
FROM table1 t1
INNER JOIN table2 t2 ON t1.dept_id = t2.dept_id;
```

### LEFT JOIN
```sql
SELECT t1.name, t2.dept_name
FROM table1 t1
LEFT JOIN table2 t2 ON t1.dept_id = t2.dept_id;
```

### RIGHT JOIN
```sql
SELECT t1.name, t2.dept_name
FROM table1 t1
RIGHT JOIN table2 t2 ON t1.dept_id = t2.dept_id;
```

### FULL JOIN
```sql
SELECT *
FROM table1
FULL JOIN table2 ON table1.id = table2.id;
```

## 🎓 Bonus Resources
- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)
- [LeetCode SQL Practice](https://leetcode.com/studyplan/top-sql-50/)
- [HackerRank SQL Challenges](https://www.hackerrank.com/domains/sql)

## 🙋 Any Questions?
**Thank You!**  
*Presented by Abhishek Anand*
