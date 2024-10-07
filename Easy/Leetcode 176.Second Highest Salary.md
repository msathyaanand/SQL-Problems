![image](https://github.com/user-attachments/assets/7f1d6376-b69e-40ff-82fc-2edffc0fdbb9)
![image](https://github.com/user-attachments/assets/9ed2edf4-3a12-4b83-9083-328df4196433)

Solution:
```sql
SELECT MAX(salary) AS SecongHighestSalary
FROM Employee
WHERE salary < (SELECT MAX(salary) IN Employee)
```
