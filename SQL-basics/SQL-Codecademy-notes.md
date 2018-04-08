### SQL basics

SQL, which stands for Structured Query Language, is a language for interacting with data stored in something called a relational database.

**Relational database** is database that organizes information into one or more tables.

**Table** is a collection of data organized into rows and columns.

Data types:
* Integer: positive or negative, a whole number
* Text: a text string
* Date: formatted as *YYY-MM-DD*
* Real: a decimal value

**SQL statement** - a text that SQL recognizes as a valid command

*Clauses* - perform specific tasks in SQL, written in capital letters.
*Parameters* - a list of columns, datatypes or values that are passed to the clause as an argument.

**Creating a table**

``CREATE TABLE celebs (``  <br>
``id INTEGER,``<br>
``name TEXT,``<br>
``age INTEGER``<br>
``);``

**Adding a row to a table**

``INSERT INTO celebs (id, name, age)`` <br>
``VALUES (1, 'Justin Bieber', 21);``

``INSERT INTO`` is a clause that adds the specified row or rows.

**Querying data**

``SELECT * FROM table_name``

``SELECT`` is a clause that indicates that the statement is a query. You will use SELECT every time you query data from a database.

``* `` - wildcard, allows to select every column in the table.

**Updating a row in the table**

``UPDATE celebs`` <br>
``SET age = 22`` <br>
``WHERE id = 1;`` <br>

``UPDATE`` is a clause that edits a row in the table.

``SET`` is a clause that indicates the column to edit.

**Adding column to a table**

``ALTER TABLE celebs`` <br>
``ADD COLUMN twitter_handle TEXT;``

``DELETE FROM celebs WHERE twitter_handle``<br>
``IS NULL;``

**Deleting data from a table**

``DELETE FROM`` statement deletes one or more rows from a table.

``CREATE TABLE awards (`` <br>
``id INTEGER PRIMARY KEY,`` <br>
``recipient TEXT NOT NULL,`` <br>
``award_name TEXT DEFAULT "Grammy");``

##### Constraints

Constraints that add information about how a column can be used are invoked after specifying the data type for a column.

``PRIMARY KEY`` columns can be used to uniquely identify the row. Attempts to insert a row with an identical value to a row already in the table will result in a constraint violation which will not allow you to insert the new row.

``UNIQUE`` columns have a different value for every row. This is similar to PRIMARY KEY except a table can have many different UNIQUE columns.

``NOT NULL`` columns must have a value. Attempts to insert a row without a value for a NOT NULL column will result in a constraint violation and the new row will not be inserted.

``DEFAULT`` columns take an additional argument that will be the assumed value for an inserted row if the new row does not specify a value for that column.

##### Generalizations

``CREATE TABLE`` creates a new table. <br>
``INSERT INTO`` adds a new row to a table. <br>
``SELECT`` queries data from a table. <br>
``UPDATE`` edits a row in a table. <br>
``ALTER TABLE`` changes an existing table. <br>
``DELETE FROM`` deletes rows from a table. <br>

##### Querying

``AS`` is a keyword in SQL that allows you to rename a column or table using an alias. It is important to remember that the columns have not been renamed in the table. The aliases only appear in the result.

Example:<br>
``SELECT name AS 'movies'`` <br>
``FROM movies;``

``DISTINCT`` is used to return unique values in the output. It filters out all duplicate values in the specified column(s).

``WHERE`` clause filters the result set to only include rows where the following condition is true.

Comparison operators: <br>
``=`` equal to <br>
``!=`` not equal to <br>
``>`` greater than <br>
``<`` less than <br>
``>=`` greater than or equal to <br>
``<=`` less than or equal to <br>

``LIKE`` is a special operator used with the WHERE clause to search for a specific pattern in a column.

Example:<br>
`SELECT * `<br>
`FROM movies`<br>
`WHERE name LIKE 'Se_en';`<br>

`_` - substitute of any individual character <br>
`%` - zero or more missing letters in the pattern, can be used before or after a pattern

`IS NULL` - select only rows that have no values<br>
`IS NOT NULL` - select only rows that have values

The `BETWEEN` operator can be used in a `WHERE`  clause to filter the result set within a certain range.

`BETWEEN` two letters is not inclusive of the 2nd letter. <br>`BETWEEN` two numbers is inclusive of the 2nd number.<br>
`AND` combines two conditions, both conditions must be true <br>

`AND` operator displays a row if all the conditions are true.<br>
`OR` operator displays a row if any condition is true.

`ORDER BY` is a clause that indicates you want to sort the result set by a particular column. Always goes after `WHERE`, if it's present.

`DESC` is a keyword used in ORDER BY to sort the results in descending order (high to low or Z-A).<br>
`ASC` is a keyword used in ORDER BY to sort the results in ascending order (low to high or A-Z).

Example: <br>
`SELECT name, year, imdb_rating` <br>
`FROM movies`<br>
`ORDER BY imdb_rating DESC;`

`LIMIT` is a clause that lets you specify the maximum number of rows the result set will have. Always goes at the very end of the query. Also, it is not supported in all SQL databases.

A `CASE` statement allows us to create different outputs (usually in the SELECT statement). It is SQL's way of handling if-then logic.

Example:<br>
`SELECT name,`<br>
`CASE`<br>
  `WHEN genre = 'romance' THEN 'Chill'`<br>
  `WHEN genre = 'comedy'  THEN 'Chill'`<br>
  `ELSE 'Serious'`<br>
 `END AS 'Mood'`<br>
`FROM movies;`

##### Generalizations
`SELECT` is the clause we use every time we want to query information from a database.<br>
`AS` renames a column or table.<br>
`DISTINCT` return unique values.<br>
`WHERE` is a popular command that lets you filter the results of the query based on conditions that you specify.<br>
`LIKE` and `BETWEEN` are special operators.<br>
`AND` and `OR` combines multiple conditions.<br>
`ORDER BY` sorts the result.<br>
`LIMIT` specifies the maximum number of rows that the query will return.<br>
`CASE` creates different outputs.

##### Functions
`COUNT`: count the number of rows <br>
`SUM`: the sum of the values in a column <br>
`MAX/MIN`: the largest/smallest value <br>
`AVG`: the average of the values in a column <br>
`ROUND`: round the values in the column, takes two arguments: column name and integer <br>

Example:<br>
`SELECT name, ROUND(price,0)`<br>
`FROM fake_apps;`<br>

Example:<br>
`SELECT ROUND(AVG(price),2)`<br>
`FROM fake_apps;`

`GROUP BY` is a clause in SQL that is used with aggregate functions. It is used in collaboration with the `SELECT` statement to arrange identical data into groups.

The `GROUP BY` statement comes after any `WHERE` statements, but before `ORDER BY` or `LIMIT`.


When we want to limit the results of a query based on values of the individual rows, use `WHERE`.

When we want to limit the results of a query based on an aggregate property, use `HAVING`.

`HAVING` statement always comes after `GROUP BY`, but before `ORDER BY` and `LIMIT`.


##### Generalizations

`COUNT`: count the number of rows <br>
`SUM`: the sum of the values in a column <br>
`MAX/MIN`: the largest/smallest value <br>
`AVG`: the average of the values in a column <br>
`ROUND`: round the values in the column

Aggregate functions combine multiple rows together to form a single value of more meaningful information.

`GROUP BY` is a clause used with aggregate functions to combine data from one or more columns.<br>
`HAVING` limit the results of a query based on an aggregate property.


### Joining tables

JOIN - *INNER JOIN*

SELECT COUNT (*) <br>
FROM newspaper; <br>

SELECT COUNT (*) <br>
FROM online; <br>

SELECT COUNT (*) <br>
FROM newspaper <br>
JOIN online ON newspaper.id = online.id;


LEFT JOIN

A left join will keep all rows from the first table, regardless of whether there is a matching row in the second table.
