

```SELECT column_name, column_name``` <br>
```FROM table_name;```

```SELECT *``` --> select all columns<br>
```FROM table_name``` <br>
```LIMIT 10``` --> limit the records

```SELECT DISTINCT column_name``` --> select only unique values<br>
```FROM table_name```

```SELECT COUNT(*)``` --> returns no of rows in the table <br>
```FROM table_name;```

```SELECT COUNT (column_name)``` --> returns no of rows in the colum <br>
```FROM table_name;```

```SELECT COUNT (DISTINCT column_name)``` --> returns no of distinct values from the column <br>
```FROM table_name;```

In SQL, the ```WHERE``` keyword allows you to filter based on both text and numeric values in a table. There are a few different comparison operators you can use: <br>
```=``` equal <br>
```<>``` not equal <br>
```<``` less than <br>
```>``` greater than <br>
```<=v``` less than or equal to <br>
```>=``` greater than or equal to <br>

Example: <br>
```SELECT column_name``` <br>
```FROM table_name``` <br>
```WHERE value_column_name > 2000;```

Example: <br>
```SELECT column_name1``` <br>
```FROM table_name``` <br>
```WHERE column_name2 = 'text';``` <br>

#### AND operator: display rows that meet few conditions <br>

Example: <br>
```SELECT column_name1``` <br>
```FROM table_name ```<br>
```WHERE value_column_name4 > 100``` <br>
```AND value_column_name3 < 2000;``` <br>

#### OR operator: display rows that meet one of the specified conditions. <br>

Example: <br>
```SELECT column_name``` <br>
```FROM table_name``` <br>
```WHERE value_column_name = 1994``` <br>
```OR value_column_name = 2000;``` <br>

Example: <br>
```SELECT column_name``` <br>
```FROM table_name``` <br>
```WHERE (value_column_name = 1994 OR value_column_name = 1995)``` <br>
```AND (column_name1 = 'PG' OR column_name1 = 'R'); ```<br>
