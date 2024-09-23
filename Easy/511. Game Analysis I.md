![image](https://github.com/user-attachments/assets/d5ff0460-53c3-4dca-a551-52d0594ae39e)
![image](https://github.com/user-attachments/assets/b79baa9b-f7d1-4035-8b47-8a2155f6461c)

Solution:
```
SELECT player_id, MIN(event_date) AS first_login
FROM Activity
GROUP BY player_id;
```
