# **Diference Triggers (BEFORE, AFTER  and  INSTEAD OF)**
We have the next table to do de example: 

|NAME|ID|SALARY|
| :-----: | :----: | :----:|
|JHON| 1 | 1500|
|kAREN | 2 | 756000|
|lUIS | 3 | 8500|
|DIOMEDES | 4 | 26000|
|FERNANDO | 5 | 30400|

**BEFORE**

Usually it is use to validation and update.


```
CREATE OR REPLACE TRIGGER min_Salary
BEFORE INSERT or UPDATE on employee
FOR EACH ROW 

DECLARE

BEGIN
  
  if(:NEW.salary<1000) then
  DBMS_OUTPUT.PUT_LINE ('Employee must have at least a minimun salary');  
    END IF;
END;    

```

when it insert in table 

```
Insert into employee values ('kevin',7,450);
```


**AFTER**








