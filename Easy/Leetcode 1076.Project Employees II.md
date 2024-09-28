![image](https://github.com/user-attachments/assets/51044390-0128-464e-b14f-a353d1de2f33)
![image](https://github.com/user-attachments/assets/f4a616c4-71cd-4a16-bc99-22e65cf49c93)

Solution 1:
```
select project_id
from Project
group by project_id
having count(distinct employee_id) = (
select max(count_employee_id) from (
select project_id, count(employee_id) as count_employee_id
from Project
group by project_id
) as max_employee
);
```

Solution 2:
```
WITH max_employee AS (
SELECT project_id, COUNT(employee_id) AS count_employee_id
FROM Project
GROUP BY project_id
)
SELECT project_id
FROM Project
GROUP BY project_id
HAVING COUNT(DISTINCT employee_id) = (
SELECT MAX(count_employee_id)
FROM max_employee
);
```
