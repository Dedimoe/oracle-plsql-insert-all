# oracle-plsql-insert-all (bulks insert)
### syntax for the INSERT ALL statement in Oracle/PLSQL

Syntax:

The syntax for the INSERT ALL statement in Oracle/PLSQL is:
```
INSERT ALL
  INTO mytable (column1, column2, column_n) VALUES (expr1, expr2, expr_n)
  INTO mytable (column1, column2, column_n) VALUES (expr1, expr2, expr_n)
  INTO mytable (column1, column2, column_n) VALUES (expr1, expr2, expr_n)
SELECT * FROM dual;
```
### Parameters or Arguments

- *mytable*: The table to insert the records into.
- *column1, column2, column_n*: The columns in the table to insert values.
- *expr1, expr2, ... expr_n*: The values to assign to the columns in the table.


Example - Insert into One Table
```
INSERT ALL
  INTO companies (c_id, c_name) VALUES (1000, 'Apple')
  INTO companies (c_id, c_name) VALUES (2000, 'Oracle')
  INTO companies (c_id, c_name) VALUES (3000, 'Novell')
SELECT * FROM dual;
```
This is equivalent to the following 3 INSERT statements:
```
INSERT INTO companies (c_id, c_name) VALUES (1000, 'Apple');
INSERT INTO companies (c_id, c_name) VALUES (2000, 'Oracle');
INSERT INTO companies (c_id, c_name) VALUES (3000, 'Novell');
```
