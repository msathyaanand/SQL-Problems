![image](https://github.com/user-attachments/assets/d1143934-7020-47e6-8bf6-1ffc2187b3ce)
![image](https://github.com/user-attachments/assets/df119f03-0149-4226-aa69-cbbcb76baa74)

Solution 1:
```
DELETE P1 FROM Person P1, Person P2
WHERE P1.email = P2.email and p1.id>p2.id;
```

Solution 2:
```
WITH DUP AS(
  SELECT MIN(id) as MINID
  FROM Person
  GROUP BY email 
)

DELETE FROM Person
WHERE id not in (SELECT MINID FROM DUP);
```
