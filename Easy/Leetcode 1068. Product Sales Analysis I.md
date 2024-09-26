![image](https://github.com/user-attachments/assets/545f96ff-0af9-46d1-93bf-3e6ef7884a2f)
![image](https://github.com/user-attachments/assets/4f82fd6d-2790-4f76-9bf3-e260c90d0e8d)
![image](https://github.com/user-attachments/assets/6a0134c9-2486-41ba-860d-0eab020d7b93)

Solution:
```
SELECT P.product_name,S.year,S.price
FROM Sales S
LEFT JOIN Product P
USING (product_id)
```
