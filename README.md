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
 
<details>
 <summary>What is the NULL is , and what is the format to filter the NULL value</summary>
     
- NULL is missing value (can come from human error, information not available, Unknown, other)
- The format is

```sql

   --Filter NULL
SELECT column_name1
FROM table_name
WHERE column_name1 IS NULL;

--Filter out NULL
SELECT column_name1
FROM table_name
WHERE column_name1 IS NOT NULL;
```

<details><summary>If we use COUNT(column_name) and COUNT(*), these two will include the NULL or not</summary>

- COUNT(column_name) not include NULL values
- COUNT(*) will include NULL values
  
</details>
</details>

<details><summary>When to use UPDATE syntax, and what is the format to use this syntax, how different between UPDATE and INSERT INTO syntax</summary>

 - UPDATE has function like itselfs name, use to update some old values in the table with the new one

```sql

--update some values in those specific column
UPDATE tablename
SET column_name1 = 'value_to_update_in_column1', column_name2 = 'value_to_update_in_column2'
WHERE condition;

--update in whole colum with new value
UPDATE tablename
SET column_name1 = 'value_to_update_in_column1', column_name2 = 'value_to_update_in_column2'

--values in column1 and column2 will be updated
```
- UPDATE is different from INSERT INTO in the way that UPDATE just update the old value with new value, but INSERT INTO uses for add new values as new row of the table
</details>


<details><summary>The meaning of primary key and foreign key</summary>
TBC
</details>


<details><summary>How many type of JOIN function, what are functions of each one </summary>

**more than 4 types: e.g.**

- INNER JOIN
- OUTER JOIN
- CROSS JOIN
- SELF JOIN

</details>
<details><summary>Concept of INNER JOIN and format of sql code</summary>

**Inner Join**: like the intersection operation in high-school mathematics topic named set

**I)**

```sql
FROM table_name1 AS t1

```

**II)**

[1]specify the key area that intersect each other

[2]in case that the key intersection field have the same column name on both table, can use this> USING (table_name); [2] in stead of ON [1] syntax 

[3] in case that have multiple joins, specify either table_name1 or table_name2 and can use either [3]+[4] or [5] for the third join

```sql
INNER JOIN table_name2 AS t2       
ON t1.column_name_table1 = t2.column_name_table2 --[1] 
USING (column_name) --[2]
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
INNER JOIN table_name1 --[3]
ON t1.column_name_table1 = t2.column_name_table2 --[4] 
AND t1.column_name_table1 = t2.column_name_table2 --[5] 


```


**III)**

- t1.column_name_table1 (in case that the name of this column has on both table, need to specify table name)
- column_name_table1(in case that the name of this 	column is unique for both table)
- column_name_table 2 AS result_set_name (If want 	define new column name shown in the result set)

```sql

SELECT t1.column_name_table1, column_name_table 2 AS result_set_name 

```


</details>



<details><summary>Concept of OUTER JOIN and format of sql code</summary>

<details><summary>RIGHT JOIN</summary></details>
<details><summary>LEFT JOIN</summary></details>
<details><summary>FULL JOIN</summary></details>
<details><summary>Example of situation applied with INNER & OUTER JOIN</summary></details>


</details>

<details><summary>Concept of CROSS JOIN and format of sql code</summary></details>

<details><summary>Concept of SELF JOIN and format of sql code</summary></details>

<details><summary></summary></details>
<details><summary></summary></details>

