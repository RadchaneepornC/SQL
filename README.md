# SQL
As the learning technique named active recall is one of the most efficient techniques, I apply this technique by jotting down <br>
my **SQL learning** notes in a Q&A format. Enjoy Reading !

 <details>
 <summary> SQL is stand for</summary>
     
   ```Structureed query language```
 
 </details>

 <details>
 <summary> Example of databases that understand SQL</summary>
     
   ```Oracle, MySQL,PostgreSQL, Microsoft SQL Server, IBM Db2, MS Access```
 
 </details>

<details>
 <summary> SQL is case sensitive or not</summary>
     
   ```No, but the clause using with LIKE, NOT LIKE are case sensitive```
 
 </details>

 <details>
 <summary> How to add comment in SQL</summary>
     
   ```sql

      /* comment */
        or
      --Comment
   ```
 
 </details>

 
 <details>
 <summary> What is the 'records' and 'field' means in SQL </summary>
     
   ```
      records = rows

      field = column

   ```
 </details>


 <details> <summary> the standard formats to use select for query I) specific column, II)select All column III) return only unique records</summary>

<br>

**I) specific column**

    
```sql
    
    SELECT column_name1, column_name2,…
    FROM table_name
    WHERE condition;
```
    
    
**II) select All column**
    
 ```sql
    SELECT (*)
    FROM table_name
    WHERE condition;
```
    
    but if COUNT(*) mean count all rows
    
**III) return only unique records**
    
```sql
    SELECT DISTINCT column_name1, column_name2,…
    FROM table_name
    WHERE condition;
```
</details>

 <details>
 <summary> For AND operator, which is the practical one  </summary>
     
**I)**
```sql
SELECT column_name
FROM table_name
WHERE condition>20 AND condition <30;
```

**II)**

```sql

SELECT column_name
FROM table_name
WHERE condition>20 AND <30;

```


<details><summary> The answer is </summary>
I) is correct, II) is syntax error

If want to write in the form of II)

```sql

SELECT column_name
FROM table_name
WHERE condition BETWEEN 20 AND 30; --but this is include 20,30

```

</details>
</details>


 <details>
 <summary>What view syntax use for, and please write basic format of view using?</summary>

 the virtual table that is the result of a saved SQL SELECT statement, stored for future use and not stored in the data base

```sql
 --format 
CREATE VIEW view_name AS
SELECT coumn_name1, column_name2, colum_name3
FROM table_name;

--no result set created for view
--avoid to use ORDER BY in the structure of view creating, if want to use, use when recall the view for using instead
```

```sql
--when recall the view to use
SELECT column_name1, column_name2
FROM view_name;

```

 </details>

 <details>
 <summary> When to use OEDER BY syntax, and what is the format to use this syntax </summary>

```ORDER BY``` uses when want to sort the result set numeriacally or alphabetically, the format of using is
   
```sql

SELECT column_name1, column_name2,…
FROM table_name
ORDER BY column_name1, column_name2 DESC;

/*this mean you sort the row in column 1 ascendingly(DEFULT,no need to write ASC
 (A to Z, min to max) for the repeated value of column 1, you will sort the row
 in column 2 descendingly */
```
 
 </details>

 <details>
 <summary> INSERT INTO syntax, use for ? and what is the format of its using ? </summary>
     
  ```INSERT INTO used``` to insert new row to the table

formats are below

**I) insert data in every column** <br>

(can both specific column name and does not, for later case, make sure that values are in the correct order that you want)
   
 ```sql

 --specify column
INSERT INTO tablename(column_name1, column_name2, column_name3)
VALUES ('value_to_column1', 'value_to_column2','value_to_column3')
--should input ' ' both string and integer values

--do not specify column
INSERT INTO tablename
VALUES ('value_to_column1', 'value_to_column2','value_to_column3')

```

**II) insert data for specific columns** <br>


   
 ```sql

INSERT INTO tablename(column_name1, column_name3)
VALUES ('value_to_column1','value_to_column3')
--NULL will appear in the column2 area since we do not provide the value

```


 </details>
 

 

