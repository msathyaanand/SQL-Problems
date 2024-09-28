![image](https://github.com/user-attachments/assets/3c50ca36-ec90-4754-9e46-dcf023bee48c)
![image](https://github.com/user-attachments/assets/174042ed-3565-420c-bb3a-3eea2c126d18)

Solution:
```
SELECT seller_id
FROM Sales
GROUP BY seller_id
HAVING
    SUM(price) >= ALL (
        SELECT SUM(price)
        FROM Sales
        GROUP BY seller_id
    );
```
