![image](https://github.com/user-attachments/assets/f9c2a03d-5cc6-465c-96b4-6c45342c9bce)
![image](https://github.com/user-attachments/assets/977cf15d-2eb1-4215-9e00-81f9257ea4d3)

Solution 1:
```
SELECT project_id,
ROUND(AVG(experience_years),2) AS average_years
FROM Project 
JOIN Employee 
USING (employee_id)
GROUP BY project_id
```

Solution 2:
```
SELECT p.project_id, 
ROUND(SUM(e.experience_years)/COUNT(p.project_id),2) AS average_years
FROM Project p
LEFT JOIN Employee e ON p.employee_id=e.employee_id
GROUP BY p.project_id;
```
