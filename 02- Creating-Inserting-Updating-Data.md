# DataTypes

Initially we have Data Types in SQL, few of the most used commands are as follows,

<b>CHAR(50)</b> - Specifies the column length upto 50 characters-  can be from 0 to 255.

<b>INT(11)</b> - Integer with maximum 11 digits.

<b>VARCHAR(50)</b> - Variables containes special characters like letters, numbers, and special characters.

<b>DATE</b> - To store dates

<b>TIME</b> - It stores time.

## Constraints

<b>Primary Key</b>- The values in this column are unique, and each value identifies a unique row in this table.

<b>Foreign Key</b>- Each value in this column must correspond to at least one value in a column in another table.

<b>UNIQUE</b>- The value in this column has to be unique, and you cannot insert another row in the table with the same value as this column.

<b>NOT NULL</b>- The inserted value must not be 'NULL'.

## CREATE STATEMENT

Create is used to a new table

Syntax: CREATE TABLE table_name (data type column_names ....);

We create a new table by specifying their datatypes as well.

Example:

 CREATE TABLE Employee(Emp_id int, Emp_name VARCHAR, Age int);

## INSERT STATEMENT

Inserting new records to the table

INSERT INTO table_name (column1, column2,...)

values (value1, value2,..);

INSERT INTO table_name

values (value1, value2,..);

Example:

INSERT INTO Employee (Emp_id,Emp_name,Age)

values (1,Neha,10);

values (2,Keerthana,20);

Order of values doesnt matter.
We can also insert values to specified columns as well.

## UPDATE STATEMENT

By using update statement we can modify the existing table

UDPATE table_name

SET column1=value, column2=value,..

where condition;

Example: 

UPDATE Employee

SET Emp_name='Ananya'

where Emp_id=1;

Note- Where clause specifes which column must be updated, if where clause to missed entire records will be updated.

## DELETE STATEMENT

It deletes the existing record in a table.

DELETE FROM table_name WHERE condition;

Example:

 DELETE FROM Employee WHERE Emp_name='Neha';
