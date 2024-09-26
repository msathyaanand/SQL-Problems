![image](https://github.com/user-attachments/assets/d99b2023-1724-4bbb-8b47-3032d4ff3801)
![image](https://github.com/user-attachments/assets/14df452f-b2b2-49eb-991d-a5859761913a)

Solved using Triangle Inequality theorem : <br>
(a + b > c)<br>
(b + c > a)<br>
(c + a > b)

Solution:
```
SELECT
    x, y, z,
    CASE WHEN x + y > z AND y + z > x AND z + x > y THEN 'Yes' ELSE 'No' END AS triangle
FROM triangle;
```
