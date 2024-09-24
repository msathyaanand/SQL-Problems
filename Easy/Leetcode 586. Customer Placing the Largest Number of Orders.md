![image](https://github.com/user-attachments/assets/520d23ce-30f3-4304-a033-04921351b210)
![image](https://github.com/user-attachments/assets/3962fd5a-b0c7-4157-bb71-9071049d61e0)

Solution:
```
SELECT customer_number
FROM Orders
GROUP BY customer_number
ORDER BY COUNT(customer_number) DESC
LIMIT 1;
```
