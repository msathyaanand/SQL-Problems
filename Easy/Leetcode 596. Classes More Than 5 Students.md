![image](https://github.com/user-attachments/assets/0665212b-0fb8-4d45-baae-86c0849e4c35)
![image](https://github.com/user-attachments/assets/5dae51ac-d4fc-4d3f-a6d7-df6df5d006a3)

Solution:
```
SELECT class
FROM Courses
GROUP BY class
HAVING COUNT(class)>=5
```
