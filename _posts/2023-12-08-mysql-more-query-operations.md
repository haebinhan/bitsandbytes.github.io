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

```sql
ALTER TABLE table_name
ADD ColumnName varchar(255)
DROP COLUMN columnName
MODIFY COLUMN columnName datatype;
```


<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### Difference
The result of a difference is all tuples from the first given relation that do not exist in the second given relation. The relations, like a union, must be union compatible. A difference, however, is NOT commutative, and the order matters. `A - B` does NOT equal `B - A`. 

Syntax:
`A-B`
`A DIFFERENCE B`


<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### Intersection
An intersection is a relation that contains the tuples that exist in BOTH relations supplied. In a Venn diagram, this would be the middle section of two intersecting sircles. Relations must be union compatible. Like unions, intersections are commutative. This means that `A INTERSECT B` is the same as `B INTERSECT A`. 


If the tables or statements aren't union compatible, an intersection cannot be used. Instead, a `JOIN` can be used. 
```sql
FROM student INNER JOIN part_timers
ON student.stuID = part_timers.stuID;
```
See more on [Joins](#joins) below. 


<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### Product
A product gives a set of tuples from combining each tuple in one relation with each tuple in another relation. It's also called a *Cartesian product* and a *Cross product*. 

Syntax: `A x B` and `A PRODUCT B`. It is typically used with other operations such as JOIN. 

With a relation that has 5 rows and another relation with 5 rows, the resulting relation would display 25 rows. 


<div align="center">── ⋅ ⋅ ── ✩ ── ⋅ ⋅ ──</div>


#### Joins
Types of joins: 


<div align="center">────── ⋅ ⋅ ──── ✩ ──── ⋅ ⋅ ──────</div>


### Subqueries
Subqueries allow for two queries to be combined. 



<div align="center">────── ⋅ ⋅ ──── ✩ ──── ⋅ ⋅ ──────</div>

