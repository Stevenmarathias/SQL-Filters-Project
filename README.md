# SQL-Filters-Project
git clone https://github.com/Stevenmarathias/SQL-Filters-Project.git
cd SQL-Filters-Project

mkdir src
touch src/sql_filters.sql
touch README.md
touch .gitignore

-- Retrieve after hours failed login attempts
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;

-- Retrieve login attempts outside of Mexico
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';

-- Retrieve employees in Marketing
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';

-- Retrieve employees in Finance or Sales Departments
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';

-- Retrieve employees not in IT Department
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';

# Apply Filters to SQL Queries

## Project Description
This project involves utilizing SQL queries with filters to address various security-related tasks. These tasks include retrieving failed login attempts after business hours, identifying login attempts from specific locations, and gathering information on employees in specific departments.

## How to Use
1. Place the `sql_filters.sql` file in your SQL environment.
2. Run the queries to retrieve the required information.

## SQL Queries
- Retrieve after-hours failed login attempts.
- Retrieve login attempts outside of Mexico.
- Retrieve employees in the Marketing department.
- Retrieve employees in the Finance or Sales departments.
- Retrieve employees not in the IT department.

git add .
git commit -m "Initial commit with SQL queries and README"
git push origin main
