# GUVI - DAY 33

## MySQL Exercises

1. About MySQL.

   > - SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database.
   > - They are scalable and a safe storage.
   > - A relational database represents a collection of related (two-dimensional) tables.
   > - They are very similar to a Microsoft Excel Spreadsheet.
   > - MySQL is case-insensitive.

2. About the Task.

   > - In this task, we solve given exercises from the following website: *https://sqlbolt.com/*.
   > - This website gives us a good idea about the concepts in SQL and also provides a platform to practice the concepts using some exercises.
   > - There are total of 18 exercises in this task which are completed and submitted in the pdf file.
   > - The PDF file contains pictures of the exercises completed and submitted in the website.
   > - [Source File](./Task%20Document.pdf)

3. Inference.

   > - In this section, We will be discussing about the concepts inferred by myself through this task and exercises.

   1. Creating a table/database in MySQL.

      > - We can create a database or a table in MySQL by running the following query syntax.

      ```
      CREATE DATABASE db_name;
      CREATE TABLE table_name;
      ```

   2. Inserting data to a table.

      > - Data is added to a table by using the `INSERT` keyword.
      > - The syntax is as follows:

      ```
      INSERT INTO table_name (column1, column2, column3) VALUES (value1, value2, value3);
      ```

   3. Updating a record in a table.

      > - We can update a record in a table by using the `UPDATE` keyword.
      > - The syntax is as follows:

      ```
         UPDATE table_name SET column_name = value;
      ```

      > - If run without a `WHERE` clause, all the records in the table, will be updated, so to achieve accurate and safe updationg of data, `WHERE` clause is a must to use.

      ```
         UPDATE table_name SET column_name = value WHERE unique_identifier = id_value;
      ```

   4. Deleting a record in a table.

      > - We can delete a record in a table by using the `DELETE` keyword.
      > - The syntax is as follows:

      ```
      DELETE FROM table_name;
      ```

      > - The above query will truncate the whole table. Hence, like the `UPDATE` keyword, it is safe to use `DELETE` query, only with a `WHERE` clause.

      ```
      DELETE FROM table_name WHERE unique_identifier = id_value;
      ```

   5. Fetching data from a table.

      > - We fetch data from the database tables using the `SELECT` query.
      > - The syntax is as follows:

      ```
      SELECT * FROM table_name;
      ```

      > - Here, asterisk (\*) represents all the columns in the table.

      > - We can fetch specific columns from the table as well, it is achieved by using the following syntax:

      ```
      SELECT column_1, column_2 from table_name;
      ```

   6. Filtering data from a table, while fetching.

      > - Data is a database is very vast, therefore, it is must to only fetch the data that is required to not expose it to the world.
      > - We can filter the data, by using the `WHERE` clause and some operators, that help us in filtering data accurately.
      > - Example:

      ```
      SELECT * FROM table_name WHERE condition = value;
      ```

      > - We can combine conditions together by using Logical operators (AND, OR, NOT)

      ```
      SELECT * FROM table_name WHERE condition1 = value1 AND condition2 = value2;
      SELECT * FROM table_name WHERE condition1 = value1 OR condition2 = value2;
      SELECT * FROM table_name WHERE condition != value;
      SELECT * FROM table_name WHERE NOT(condition = value);
      ```

      > - We can compare values in various ways, equality is just one of them. Other operators in MySQL are: `LIKE, NOT LIKE, IN, NOT IN`

      > - `LIKE` is a special operator which can be used to compare string values by using basic _placeholders_. There are 2 placeholders, `%` and `_`. `%` represent a sequence of characters while `_` represents a single character.

      > - `IN` Operator is a special operator which can be used to check if a value exists within a sequence of values that are represented using the parentheses()

      ```
      SELECT * FROM table_name WHERE value LIKE 'patt_ern%';

      SELECT * FROM table_name WHERE value IN (value1, value2, value3);
      ```

      > - `NOT IN` and `NOT LIKE` operators are negations of the `IN` and `LIKE` operators respectively.

   7. Sorting of records.

      > - To sort the records in the table, we use the `ORDER BY` operator.
      > - We can sort the records in any fashion, either Ascending(ASC) or Descending(DESC).
      > - The default for `ORDER BY` is Ascending.
      > - Syntax:

      ```
      SELECT * FROM table_name ORDER BY column_name;
      ```

      > - We can limit the number of records by using the `LIMIT` operator.

      ```
      SELECT * FROM table_name LIMIT 5;
      ```

      > - We can fetch specific records from the table, even the records located between the table using `OFFSET` operator.

      ```
      SELECT * FROM table_name LIMIT 5 OFFSET 5;
      ```

      > - We fetch 5 reecords from the table, after leaving the first 5 records which is our offset value.

   8. Aggregate Functions and GROUP BY.

      > - In MySQL, we can also perform mathematical and also String or Date operations using the aggregate functions such as AVG(), SUM(), ABS(), etc.

      ```
      SELECT SUM(column_name) FROM table_name;
      ```

      > - While operating with such functions, we can group them by other columns as well.
      > - For example, Let's find the `sum` of `salary` in the `employees` table and group them by their roles.

      ```
      SELECT role, SUM(salary) FROM employees GROUP BY role;
      ```

   9. Combining two or more tables.

      > - When working with large databases, we face a need to fetch data from multiple tables that are related to each other, for the data to be meaningful.
      > - We can achieve this behaviour by using the `JOIN` keyword.
      > - There are 5 types of JOINs in MySQL, `LEFT JOIN`, `RIGHT JOIN`, `INNER JOIN`, `SELF JOIN` and `FULL JOIN`.
      > - Syntax:

      ```
      SELECT * from table_1 JOIN table_2 ON table_1.id = table_2.id;
      ```

      > - The default for `JOIN` is `INNER JOIN`.

   10. NULL in MySQL.
       > - In MySQL, NULL is an empty value that needs to be avoided.
       > - We can use data-type specific values such as 0 for INTEGER.
       > - To check whether a value is NULL or not we use the `IS` keyword.
       > - Syntax:
       ```
       SELECT * FROM table_name WHERE column IS NULL;
       ```
       > - To check if the value is not NULL, we go with the `NOT NULL` check.
       ```
       SELECT * FROM table_name WHERE column IS NOT NULL;
       ```

4. Conclusion.
   > - In conclusion, MySQL is a RDBMS technology with which we can achieve a relational database to store data that is safe and secure to deploy.
