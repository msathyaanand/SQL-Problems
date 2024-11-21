![image](https://github.com/user-attachments/assets/e905f35f-795c-4162-b845-6fdf225c25df)
![image](https://github.com/user-attachments/assets/e0e5241a-dc8e-46bc-adaf-5c95446ce392)

Solution:
```sql
# Write your MySQL query statement below
/*
SELECT person_name
FROM Queue q1
WHERE (SELECT SUM(WEIGHT) FROM Queue q2 
        WHERE q2.turn <= q1.turn
    ) <= 1000
ORDER BY turn DESC
LIMIT 1
*/

WITH CTE AS
(
    SELECT person_name,
    SUM(weight) OVER (ORDER BY turn) as cumulative_weight
    FROM Queue
)
SELECT person_name
FROM CTE
WHERE cumulative_weight <=1000
ORDER BY cumulative_weight DESC
LIMIT 1
