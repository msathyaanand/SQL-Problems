![image](https://github.com/user-attachments/assets/4691d5b3-43db-4bf5-b041-d0e8866997f6)
![image](https://github.com/user-attachments/assets/614029f3-dca9-42e0-95a8-9407891d0d5f)

Solution:
```
SELECT name as Customers
FROM Customers C
LEFT JOIN ON Orders O
ON C.id = O.customerId
WHERE O.customerId IS NULL
```

Solution 2:
```
SELECT name AS Customers
FROM Customers
WHERE id NOT IN (SELECT customerId FROM ORDERS)
```
