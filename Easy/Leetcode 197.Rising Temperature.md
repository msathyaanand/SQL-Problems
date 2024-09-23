![image](https://github.com/user-attachments/assets/b96eaa43-ba00-4e1f-b845-253c6b894cb4)
![image](https://github.com/user-attachments/assets/986407d2-772c-4713-95da-26acd19269db)

Solution 1:
```
SELECT W1.id
FROM Weather W1,
Weather W2
WHERE DATEDIFF(W1.recordDate,W2.recordDate)=1
AND W1.temperature > W2.temperature
```

Solution 2:
```
SELECT W1.id
FROM Weather W1 INNER JOIN Weather W2
ON date_add(W1.recordDate, interval -1 day)=W2.recordDate
WHERE W1.temperature > W2.temperature
```
