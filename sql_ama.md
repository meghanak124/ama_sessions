# SQL & Programming Short Notes

## 1. List Aggregate Functions in SQL

-   COUNT() -- Counts rows
-   SUM() -- Adds values
-   AVG() -- Finds average
-   MIN() -- Smallest value
-   MAX() -- Largest value
-   STRING_AGG() / GROUP_CONCAT() -- Combines text values

------------------------------------------------------------------------

## 2. Difference Between Tuple and List (Python)

  List                   Tuple
  ---------------------- ---------------------------
  Mutable (can change)   Immutable (cannot change)
  
  Uses []              Uses ()
  
  Slower                 Faster

------------------------------------------------------------------------

## 3. Subqueries in SQL

A subquery is a query inside another query.
It runs first and its result is used by the main query.

Example: SELECT name FROM students

WHERE marks > (SELECT AVG(marks) FROM students);

------------------------------------------------------------------------

## 4. ORDER BY in SQL

Used to sort results. 

- ASC → Ascending (default) 

- - DESC → Descending

Example: SELECT * FROM students ORDER BY marks DESC;

------------------------------------------------------------------------

## 5. GROUP BY in SQL

Groups rows with same values. Used with aggregate functions.

Example: SELECT department, COUNT(*) FROM employees GROUP BY department;

------------------------------------------------------------------------

## 6. How to Sort in SQL

Use ORDER BY. Example: SELECT * FROM table_name ORDER BY column_name ASC;

------------------------------------------------------------------------

## 7. What is rsync?

rsync is a Linux command used to copy and sync files between systems
efficiently.

------------------------------------------------------------------------

## 8. LIKE in SQL

Used for pattern matching.
-   % → Any number of characters\
-   _ → Single character

Example: SELECT \* FROM students WHERE name LIKE 'A%';

------------------------------------------------------------------------

## 9. WHERE vs HAVING

  WHERE                   HAVING
  ----------------------- ---------------------
  Filters rows            Filters groups
  
  Used before GROUP BY    Used after GROUP BY
  
  Cannot use aggregates   Can use aggregates

------------------------------------------------------------------------

## 10. LIMIT in SQL

Restricts number of rows returned.

Example: SELECT \* FROM students LIMIT 5;

------------------------------------------------------------------------

## 11. SQL vs NoSQL

  SQL                 NoSQL
  ------------------- -----------------------------------------
  Structured tables   Flexible structure
  Fixed schema        Dynamic schema
  Uses SQL language   Uses different models (JSON, key-value)

------------------------------------------------------------------------

## 12. SQL is Procedural or Non-Procedural?

SQL is Non-Procedural (Declarative).
You tell what you want, not how to get it.

------------------------------------------------------------------------

## 13. Can We Use List as Keys in Dict?

No.
Lists are mutable. Dictionary keys must be immutable (like tuple,
string, int).

------------------------------------------------------------------------

## 14. DML Commands in SQL

DML = Data Manipulation Language

-   INSERT -- Add data
-   UPDATE -- Modify data
-   DELETE -- Remove data
-   SELECT -- Retrieve data

### UPDATE Example:

UPDATE students
SET marks = 90
WHERE id = 1;

------------------------------------------------------------------------

## 15. Need of Primary Key

-   Uniquely identifies each row
-   Prevents duplicate records
-   Cannot be NULL
-   Helps in relationships (foreign keys)

------------------------------------------------------------------------

## 16. How to Sort Dictionary by Values (Python)

Example:

sorted_dict = dict(sorted(my_dict.items(), key=lambda item: item\[1\]))

This sorts dictionary based on values in ascending order.
