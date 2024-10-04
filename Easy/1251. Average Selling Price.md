![image](https://github.com/user-attachments/assets/9799bc03-39f3-4562-a820-870ead63e4c3)
![image](https://github.com/user-attachments/assets/7452880c-3e24-4499-990c-99c2d31e1057)

![image](https://github.com/user-attachments/assets/563bd5f3-1d9b-4a0b-a0ec-766315f14e43)
![image](https://github.com/user-attachments/assets/b794aaac-03f2-47c2-ba2d-4effc452a523)

Solution 1:
```sql
SELECT
    P.product_id,
    ROUND(COALESCE(SUM(U.units * P.price) / NULLIF(SUM(U.units), 0), 0), 2) AS average_price
FROM Prices AS P
LEFT JOIN UnitsSold AS U ON P.product_id = U.product_id
AND U.purchase_date BETWEEN P.start_date AND P.end_date
GROUP BY P.product_id;
```

Solution 2:
```sql
select p.product_id,
       coalesce(
         round(sum(p.price * units) / sum(units), 2),
         0) as average_price
from Prices p
left join UnitsSold us on p.product_id = us.product_id
and us.purchase_date >= p.start_date
and us.purchase_date <= end_date
group by (p.product_id)
