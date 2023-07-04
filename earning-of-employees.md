* Earning Of Employees ( Medium )

- We define an employee's total earnings to be their monthly  worked, and the maximum total earnings to be the maximum total earnings for any employee in the Employee table. Write a query to find the maximum total earnings for all employees as well as the total number of employees who have maximum total earnings. Then print these values as  space-separated integers.

- Query Answer: 

```
SELECT
CONCAT(MAX(employee.months * employee.salary),' ',COUNT(employee_id))
FROM employee
WHERE (employee.months * employee.salary) = (SELECT MAX(employee.months * employee.salary) FROM employee);
```