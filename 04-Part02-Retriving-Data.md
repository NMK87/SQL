# Retriving Data From Database

# Operators

By continuing the first part, we see more operators that makes our retirival query more specific.

|Operators| Descriptions| Examples
|:--|:--|:--|
LIKE| This will compare any string in the database|col1 LIKE "xyz"|
NOT LIKE| This will not match any string in the database|
%| Used to match a sequence in a string|col1 LIKE "%xyz"|
_| Used to match a single character| col1 LIKE "xy_"|

Examples:

```
1. SELECT * FROM Employee

   WHERE Emp_name LIKE "NEHA";

```
```
2. SELECT * FROM Employee

   WHERE Emp_name LIKE "%EH%";
```
```
3. SELECT * FROM Employee

   WHERE Emp_city LIKE "BANGLOR_";
```

# Distinct

A database may have unique data, but the results of any particular query may not be, hence <b>DISTINCT</b> keyword is used.

For example, movies can be different but release date can be same.

Syntax:
```
SELECT DISTINCT column1, column2, …
FROM table_name
WHERE condition;
```
Since distinct keyword will remove all duplicates rows, we uses <b>ORDER BY</b> to assign them accrodingly.

# Order By
An <b>ORDER BY</b> clause sorts rows alpha-numerically based on the value of the specified column.

Syntax:
```
SELECT column1, column2, …
FROM table_name
WHERE condition
ORDER BY column ASC/DESC;
```

Example:
```
SELECT DISTINCT Emp_city FROM Employee
ORDER BY Emp_city ASC;
```
In the above Example, Emp_city is printed without duplicates and aplhabets are arranged in ascending order.

Note: As we write queries its order of excution also matters the most.

## Order of Execution 

```
SELECT DISTINCT column1, column2
FROM table_name
    JOIN another_table
      ON table_name.column = table_name.column
    WHERE condition
    GROUP BY column
    HAVING condition
    ORDER BY column ASC/DESC
    LIMIT count OFFSET COUNT;
    
```
## Select 

SELECT part in the query are used for computation.

## From and Join's

 The clause includes subqueries and can create temporary tables under the hood that contain the columns and rows of the joined tables.
 For the query to be successful, the FROM clause and JOINs need to be executed first.

 ## Where

 WHERE constraints are applied to the individual rows, and rows that do not satisfy the constraint are discarded. In the FROM clause, each constraint can only access columns directly from the tables requested. 
 
 The SELECT part of the query may include Expressions whose execution depends on parts that have yet to be executed, so aliases are not accessible.

 ## Group By

 After using where clause on the rows, GROUP BY clause is used to group the common values in the column specified.

  As a result of grouping, rows will be left out with the unique values in the column. 

  ## Having

Once we use GROUP BY claue, Having clause constraints are applied on the grouped rows and the rows that doesnt meet the contraint will be discarded.

## Order By

If ORDER BY is getting used then the rows are sorted by the speccifed data in ascending or descending order. 

## LIMIT/ OFFSET 

Rows that are not in range are specified by LIMIT and OFFSET are ranged out leaving the finalized set of rows that are needed to the query.