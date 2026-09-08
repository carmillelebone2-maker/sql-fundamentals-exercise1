CREATE CATALOG IF NOT EXISTS employees;

CREATE SCHEMA IF NOT EXISTS employees.table;

CREATE OR REPLACE TABLE employees.table.employee(
employee_id INT,
first_name STRING,
last_name STRING,
department STRING,
salary INT,
hire_date DATE,
city STRING);

DROP TABLE employees.table.employee;

DROP TABLE IF EXISTS exercise.employees.table;


CREATE CATALOG IF NOT EXISTS employees;

CREATE SCHEMA IF NOT EXISTS employees.table;

CREATE OR REPLACE TABLE employees.table.employees(
employee_id INT,
first_name STRING,
last_name STRING,
department STRING,
salary INT,
hire_date DATE,
city STRING);

INSERT INTO employees.table.employees VALUES
(1, 'Alice', 'Green', 'IT', 70000, '2020-01-10', 'Johannesburg'),
(2, 'Brian', 'Lee', 'HR', 45000, '2019-03-22', 'Cape Town'),
(3, 'Cathy', 'Zulu', 'Finance', 65000, '2018-07-18', 'Durban'),
(4, 'David', 'Mokoena', 'Marketing', 50000, '2021-11-05', 'Pretoria'),
(5, 'Eva', 'Naidoo', 'IT', 72000, '2017-09-30', 'Johannesburg');

--Checking the table
SELECT* FROM employees.table.employees;

--Question 1: Retreive all columns from the employees table
SELECT* FROM employees.table.employees;

--Question 2: Find all unique departments
SELECT DISTINCT department
FROM employees.table.employees;

--Question 3: Retrieve first and last names ordered by salary descending
SELECT first_name,
       last_name
FROM employees.table.employees
ORDER BY salary DESC;

--Question 4: Retrieve the top 3 highest-paid employees
SELECT first_name,
       last_name,
       salary
FROM employees.table.employees
ORDER BY salary DESC
LIMIT 3;

--Question 5: Find employees in the IT department
SELECT employee_id,
       first_name,
       last_name,
       department
FROM employees.table.employees
WHERE department = 'IT';

--Question 6: Find employees in Finance with salary > 60000
SELECT employee_id,
       first_name,
       last_name,
       department,
       salary
FROM employees.table.employees
WHERE salary > 60000 AND department = 'Finance';

--Question 7: Find employees in HR or Marketing
SELECT employee_id,
       first_name,
       last_name,
       department
FROM employees.table.employees
WHERE department = 'HR' OR department = 'Marketing';

--Question 8:Find employees not in IT
SELECT employee_id,
       first_name,
       last_name,
       department
FROM employees.table.employees
WHERE NOT department = 'IT';

--Question 9: Find employees in IT, HR or Finance using IN
SELECT employee_id,
       first_name,
       last_name,
       department
FROM employees.table.employees
WHERE department IN ('IT', 'HR', 'Finance');


--Question 10: Find employees in IT with salary > 65000 and city Johannesburg
SELECT employee_id,
       first_name,
       last_name,
       department,
       salary,
       city 
FROM employees.table.employees
WHERE department = 'IT' AND salary > 65000 AND city = 'Johannesburg';
