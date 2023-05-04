# OVERVIEW:
This week?s Challenge is about the HR data in a company named Pewlett Hackard (a fictional company). 
The task was to create a research project about people whom the company employed during the 1980s and 1990s. Six CSV files were provided as data to load and create 6 tables for a database namely: employees, departments, dept_manager, dept_emp, salaries and titles. The following ERD was used to build the database:




# ANALYSIS
Resources used:
I used PostgreSQL in PGAdmin4 to create the database and then the tables and eventually the queries. I used QuickDBD to create the ERD. 
I worked with my tutor, Kelli Kennedy and a lot of internet searches.


Most of the requirements needed joining different tables. For example, to find the list of employees in Sales and Development we needed to join three tables: employees, dept_emp and departments. The query looks like: SELECT a.emp_no, a.last_name, a.first_name, c.dept_name
FROM employees as a
    JOIN dept_emp as b
    ON a.emp_no=b.emp_no
	JOIN departments as c
	ON b.dept_no = c.dept_no
	WHERE c.dept_name IN ('Sales', 'Development')
ORDER BY a.emp_no;

The result is:



For analysis no. 5 - List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B. ? I used the following query:
SELECT first_name, last_name, sex
FROM employees
WHERE first_name = 'Hercules'
AND last_name LIKE 'B%';

The data was found in a single table. The following was the result:



# CONCLUSION:
While we explored the data which is mostly for older employees, perhaps we should increase the scope to check the data about younger employees and which department employees the youngest employees. We can also check how long they have been in their current roles and with the organization.
