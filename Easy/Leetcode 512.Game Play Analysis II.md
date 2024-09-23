![image](https://github.com/user-attachments/assets/d2ac625b-cbc5-4ce9-a3a1-3f3e285497af)
![image](https://github.com/user-attachments/assets/14630a27-d785-4bd5-b361-f1485cc6ffa6)

Solution:
```
SELECT player_id, MIN(device_id)
FROM Activity
GROUP BY player_id;
```

CREATED TABLE IN MYSQL WORKBENCH AS BELOW:
```
CREATE TABLE ACTIVITY(
	player_id int,
    device_id int,
    event_date date,
    games_played int
);

INSERT INTO ACTIVITY VALUES(1,2,STR_TO_DATE('2016-03-01','%Y-%m-%d'),5);
INSERT INTO ACTIVITY VALUES(1,2,STR_TO_DATE('2016-05-02','%Y-%m-%d'),6);
INSERT INTO ACTIVITY VALUES(2,3,STR_TO_DATE('2017-06-25','%Y-%m-%d'),1);
INSERT INTO ACTIVITY VALUES(3,1,STR_TO_DATE('2016-03-02','%Y-%m-%d'),0);
INSERT INTO ACTIVITY VALUES(3,4,STR_TO_DATE('2018-07-03','%Y-%m-%d'),5);

SELECT * FROM ACTIVITY;
```
![image](https://github.com/user-attachments/assets/5489974d-fb95-4c68-9e4e-6f1c21db794b)
