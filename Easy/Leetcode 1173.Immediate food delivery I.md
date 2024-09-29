![image](https://github.com/user-attachments/assets/dce3d918-7703-48c1-b81e-5ea448af0ed2)
![image](https://github.com/user-attachments/assets/88c0e469-95db-4d8a-b73c-7b7d84956126)

Solution:
```sql
SELECT
    ROUND(SUM(order_date = customer_pref_delivery_date) / COUNT(1) * 100, 2) AS immediate_percentage
FROM Delivery;
```
