![image](https://github.com/user-attachments/assets/39199515-c28c-4575-aa5c-889977fc0568)
![image](https://github.com/user-attachments/assets/61219a60-9620-41c2-b0d8-a23ae4c25507)

![image](https://github.com/user-attachments/assets/5206cffb-b0ff-4599-98ce-5a63f869ad6c)
![image](https://github.com/user-attachments/assets/cf7278b3-b376-4623-b3d1-5b831eb83abd)
![image](https://github.com/user-attachments/assets/92c452ca-2c82-4890-ac2c-4e81b60469ad)


Solution:
```sql
# Write your MySQL query statement below

SELECT
    S.student_id,
    S.student_name,
    SB.subject_name,
    COUNT(E.subject_name) AS attended_exams
FROM
    Students S
CROSS JOIN
    Subjects SB  -- Crucial: CROSS JOIN to get all subjects for each student
LEFT JOIN
    Examinations E ON S.student_id = E.student_id AND SB.subject_name = E.subject_name
GROUP BY
    S.student_id, S.student_name, SB.subject_name
ORDER BY
    S.student_id, SB.subject_name;

```
