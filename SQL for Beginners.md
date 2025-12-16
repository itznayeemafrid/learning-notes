
### Module 0 - Comment
- Use -- double hyphen at the beginning of a line to make it a comment.
```SQL
--This is a comment
```
---
### Module 1 - SELECT
- This selects column from a table.
- Use * asterisk to select all column. 
```SQL
SELECT Column_name, Column_name ...
SELECT *       --To select all column
```
---
### Module 2 - FROM
- To import selected data from a table.
```SQL
SELECT Column_name
FROM table1
```
---
### Module 3 - WHERE
- To add different conditions.
- The result will be shown based of this condition.
- All these (=, !=, <, <=, >, >=) Standard numerical operators can be used.
```SQL
SELECT Movie_Title, Year
FROM Movies
WHERE Year > 2010
```
---
- Use `AND` , `OR` for more complex condition (`num_wheels >= 4 AND doors <= 2`).
- Below are some useful operators (*`for numerical data`*):

| Operator            | Condition                              | SQL Example                     |
| ------------------- | -------------------------------------- | ------------------------------- |
| =, !=, <, <=, >, >= | Standard numerical operators           | `col_name != 4`                 |
| BETWEEN … AND …     | Number is within range (inclusive)     | `col_name BETWEEN 1.5 AND 10.5` |
| NOT BETWEEN … AND … | Number is not within range (inclusive) | `col_name NOT BETWEEN 1 AND 10` |
| IN (…)              | Number exists in a list                | `col_name IN (2, 4, 6)`         |
| NOT IN (…)          | Number does not exist in a list        | `col_name NOT IN (1, 3, 5)`     |
- Below are some useful operators (*`for string data`*):

| Operator   | Condition                                         | Example                                                       |
| ---------- | ------------------------------------------------- | ------------------------------------------------------------- |
| =          | Case sensitive exact string comparison            | `col_name = "abc"`                                            |
| != or <>   | Case sensitive exact string inequality comparison | `col_name != "abcd"`                                          |
| LIKE       | Case insensitive exact string comparison          | `col_name LIKE "ABC"`                                         |
| NOT LIKE   | Case insensitive exact string inequality          | `col_name NOT LIKE "ABCD"`                                    |
| %          | Matches zero or more characters (with LIKE)       | `col_name LIKE "%AT%"` (matches "AT", "ATTIC", "CAT", "BATS") |
| _          | Matches a single character (with LIKE)            | `col_name LIKE "AN_"` (matches "AND", not "AN")               |
| IN (…)     | String exists in a list                           | `col_name IN ("A", "B", "C")`                                 |
| NOT IN (…) | String does not exist in a list                   | `col_name NOT IN ("D", "E", "F")`                             |
### Module 4 - DISTINCT
- To remove duplicates from selected all columns.
```SQL
SELECT DISTINCT Column_name, Column_name
FROM table1
```
---
### Module 5 - ORDER BY
- To order list.
- Use `ASC` , `DESC` to order by ascending or descending.
```SQL
SELECT Roll, Name
FROM Students
ORDER BY Roll ASC
```
---
### Module 6 - LIMIT & OFFSET
- `LIMIT` is used to **show a certain number of rows**.
- `OFFSET` is used to **skip rows from the top**.
```SQL
SELECT Roll, Name
FROM Students 
LIMIT 5  OFFSET 10  
```
---
### Module 7 - Dot (`.`) Notation
- The dot `.` is used to **specify which table a column belongs to**.
- Format: `TableName.ColumnName`
```SQL
SELECT Students.Name, Enrollments.Course 
```
---
### Module 8 - JOINs
- `JOIN` is used to **combine rows from two or more tables**.

**INNER JOIN**
- Shows rows **only when there is a match in both tables**.
```SQL
SELECT Students.Name, Enrollments.Course  
FROM Students  
INNER JOIN Enrollments  
  ON Students.ID = Enrollments.Student_ID 
```
---

**LEFT JOIN (or LEFT OUTER JOIN)**
- Shows **all rows from the left table**, and matched rows from the right table.
- If no match, right table shows `NULL`.
```SQL
SELECT Students.Name, Enrollments.Course  
FROM Students  
LEFT JOIN Enrollments  
  ON Students.ID = Enrollments.Student_ID 
```
---

**RIGHT JOIN (or RIGHT OUTER JOIN)**
- Shows **all rows from the right table**, and matched rows from the left table.
- If no match, left table shows `NULL`.
```SQL
SELECT Students.Name, Enrollments.Course  
FROM Students  
RIGHT JOIN Enrollments  
  ON Students.ID = Enrollments.Student_ID 
```
---

**FULL JOIN (or FULL OUTER JOIN)**
- Shows **all rows when there is a match in one of the tables**.
- If no match, the missing side shows `NULL`.
```SQL
SELECT Students.Name, Enrollments.Course  
FROM Students  
FULL JOIN Enrollments  
  ON Students.ID = Enrollments.Student_ID 
```
---
### Module 9 - IS NULL & IS NOT NULL
- Use `IS NULL` to **check if a column has no value** (empty or missing).
- Use `IS NOT NULL` to **check if a column has a value** (not empty).
```SQL
SELECT Name, Email
FROM Students
WHERE Email IS NULL;   -- shows students without an email`
```
---
### Module 10 - AS (Alias)
- `AS` is used to **give a temporary name (alias) to a column or table** in the result.
```SQL
SELECT Name AS Student_Name, Age AS Student_Age
FROM Students;
```
---
### Module 11 - Expressions (Math & Operations)
- You can do **math or other operations directly in SQL**.
- These can be used in `SELECT`, `WHERE`, and other clauses.
```SQL
SELECT particle_speed / 2.0 AS Half_Speed
FROM Particles;     --The result will show in a column named Half_Speed
```
---
### Module 12 - ABS (Absolute Value)
- `ABS()` is used to **return the absolute (non-negative) value** of a number, removing any negative sign.
```SQL
SELECT ABS(-25) AS Absolute_Value; -- Output: 25`
```
---
### Module 13 - Aggregate Functions
- **Aggregate functions** help you **summarize data** from many rows into **one single result**.
- If no `GROUP BY` is used, the function runs over **all rows**.
 ```SQL
SELECT SUM(Salary) AS Total_High_Earners
FROM Employees
WHERE Salary > 50000;
```

**Common Aggregate Functions:**

|Function|Description|
|---|---|
|`COUNT(*)` or `COUNT(column)`|Counts total rows (or non-NULL values in a column).|
|`MIN(column)`|Returns the **smallest** value in the column.|
|`MAX(column)`|Returns the **largest** value in the column.|
|`AVG(column)`|Calculates the **average** of numeric values.|
|`SUM(column)`|Adds up all numeric values in the column.|

---
### Module 13 - GROUP BY
- `GROUP BY` **groups together rows that have the same value** in a column.
```SQL
SELECT Department, AVG(Salary) AS Avg_Salary
FROM Employees
GROUP BY Department;
````
---
### Module 14 - HAVING
- `HAVING` is used to **filter groups** after they’ve been created by `GROUP BY`. 
- It's like `WHERE`, but instead of filtering individual rows, it filters the **results of grouped data**.
 ```SQL
SELECT Department, AVG(Salary) AS Avg_Salary
FROM Employees
GROUP BY Department
HAVING AVG(Salary) > 60000;
```
---
### Module 15 - SQL Query Execution Order
- SQL runs queries in this order:

| Step | Clause       | What It Does               |
| ---- | ------------ | -------------------------- |
| 1    | FROM/JOIN    | Get data from tables       |
| 2    | WHERE        | Filter rows                |
| 3    | GROUP BY     | Group rows                 |
| 4    | HAVING       | Filter groups              |
| 5    | SELECT       | Choose columns             |
| 6    | DISTINCT     | Remove duplicate rows      |
| 7    | ORDER BY     | Sort results               |
| 8    | LIMIT/OFFSET | Limit number of rows shown |

---
### Module 16 - Database Schema

- A **database schema** is the **blueprint** of a table.
- It defines the **columns** in the table and the **type of data** each column can hold.
- The schema helps keep data **organized** and **consistent**.
```TEXT
Movies table:
	- Title (text/string)
	- Year  (number/integer)
```
---
### Module 16 - Inserting Rows (`INSERT`)
- The **database schema** defines the structure of a table — its columns and their data types.
- Use the `INSERT` statement to **add new rows** to a table.
---
#### Insert all columns:
```SQL
INSERT INTO table_name
VALUES (value1, value2, value3),
       (value4, value5, value6);
```
#### Insert specific columns:
```SQL
INSERT INTO table_name (column1, column2)
VALUES (value1, value2),
       (value3, value4);
```
#### Insert with expressions:
```SQL
INSERT INTO boxoffice (movie_id, rating, sales_in_millions)
VALUES (1, 9.9, 283742034 / 1000000);
```
---
### Module 17 - Updating Rows (`UPDATE`)
- `UPDATE` is used to **change data** in existing rows of a table.
- You must:
    - Say **which table** to update
    - Set **which columns** to change
    - Add a `WHERE` condition to **choose the right rows**
```SQL
UPDATE Movies
SET rating = 9.5
WHERE id = 3;
```
---
### Module 18 - Deleting Rows (`DELETE`)
- `DELETE` is used to **remove rows** from a table.
- You must:
    - Say **which table** to delete from
    - Add a `WHERE` clause to **specify which rows** to delete
```SQL
DELETE FROM Movies
WHERE id = 5;
```
---
### Module 19 - Creating Tables (`CREATE TABLE`)
- `CREATE TABLE` is used to **make a new table** in the database.
- You define:
    - Column **names**
    - Their **data types**
    - Optional **constraints** (rules for valid data)
    - Optional **default values**
```SQL
CREATE TABLE movies (
	id INTEGER PRIMARY KEY,
	title TEXT,
	director TEXT,
	year_released INTEGER,
	length_minutes INTEGER
);
```

#### Common Data Types:

|Type|Description|
|---|---|
|`INTEGER`, `BOOLEAN`|Whole numbers, true/false|
|`FLOAT`, `DOUBLE`, `REAL`|Decimal numbers (for precise values)|
|`TEXT`, `VARCHAR(n)`|Strings and text|
|`DATE`, `DATETIME`|Dates and timestamps|
|`BLOB`|Binary data (e.g., images, files)|

---
#### Common Constraints:

|Constraint|What It Means|
|---|---|
|`PRIMARY KEY`|Uniquely identifies each row|
|`AUTOINCREMENT`|Automatically increases number on each insert|
|`UNIQUE`|Value must not repeat across rows|
|`NOT NULL`|Value is required (can’t be empty)|
|`CHECK (cond)`|Value must pass a rule (e.g., `CHECK(age > 0)`)|
|`FOREIGN KEY`|Value must exist in another table's column|

---
### Module 20 - Altering Tables (`ALTER TABLE`)
- `ALTER TABLE` lets you **change the structure** of an existing table.
- You can **add**, **remove**, or **rename** columns, or even **rename the table** itself.
#### Add a Column:
```SQL
ALTER TABLE table_name
ADD column_name DataType [Constraint] DEFAULT default_value;
```
#### Remove a Column:
```SQL
ALTER TABLE table_name
DROP column_name;
```
#### Rename a Table:
```SQL
ALTER TABLE old_table_name
RENAME TO new_table_name;
```
#### Example
```SQL
ALTER TABLE movies
ADD budget INTEGER DEFAULT 0;

ALTER TABLE movies
DROP length_minutes;

ALTER TABLE movies
RENAME TO film_list;
```
---
### Module 21 - Dropping Tables (`DROP TABLE`)
- `DROP TABLE` is used to **completely remove a table** from the database — including all its data **and** structure.
- `IF EXISTS` prevents an error if the table doesn’t exist.
```SQL
DROP TABLE IF EXISTS table_name;
```
---

>[!tip]
>- **Rows = records / entries**
>- **Columns = data fields / attributes**

