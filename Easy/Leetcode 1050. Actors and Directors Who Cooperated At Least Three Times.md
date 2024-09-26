![image](https://github.com/user-attachments/assets/9bb617e5-d3bd-4a64-8a83-d21fb5a870c2)
![image](https://github.com/user-attachments/assets/d2f3bee2-7ab5-4116-9ba8-57863295ccb3)

Solution:
```
SELECT actor_id, director_id
FROM ActorDirector
GROUP BY actor_id,director_id
HAVING COUNT(*)>=3;
```
