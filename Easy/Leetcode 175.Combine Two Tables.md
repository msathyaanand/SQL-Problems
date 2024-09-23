![image](https://github.com/user-attachments/assets/8c6ed0fd-d0e8-4ce2-bc26-cfa4da1dc526)
![image](https://github.com/user-attachments/assets/2a2ac271-74fb-498b-8bce-726560b184e8)

Solution:
```
select p.firstName, p.lastName, a.city, a.state
from Person p
left join Address a
on p.personId = a.personId
```
