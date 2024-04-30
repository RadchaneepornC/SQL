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




</details>
