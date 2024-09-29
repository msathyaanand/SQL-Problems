![image](https://github.com/user-attachments/assets/3074fdaf-5cb6-4eea-a057-f4bb2afcdfeb)
![image](https://github.com/user-attachments/assets/58a09c4c-2d2f-432a-aced-8123774152e9)

Solution 1:
```
SELECT P.product_id, P.product_name
FROM Sales S
INNER JOIN Product P
USING (product_id)
GROUP BY 1,2
HAVING SUM(
    S.sale_date < '2019-01-01'OR
    S.sale_date > '2019-03-31'
)=0;
```
Solution 2:
```
SELECT Sales.product_id, product_name
FROM Sales JOIN Product ON Sales.product_id = Product.product_id
GROUP BY Sales.product_id
HAVING MAX(sale_date) >= '2019-01-01' AND MAX(sale_date) <= '2019-03-31'
    AND MIN(sale_date) >= '2019-01-01' AND MIN(sale_date) <= '2019-03-31';
```
