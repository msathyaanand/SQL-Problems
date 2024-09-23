![image](https://github.com/user-attachments/assets/e82762c0-df5c-4832-bbf5-3085e775d511)
![image](https://github.com/user-attachments/assets/140ee4eb-67aa-48f3-8681-b4d5b7b15ee5)

Solution 1:
```
SELECT email as Email
FROM Person
GROUP BY email
HAVING COUNT(email) > 1
```

Solution 2:
```
SELECT DISTINCT email as Email
FROM Person
WHERE email IN (
    SELECT email FROM Person
    GROUP BY email
    HAVING COUNT(email) > 1
)
```

Solution 3:
```
WITH DUP AS (
    SELECT MIN(id) AS MINID FROM Person 
    GROUP BY email
)

DELETE FROM Person
WHERE id not in (
    SELECT MINID FROM DUP
)
```
