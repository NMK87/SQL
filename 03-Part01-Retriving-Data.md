# Retrieval

## Select clause 

In SQL databases, we retrieve data by writing <b>SELECT</b> statements, which are often called queries.
```
SELECT column1, column2,....

From table_name;
```
OR
```
SELECT * 

FROM table_name;

SELECT * 
FROM table_name 
WHERE condition;
```

Example:
```
Select Emp_id FROM Employee;

Select * FROM Employee;

Select * FROM Employee WHERE Emp_id=1;
```
## Where clause

A <b>Where </b>clause determines whether a row of data should be included in the results by checking specific column values.
```
SELECT column_1, column_2, …

FROM mytable

WHERE condition_1
    AND/OR condition_2
    AND/OR …;
```
The OR and AND logical keywords can be combined to form more complex clauses 

Example:
```
SELECT Emp_id, Emp_name

FROM Employee

WHERE salary > 40000;
```

# Operators

Below are some useful operators that you can use for numerical data :

| Operator | Descrption | Examples
|:---|:---|:---
=,!=,<,<=,>,>=| Numerical operators| col1 >= 5|
AND | Both conditions must be true| col1>2 AND Col2=="Git"|
OR| Either of the conditions must be true| col1>2 OR Col2=="Git"|
BETWEEN...AND| Range of numeric values| col1 BETWEEN 20 AND 30|
NOT BETWEEN...AND| Numbers not in range| col1 NOT BETWEEN 20 AND 30|
IN | If any numeric value exsits| col1 IN(1,2,3)|
NOT IN| If any numeric value doesnt exist| col1 NOT IN(1,2,3)|

Few exmaples containing these operators are: 
```
1. Select * FROM Employee

   WHERE Emp=salary BETWEEN 2000 AND 4000;
```

```
2. Select * FROM Employee

   WHERE Date_of_Birth >= '1990-01-01';
```
Note : Date format must be as YYYY-MM-DD.

OR 
```
3. Select * FROM Employee

   WHERE Date_of_Birth BETWEEN '1990-01-01' AND '2000-01-01';
```

```
4. Select * FROM Employee

   WHERE Emp_city IN ('Delhi','Pune','Karnataka');
```
