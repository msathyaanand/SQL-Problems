![image](https://github.com/user-attachments/assets/3e7d3019-9024-467f-a41a-e081d14723e3)
![image](https://github.com/user-attachments/assets/6459152b-c5e5-4c12-81ed-abd80763d94c)

Solution:
```sql
SELECT name, bonus
FROM Employee
LEFT JOIN Bonus
USING (empId)
where bonus<1000 OR bonus is NULL
```
