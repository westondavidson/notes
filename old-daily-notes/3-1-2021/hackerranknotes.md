- Given the table schemas below, write a query to print the 
company_code, 
founder name, 
total number of lead managers, 
total number of senior managers, 
total number of managers, 
and total number of employees. 

Order your output by ascending company_code.

SELECT c.name AS 'company_code'
        , t.name AS '

        select * from INFORMATION_SCHEMA.COLUMNS
        where COLUMN_NAME like '


SELECT company, lead_manager.lead_manager_code, senior_manager.senior_manager_code, manager.manager_code,
employee.employee_code 
from company
LEFT JOIN lead_manager
ON company.company_code = lead_manager.company_code
LEFT JOIN 
