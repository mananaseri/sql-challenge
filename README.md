# https://app.quickdatabasediagrams.com/#/

departments
-
dept_no         VARCHAR(4) PK
dept_name       VARCHAR(40)

titles
-
title_id            VARCHAR(5) PK
title               VARCHAR(50)

employees
-
emp_no          INT PK         
emp_title_id    VARCHAR(5) FK >- titles.title_id
birth_date      DATE            
first_name      VARCHAR(30)
last_name       VARCHAR(30)
sex             VARCHAR(1) 
hire_date       DATE           


dept_emp
-
emp_no  INT PK FK >- employees.emp_no
dept_no VARCHAR(4)  FK >- departments.dept_no


dept_manager
-
dept_no VARCHAR(4) PK FK >- departments.dept_no
emp_no INT  FK >- employees.emp_no

salaries
-
emp_no INT PK FK >- employees.emp_no
salary INT 

 
 we used SQL queries for performing data analysis on the Pewlett Hackard employee database.
 The database contains information about employees, departments, job titles, salaries, and employee-managers.
sql-challenge includes 3 parts, Data Modelling, Data Engineering, and Data Analysis.
 
-In Data Modelling , we created our diagram by http://www.quickdatabasediagrams.com/. and saved it to PNG file. 
-with Data Engineering, we wrote codes and added tables by importing csv files to PgAdmin and saved them as table.sql
 
-And lastly in Data Analysis, 8 question are going to be answered and saved as Data_Analaysis.sql

1) Analyz Employee Information with Salary
2) get Employee Informartion who hired in 1986.
3) analyz manager department with department information
4) getting department number with employee informartion
5) listing Employees Named Hercules whos name start with "B"
6) listing employees in sales department
7) listing employees in sales and development department
8) List the frequency counts, in descending order, of all the employee last names 





