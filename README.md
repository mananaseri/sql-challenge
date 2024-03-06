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

