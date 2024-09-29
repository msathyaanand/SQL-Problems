![image](https://github.com/user-attachments/assets/419f17c7-e14c-42c0-8b4c-02150d7c1238)
![image](https://github.com/user-attachments/assets/335d2100-433c-4598-a4a8-861f70ed0685)

Solution:
```sql
SELECT author_id as id
FROM Views
Where author_id=viewer_id
GROUP BY 1
ORDER BY 1
```
