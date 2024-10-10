![image](https://github.com/user-attachments/assets/77ac8e95-d785-4e36-90c8-3d77acc5bc05)
![image](https://github.com/user-attachments/assets/3af55fed-5db8-4ca4-925e-71e70c60c2b1)

Solution:
```sql
SELECT *
FROM Cinema
WHERE id%2 <> 0 AND description <> 'boring'
ORDER BY rating DESC
```
