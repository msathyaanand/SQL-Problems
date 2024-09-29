![image](https://github.com/user-attachments/assets/bc1b8975-a72d-4a87-a732-bcb3dedab282)
![image](https://github.com/user-attachments/assets/5bd13627-95ea-4e01-baff-e59c1c87f7e2)

Solution:
```
SELECT buyer_id
FROM
    Sales
    JOIN Product USING (product_id)
GROUP BY 1
HAVING SUM(product_name = 'S8') > 0 AND SUM(product_name = 'iPhone') = 0;
```

*Note*
In this scenario, we are not counting the occurences of S8 or IPhone. So we will use count function typically when we want to count the occurences of specific rows.
