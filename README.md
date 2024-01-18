# use existing employee table
Write a SQL query to find the average salary for each department and also include the total number of employees in each department. Display the results in descending order of the average salary.


```SQL
SELECT
    department_id,
    TRUNC( AVG(salary), 2 ) AS average_salary,
    COUNT(employee_id) AS total_employees
FROM
    employees
GROUP BY
    department_id
ORDER BY
    average_salary DESC;
```
