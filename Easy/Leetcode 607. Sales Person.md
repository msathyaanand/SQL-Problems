![image](https://github.com/user-attachments/assets/58a15bf7-2109-4021-842a-59289635f0d6)
![image](https://github.com/user-attachments/assets/bfc3c996-d73c-49bf-82b7-b7320f544cef)
![image](https://github.com/user-attachments/assets/f447adb9-f318-42b7-947e-ccb10209d937)
![image](https://github.com/user-attachments/assets/c1422d39-7bdf-45a4-a787-1856d987b1ba)

Solution:
```
SELECT name
FROM SalesPerson
WHERE sales_id NOT IN (
SELECT sales_id FROM Orders
JOIN Company
USING(com_id)
WHERE name = 'RED')
```
