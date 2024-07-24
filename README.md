## Database Management Systems (DBMS) and Relational Database Management Systems (RDBMS) 🌟

### Introduction 📚

A Database Management System (DBMS) is software that interacts with end-users, applications, and the database itself to capture and analyze data. A Relational Database Management System (RDBMS) is a type of DBMS that stores data in a structured format, using rows and columns. RDBMS systems, such as MySQL, PostgreSQL, and Oracle, support SQL (Structured Query Language) for managing data.

### Contents 📋

1. **Data Definition Language (DDL)**
   - CREATE 🛠️
   - ALTER ✏️
   - DROP 🗑️
   - TRUNCATE 🚮
2. **Data Query Language (DQL)**
   - SELECT 🔍
3. **Data Manipulation Language (DML)**
   - INSERT ➕
   - UPDATE ✏️
   - DELETE ➖
4. **Transaction Control Language (TCL)**
   - COMMIT 💾
   - ROLLBACK ⏪
   - SAVEPOINT 📍
5. **Examples**

### Data Definition Language (DDL) 🛠️

DDL statements are used to define, alter, and manage database schema.

#### CREATE 🛠️

Used to create databases, tables, indexes, views, etc.

```sql
-- Create a new database
CREATE DATABASE mydatabase;

-- Create a new table
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    department VARCHAR(50)
);
```

#### ALTER ✏️

Used to modify the structure of an existing database object.

```sql
-- Add a new column to an existing table
ALTER TABLE employees ADD salary DECIMAL(10, 2);

-- Modify the datatype of a column
ALTER TABLE employees MODIFY COLUMN age SMALLINT;
```

#### DROP 🗑️

Used to delete databases, tables, indexes, views, etc.

```sql
-- Drop a table
DROP TABLE employees;

-- Drop a database
DROP DATABASE mydatabase;
```

#### TRUNCATE 🚮

Used to delete all rows from a table without deleting the table itself.

```sql
-- Truncate a table
TRUNCATE TABLE employees;
```

### Data Query Language (DQL) 🔍

DQL is used to query the database and retrieve data.

#### SELECT 🔍

Used to retrieve data from one or more tables.

```sql
-- Select specific columns
SELECT name, department FROM employees WHERE age > 30;

-- Select all columns
SELECT * FROM employees;
```

### Data Manipulation Language (DML) ➕

DML statements are used for managing data within schema objects.

#### INSERT ➕

Used to insert new records into a table.

```sql
-- Insert a single row
INSERT INTO employees (id, name, age, department) VALUES (1, 'John Doe', 30, 'HR');

-- Insert multiple rows
INSERT INTO employees (id, name, age, department) VALUES
(2, 'Jane Smith', 25, 'Finance'),
(3, 'Mike Brown', 35, 'IT');
```

#### UPDATE ✏️

Used to update existing records within a table.

```sql
-- Update a single column
UPDATE employees SET age = 31 WHERE id = 1;

-- Update multiple columns
UPDATE employees SET age = 32, department = 'Management' WHERE id = 1;
```

#### DELETE ➖

Used to delete records from a table.

```sql
-- Delete specific records
DELETE FROM employees WHERE age < 30;

-- Delete all records
DELETE FROM employees;
```

### Transaction Control Language (TCL) 💾

TCL statements are used to manage transactions in the database.

#### COMMIT 💾

Used to save the current transaction.

```sql
-- Commit the current transaction
COMMIT;
```

#### ROLLBACK ⏪

Used to undo transactions that have not yet been saved.

```sql
-- Rollback the current transaction
ROLLBACK;
```

#### SAVEPOINT 📍

Used to set a savepoint within a transaction.

```sql
-- Set a savepoint
SAVEPOINT sp1;

-- Rollback to the savepoint
ROLLBACK TO SAVEPOINT sp1;
```

### Examples 📋

#### Creating and Managing a Database 🛠️

```sql
-- Create a new database
CREATE DATABASE company_db;

-- Use the new database
USE company_db;

-- Create an employees table
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    department VARCHAR(50)
);

-- Add a new column to the employees table
ALTER TABLE employees ADD salary DECIMAL(10, 2);

-- Insert records into the employees table
INSERT INTO employees (id, name, age, department, salary) VALUES
(1, 'John Doe', 30, 'HR', 60000),
(2, 'Jane Smith', 25, 'Finance', 55000),
(3, 'Mike Brown', 35, 'IT', 70000);

-- Retrieve all employees
SELECT * FROM employees;

-- Update an employee's age
UPDATE employees SET age = 31 WHERE id = 1;

-- Delete specific employees
DELETE FROM employees WHERE age < 30;

-- Truncate the table
TRUNCATE TABLE employees;

-- Drop the table
DROP TABLE employees;

-- Drop the database
DROP DATABASE company_db;
```
