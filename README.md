# Employee Management System (SQL Server)

##  Overview
The Employee Management System is a relational database project built using Microsoft SQL Server.  
It is designed to manage employee records, departments, roles, salaries, and related operations efficiently using structured queries and database objects.

This project demonstrates strong understanding of database design, normalization, and advanced SQL concepts.

---

##  Tech Stack
- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- T-SQL

---

##  Project Objectives
- Design a normalized relational database
- Implement CRUD operations using Stored Procedures
- Enforce data integrity using Constraints
- Automate operations using Triggers
- Generate reports using Views
- Optimize queries using Indexes

---

##  Database Components

###  Tables
- Employees
- Departments
- Roles / Designations
- Salaries
- Attendance (if applicable)

###  Stored Procedures
- Add Employee
- Update Employee
- Delete Employee
- Fetch Employee Details

###  Triggers
- Audit logging on employee updates
- Automatic salary validation

###  Views
- Employee summary report
- Department-wise employee count

###  Functions
- Salary calculation
- Bonus calculation (if implemented)

---

##  How to Run the Project

1. Open SQL Server Management Studio (SSMS)
2. Connect to your SQL Server instance
3. Execute scripts in this order:
   - Create Database
   - Create Tables
   - Apply Constraints
   - Insert Sample Data
   - Create Stored Procedures / Views / Triggers
4. Run stored procedures to test functionality

---

##  SQL Concepts Used
- Primary Keys & Foreign Keys
- NOT NULL, UNIQUE, CHECK Constraints
- JOINS (INNER, LEFT, RIGHT)
- GROUP BY & Aggregate Functions
- Subqueries
- Indexing
- Stored Procedures
- Triggers
- Views
- User Defined Functions

---

##  Sample Query

```sql
SELECT d.DepartmentName, COUNT(e.EmployeeID) AS TotalEmployees
FROM Employees e
JOIN Departments d ON e.DepartmentID = d.DepartmentID
GROUP BY d.DepartmentName;
