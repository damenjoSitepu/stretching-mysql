* New Companies ( Medium )

- Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy:

- Given the table schemas below, write a query to print the company_code, founder name, total number of lead managers, total number of senior managers, total number of managers, and total number of employees. Order your output by ascending company_code.

- Query Answer: 

```
SET sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));
SELECT 
CONCAT(company.company_code,' ',company.founder,' ',COUNT(DISTINCT(employee.lead_manager_code)),' ',COUNT(DISTINCT(employee.senior_manager_code)),' ',COUNT(DISTINCT(employee.manager_code)),' ',COUNT(DISTINCT(employee.employee_code)))
FROM employee
INNER JOIN company ON employee.company_code = company.company_code
GROUP BY company.company_code;
```

