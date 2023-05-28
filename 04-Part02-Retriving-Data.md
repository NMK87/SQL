# Retriving Data From Database

# Operators

By continuing the first part, we see more operators that makes our retirival query more specific.

|Operators| Descriptions| Examples
|:--|:--|:--|
LIKE| This will compare any string in the database|col1 LIKE "xyz"|
NOT LIKE| This will not match any string in the database|
%| Used to match a sequence|col1 LIKE "%xyz"|
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