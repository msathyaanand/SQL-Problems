![image](https://github.com/user-attachments/assets/fa46ab26-a7a9-4909-85ee-a7c8e0d38d07)
![image](https://github.com/user-attachments/assets/2f5ddbc4-675a-4a05-b4cc-a4b07aa722ad)

Solution:
```
SELECT activity_date as day,
COUNT(DISTINCT user_id) as active_users
FROM Activity
WHERE datediff('2019-07-27',activity_date) < 30
AND activity_date <= '2019-07-27'
GROUP BY 1;
```
