# SOL: **Structured Query Language , is a language to build relational database**

## Relational databases
 A relational database represents a collection of related (two-dimensional) tables(Rows and Columns/Attributes ).
 emp table:
 ![](https://lennilobel.files.wordpress.com/2016/09/temporal02.png)
 
 ## SELECT all querie
 
 ```sql
 SELECT * 
FROM emp;
```
 ## Queries with constraints
 
 ```sql
 SELECT EmployeeId, FirstName, …
FROM emp
WHERE condition
    AND/OR another_condition
    AND/OR …;
 ```
 
 ## Queries with constraints
 ```sql
 SELECT EmployeeId, FirstName, …
FROM emp
WHERE Department='Executive'
    AND/OR another_condition
    AND/OR …;
 ```
 
 ## Filtering and sorting Query results
 
 
 Even though the data in a database may be unique, the results of any particular query may not be – take our Movies table for example, many different movies can be released the same year. In such cases, SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.
  ```sql
 SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);
 ```
 Since the DISTINCT keyword will blindly remove duplicate rows, we will learn in a future lesson how to discard duplicates based on specific columns using grouping and the GROUP BY clause.
 **Ordering results**
 
   ```sql
 SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;

 ```
 
