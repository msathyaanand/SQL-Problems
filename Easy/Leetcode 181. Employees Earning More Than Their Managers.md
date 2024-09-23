![image](https://github.com/user-attachments/assets/3f97c9ca-4841-44d4-b060-b20d417387ab)
![image](https://github.com/user-attachments/assets/d2efb195-0086-4aff-8062-6ff80079216b)

Solution:
```
SELECT E1.name AS Employee
FROM Employee E1
INNER JOIN Employee E2
ON E1.managerId = E2.id
WHERE E1.salary > E2.salary
```

### Approach:

Self-Join: The query uses a self-join on the Employee table. This means the table is joined with itself to compare rows within the same table.
<br>Aliases: Two aliases, E1 and E2, are used to differentiate between the employee and the manager within the same table.
<br>Join Condition: The join condition ON E1.managerId = E2.id ensures that each employee (E1) is matched with their manager (E2).
<br>Filter Condition: The WHERE clause E1.salary > E2.salary filters the results to include only those employees whose salary is greater than their manager’s salary.
