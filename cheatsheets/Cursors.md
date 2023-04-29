# **Cursors**
Contiene información de filas devueltas por una instrucción. Se conocen dos tipos de cursores:

##  **Implicit Cursors**

Son creados por oracle cuando las instrucciones son ejecutadas y no se llaman a se asignan a un cursor. Son comandos sql que permiten ver la información de la instrucción, como si afecto o no a la tabla y en que cantidad la afecto.

|Comando|Descripcion|
| :-----: | :----:|
|**sql%found**|De vuelve verdadero si afecto a una o más filas, de lo contrario falso.|
|**sql%notfound**|De vuelve verdadero si afectó alguna fila, de lo contrario falso.|
|**sql%isOpen**|Devuelve falso para cursores implicitos.|
|**sql%rowCount**|Devuele el numero de filas afectadas.|

We have the next table Employee:

|NAME|ID|SALARY|
| :-----: | :----: | :----:|
|JHON| 1 | 1500|
|kAREN | 2 | 756000|
|lUIS | 3 | 8500|
|DIOMEDES | 4 | 26000|
|FERNANDO | 5 | 30400|

```
DECLARE  
   total_rows number(2); 
BEGIN 
   UPDATE Employee 
   SET salary = salary + 500; 
   IF sql%notfound THEN 
      dbms_output.put_line('no employee selected'); 
   ELSIF sql%found THEN 
      total_rows := sql%rowcount;
      dbms_output.put_line( total_rows || ' employee selected '); 
   END IF;  
END; 
/    
```
## **Explicit Cursors**
