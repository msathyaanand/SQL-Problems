![image](https://github.com/user-attachments/assets/29c31a6d-c9bd-4f41-ab7c-a5c80a5f8db9)
![image](https://github.com/user-attachments/assets/1bf4f4ce-22e0-4441-8c6d-d5c99bad2484)

Solution:
```sql
  select query_name, 
  round(avg(rating/position),2) as quality, 
  round(avg(case when rating < 3 then 1 else 0 end)*100,2) as poor_query_percentage
  from queries
  where query_name is not null
  group by query_name
```
