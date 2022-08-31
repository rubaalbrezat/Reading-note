## What is SQL?
SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

## SQL Lesson 1: SELECT queries 101
SELECT : To retrieve data from a SQL database.

query : query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. 

example : 
SELECT * 
FROM mytable;

## SQL Lesson 2: Queries with constraints (Pt.1)

WHERE : In order to filter certain results from being returned.

example : 
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;

|  Operator   |   	Condition   | 	SQL Example  |
|----------|:-------------:|:-------------:|
| =, !=, < <=, >, >= | Standard numerical operators |col_name != 4 |
| BETWEEN … AND …|  Number is within range of two values (inclusive) |  col_name BETWEEN 1.5 AND 10.5| 
| NOT BETWEEN … AND … | …	Number is not within range of two values (inclusive) |c ol_name NOT BETWEEN 1 AND 10 | 
|IN (…)   |	Number exists in a list|col_name IN (2, 4, 6)|
|NOT IN (…)	| Number does not exist in a list|col_name NOT IN (1, 3, 5) |

## Lesson 3: Queries with constraints (Pt.2)
Here are some string comparison and pattern matching operators.

|  Operator   |   	Condition   | 	SQL Example  |
|----------|:-------------:|:-------------:|
| = | Case sensitive exact string comparison (notice the single equals) |col_name = "abc" |
| != or <> |  Case sensitive exact string inequality comparison |  col_name != "abcd"| 
| LIKE	| Case insensitive exact string comparison | col_name LIKE "ABC" | 
| NOT LIKE   |	Case insensitive exact string inequality comparison |col_name NOT LIKE "ABCD" |
| % | Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) | col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS") |
| _	| Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) | col_name LIKE "AN_"
(matches "AND", but not "AN") | 
|IN (…)  |	String exists in a list | col_name IN ("A", "B", "C") |
| NOT IN (…) | tring does not exist in a list | col_name NOT IN ("D", "E", "F") |

## SQL Lesson 4: Filtering and sorting Query results
DISTINCT : to discard rows that have a duplicate column value.

example : 
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);

ORDER BY : o sort your results by a given column in ascending or descending order. 

 example :
 SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;

## SQL Lesson 6: Multi-table queries with JOINs

Entity data in the real world is often broken down into pieces and stored across multiple orthogonal tables using a process known as normalization. Database normalization is useful because it minimizes duplicate data in any single table, and allows for data in the database to grow independently of each other (ie. Types of car engines can grow independent of each type of car).

The INNER JOIN is a process that matches rows from the first table and the second table which have the same key (as defined by the ON constraint) to create a result row with the combined columns from both tables. After the tables are joined, the other clauses we learned previously are then applied.

example :
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;


## LESSON 7: OUTER JOINs
If the two tables have asymmetric data, which can easily happen when data is entered in different stages, then we would have to use a LEFT JOIN, RIGHT JOIN or FULL JOIN instead to ensure that the data you need is not left out of the results.

example :
SELECT column, another_column, …
FROM mytable
INNER/LEFT/RIGHT/FULL JOIN another_table 
    ON mytable.id = another_table.matching_id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
Note that the OUTER keyword is optional (LEFT OUTER JOIN === LEFT JOIN).

## LESSON 8: A short note on NULLs

Select query with constraints on NULL values
SELECT column, another_column, …
FROM mytable
WHERE column IS/IS NOT NULL
AND/OR another_condition
AND/OR …;

## SQL Lesson 9: Queries with expressions

LESSON 9: Queries with expressions
An example of a query with expressions (using basic mathematical/string functions to transform values when the query is executed).

SELECT particle_speed / 2.0 AS half_particle_speed
FROM physics_data
WHERE ABS(particle_position) * 10.0 > 500;
or

SELECT column AS better_column_name, …
FROM a_long_widgets_table_name AS mywidgets
INNER JOIN widget_sales
  ON mywidgets.id = widget_sales.widget_id;


## LESSON 10: Queries with aggregates (Pt.1)

|  Function  |   	Description   | 
|----------|:-------------:|
| COUNT(*)
COUNT(column) |A common function used to counts the number of rows in the group if no column name is specified. Otherwise, count the number of rows in the group with non-NULL values in the specified column. |
| MIN(column) |  Finds the smallest numerical value in the specified column for all rows in the group. |  
| MAX(column)	| Finds the largest numerical value in the specified column for all rows in the group. | 
| AVG(column)  |	Finds the average numerical value in the specified column for all rows in the group. |
| SUM(column) | Finds the sum of all numerical values in the specified column for the rows in the group. |

## LESSON 11: Queries with aggregates (Pt.2)
SQL allows us to do this by adding an additional HAVING clause which is used specifically with the GROUP BY clause to allow us to filter grouped rows from the result set.

Select query with HAVING constraint
SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …
FROM mytable
WHERE condition
GROUP BY column
HAVING group_condition;

## LESSON 12: Order of execution of a query
The order of execution of different parts of a query is:

1. FROM and JOINs
2. WHERE
3. GROUP BY
4. HAVING
5. SELECT
6. DISTINCT
7. ORDER BY
8. LIMIT and OFFSET

## LESSON 13: Inserting rows

What is a Schema?
We previously described a table in a database as a two-dimensional set of rows and columns, with the columns being the properties and the rows being instances of the entity in the table. In SQL, the database schema is what describes the structure of each table, and the datatypes that each column of the table can contain.

INSERT : When inserting data into a database

insert statement with values for all columns
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;

## SQL Lesson 14: Updating rows

UPDATE : update existing data.

Update statement with values
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;

# LESSON 15: Deleting rows

DELETE : When you need to delete data from a table in the database

Delete statement with condition
DELETE FROM mytable
WHERE condition;

## LESSON 16: Creating tables

|  
Data type  |   	Description   | 
|----------|:-------------:|
| INTEGER, BOOLEAN |The integer datatypes can store whole integer values like the count of a number or an age. In some implementations, the boolean value is just represented as an integer value of just 0 or 1. |
| FLOAT, DOUBLE, REAL |  The floating point datatypes can store more precise numerical data like measurements or fractional values. Different types can be used depending on the floating point precision required for that value. |  
| CHARACTER(num_chars), VARCHAR(num_chars), TEXT	| The text based datatypes can store strings and text in all sorts of locales. The distinction between the various types generally amount to underlaying efficiency of the database when working with these columns.

Both the CHARACTER and VARCHAR (variable character) types are specified with the max number of characters that they can store (longer values may be truncated), so can be more efficient to store and query with big tables. | 
| DATE, DATETIME |	SQL can also store date and time stamps to keep track of time series and event data. They can be tricky to work with especially when manipulating data across timezones. |
| BLOB | Finally, SQL can store binary data in blobs right in the database. These values are often opaque to the database, so you usually have to store them with the right metadata to requery them. |


|  
Constraint |   	Description   | 
|----------|:-------------:|
| PRIMARY KEY | This means that the values in this column are unique, and each value can be used to identify a single row in this table. |
| AUTOINCREMENT | For integer values, this means that the value is automatically filled in and incremented with each row insertion. Not supported in all databases. |  
| UNIQUE	| This means that the values in this column have to be unique, so you can't insert another row with the same value in this column as another row in the table. Differs from the `PRIMARY KEY` in that it doesn't have to be a key for a row in the table. | 
| NOT NULL |	This means that the inserted value can not be `NULL`. |
| CHECK (expression) | FThis allows you to run a more complex expression to test whether the values inserted are valid. For example, you can check that values are positive, or greater than a specific size, or start with a certain prefix, etc. |
| FOREIGN KEY | This is a consistency check which ensures that each value in this column corresponds to another value in a column in another table.

For example, if there are two tables, one listing all Employees by ID, and another listing their payroll information, the `FOREIGN KEY` can ensure that every row in the payroll table corresponds to a valid employee in the master Employee list. |


## LESSON 17: Altering tables

ALTER TABLE : update your corresponding tables and database schemas.
CREATE TABLE : adding a new column is similar to the syntax when creating new rows.
DROP : is as easy as specifying the column to drop.
RENAME TO : to rename the table.

## SQL Lesson 18: Dropping tables

DROP TABLE :  to remove an entire table including all of its data and metadata.

DROP TABLE IF EXISTS mytable;

