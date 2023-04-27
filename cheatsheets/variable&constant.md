# **variable and constant**

## **Variable**
A variable is as you know is a name given to a storage area that our programs can manipulate.

The variable to declare it is necesary use command "DECLARE"  then declare it with name, datatype and intial value, the command must end in semicolon(*;*). For example:

```
my_variable Varchar(10) := 'Hola mundo';
```

If you just copy and paste this command in an line code from sql, there will be an error, because also its important that the command will be into a block. For Example:


```
DECLARE
my_variable Varchar(10) := 'Hola mundo';
--OR
my_variable Varchar(10) DEFAULT 'Hola mundo';
BEGIN
 --this space is necesary otherwise there will be an error.
 --TO print the information use the next command.
 dbms_output.put_line('Literal text',);
END;
```

Into *BEGIN* and *END* block you can set values, operate or use command *SELECT* with tables. For example:


```
DECLARE
a Integer := 10;
b Integer := 25;
c Integer;
BEGIN
 --set value.

 --Operate.

 --Use in SELECT with tables.
END;
```





