---
title: "MySQL - More Query Operations"
layout: post
date: 2023-12-08
feature_image: images/mysql_query_operations.png
tags: [mysql, database]
---

Following my post on [MySQL Query Operations](https://haebinhan.github.io/mysql-query-operations/), this post goes over more query operations.

<!--more-->

### GROUP BY, and COUNT()
Group by will display the results grouped by the selection. Count() will return the count for the parameter.

```sql
SELECT Year, COUNT(Year)
FROM Movie
GROUP BY Year;
```

<div align="center">────── ⋅ ⋅ ──── ✩ ──── ⋅ ⋅ ──────</div>


### LEFT JOIN
Left joins return records from the first table, and matching records from the second table.

```sql
SELECT table1.column2, table2.columnb, table2.columnc
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

<div align="center">────── ⋅ ⋅ ──── ✩ ──── ⋅ ⋅ ──────</div>


#### INNER JOIN

Inner join is the center of a venn diagram. This returns values existing in both.

```sql
SELECT table.column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

To inner join a table to itself, such as a table that has 
Employee
EmployeeID, FirstName, Lastname, ManagerID:

```sql
SELECT Employee.FirstName, Manager.Firstname
FROM Employee 
INNER JOIN Employee AS Manager
ON Employee.ManagerID = Manager.ID
ORDER BY Employee.FirstName;
```

<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### Subquery & AVG()

```sql
SELECT Name, Height
FROM Student
WHERE Height > 
   (SELECT AVG(Height)
   FROM Student)
ORDER BY Height;
```

<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>

#### ALTER
Alter is for changing attributes. Use [UPDATE](#update) for changing the actual values in the column.

```sql
ALTER TABLE table_name
ADD ColumnName varchar(255)
DROP COLUMN columnName
MODIFY COLUMN columnName datatype;
```


<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### INSERT INTO
You don't have to clarify the column names if you are adding all values. 

```sql
INSERT INTO tableName (column1, column2, column3...)
VALUES (value1, value2, value3...);
```

<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### UPDATE

```sql
UPDATE tableName
SET column1 = value1, column2 = value2, ...
WHERE condition;
```


<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### DELETE

```sql
DELETE FROM tableName WHERE condition;
```

<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### Joins
Types of joins: 


<div align="center">────── ⋅ ⋅ ──── ✩ ──── ⋅ ⋅ ──────</div>


### Subqueries
Subqueries allow for two queries to be combined. 



<div align="center">────── ⋅ ⋅ ──── ✩ ──── ⋅ ⋅ ──────</div>

