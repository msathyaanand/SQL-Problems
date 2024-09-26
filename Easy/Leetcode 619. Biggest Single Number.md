![image](https://github.com/user-attachments/assets/2d3637fd-def0-4637-9f02-07eea0143bdb)
![image](https://github.com/user-attachments/assets/4ff8cc76-e9f3-4b71-8b21-1ac9ef95216c)
![image](https://github.com/user-attachments/assets/735c9086-91cd-4f77-90f2-c3ba81d6bf0a)

Solution:
```
SELECT MAX(num) AS num
FROM (
  SELECT num FROM MyNumbers
  GROUP BY num
  HAVING COUNT (num) = 1
)
```
