![image](https://github.com/user-attachments/assets/fc72889b-f641-4fce-aa42-309e2cba89de)
![image](https://github.com/user-attachments/assets/ef7714ac-3acf-4bad-8e10-e352f4b9db20)

Solution:
```sql
SELECT
    x, y, z,
    CASE WHEN x + y > z AND y + z > x AND z + x > y THEN 'Yes' ELSE 'No' END AS triangle
FROM triangle;

```
