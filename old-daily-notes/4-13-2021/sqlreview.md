## 4 sublanguages of sql
- DDL - data definition language
    - define database schema
        - CREATE, ALTER, DROP, TRUNCATE
- DML - data manipulation language
    - deal with manipulating data present in a datbase
        - INSERT, UPDATE, DELETE, MERGE
- TCL - transaction control language
    - commands which deal with transactions in the database
        - COMMIT, ROLLBACK, SAVEPOINT
- DCL - data control language
    - deals with commands that provide rights, permissions, and other controls through the dbms
        - GRANT, REVOKE

## what do you mean by DBMS?
- a DBMS is a software application that interacts with the user, applications and the database itself to capture and analyse data.
- DBMS can have different vendor dialects depending on which is being used

## what is a table, what is a field?
- a table is a collection of data that forms rows and columns
- a field refers to the number of columns in a table

## what are joins in sql
- a join clause is used to combine rows from two or more tables based on a related column between them
- inner join, full join, left join, right join

## a primary key
- a primary key is the column which uniquely describes the entries in a table

## what are constraints?
- constraints are used to specify the limit on the data type of the table. things like not null, unique, check, default, index


## difference between SQL and mySQL?
- sql is the standard language, while mysql is a dbms!

## what is a unique key
- uniquely identifies a single row in the table
- duplicate values are not allowed

## what is a foreign key
- creates referential integrity by enforcing a link between the data in two tables

## data integrity
- defines the accuracy and consistency of data across the relational database

## sql query to display current date
SELECT GETDATE();

## different types of joins
- inner join, full join, left join, right join
- inner join returns records with matching values in both tables
- full join returns all records which have a match in left or right table
- left join returns records from left table and those that satisfy the condition from the right table
- right join returns records from right table and those that satisfy the condition from the left table


## entities and relationships
- an entity is any table that is stored in a database
- a relationship is the link between one table and another, provided by a foreign key and a specific type of relationship

## what is an index
- an index refers to a performance tuning method that allows faster retrieval of records from the table

## normalization
- the process of organizing data to avoid duplication and redundancy
- efficient data access, better organization, reduction of redundant and duplicate data

## drop command vs truncate
- drops the table and cannot be rolled back from database
- truncate removes all rows from the table

## types of normalization
- 1nf, 2nf, 3nf

- 1nf - records have a single value, no duplicate columns
- 2nf - single column primary key, no partial dependencies
- 3nf - db is first in 2nf and has no transitive functional dependencies
- the key, the whole key, and nothing but the key


## ACID property in a database
- Atomicity - transactions either completes or fails - nothing is done halfway
- Consistency - a transaction never leaves the database without completing it's task
- Isolation - concurrency control - a transaction is not interacting with another concurrent transaction
- Durability - if a transaction is complete, it will be committed to the database no matter any circumstance
- used to ensure that transactions are persisted reliably in a database

## triggers in sql
- special type of stored procedure that is defined to execute automatically in place or after data modifications

## types of operators in SQL
- arithmetic, bitwise, comparison, compound, and logical operators

## are null values same as 0 or blank space?
- NO, a null represents a value which has not been assigned, while a zero is a number and a blank space is a character

## subquery in SQL
- a subquery in sql is a query inside another query.
    - the subquery is always executed first, then the result of the subquery is passed to the main query

## display name of employees that begin with A
- SELECT * FROM Table_name WHERE EmpName like'A%'

## query to get third highest salary of an employee from employee_table
SELECT TOP 1 salary
FROM(
    SELECT TOP 3 salary
    FROM employee_table
    ORDER BY salary DESC
) AS emp
ORDER BY salary ASC;

## group functions/aggregate functions
- work on a set of rows and returns one result per group
- commonly used aggregate functions:
    - AVG
    - COUNT
    - MAX
    - MIN
    - SUM
    - VARIANCE

## relationships, what are the different types?
- relationships are links between entities that have something to do with each other
- types of relationships:
    - one to one
    - one to many
    - many to many
    - self referencing - two columns within the same table reference each other

## between and in condition operators
- between - display rows based on a range of values in a row
- in - check for values contained in a specific set of values

## sql functions are used for...
- performing normal function purposes! modifying data, manipulating output, converting data types, and formatting output

## MERGE statement
- allows conditional updates or insertions of data into a table

## WHERE clause vs HAVING clause
- HAVING - can be used only with SELECT statement, and is usually used in a GROUP BY clause
- WHERE - applied to each row before they are a part of the GROUP BY function in a query

## case manipulation functions
- LOWER('STRING')
- UPPER('STRING')
- INITCAP('STRING')

## operators in SQL
- UNION
    - combines rows from two separate queries
- INTERSECT
    - keeps only rows which are common in both queries
- MINUS
    - keeps only rows from the query that are not included in the query which is being subtracted

## ALIAS command
- an alias is a name that has been given to a table or column, which can be referred to in the WHERE clause to identify that particular table or column


## aggregate and scalar functions
- aggregate functions
    - used to evaluate math calculations from a number of entries and returns a single value
    - examples: avg(), sum(), max(), count()
- scalar functions
    - return a single value based on an input value
    - Examples: UCASE(), NOW()

## how to fetch alternate records from a table
- you can use the mod operator to only select rows with a specific remainder
    - example: display even number rows from a table of students and display studentids
        -SELECT studentId from (Select rowno, studentId from student) where mod(rowno, 2)=0

## operator used in query for pattern matching
- the LIKE operator!
- example: SELECT * FROM students WHERE studentname LIKE 'a%'
    - select all entries in students where the student name begins with the letter a, and is followed by 0 or more characters
    - the % symbol means zero or more characters
    - the _ symbol mean an exact match

## first 5 characters from a string
- you can use SUBSTRING() for this!
    - example:
        - SELECT SUBSTRING(studentname,1,5) as studentname FROM student
        - this will select the first five characters in a string


## what is a view?
- a view is a virtual table that consists of a subset of data contained in a data.
- views can combine data from multiple tables
- not a real table, just a view!

## what are views used for?
- restrict access to some data
- makes complex queries simple
- provides different views of same data

## what is a stored procedure?
- a function which consists of many SQL statements to access the database
- several SQL statements are consolidated and stored
- this way, you don't have to write the query again! if you have a sproc, you don't have to write the query again

## advantages of sprocs
- can be used as a modular programming system
- supports faster execution

## disadvantages of sprocs
- sprocs can only be executed in the database, not from externally

## user defined functions
- scalar functions
- multi-statement valued functions
- table valued functions

## auto increment in SQL
- allows user to create a unique number that is generated whenever a new record is inserted into the table
- IDENTITY keyword used in SQL server

## STUFF and REPLACE functions
- STUFF is used to overwrite existing characters, or insert a string into another string
    - example: STUFF(string_expression, start, length, replacement_characters)
    - stuffs the new replacement characters in the specified location
- REPLACE is used to replace all occurrences of a set of existing characters
    - example: REPLACE(string_expression, search_string, replacement_string)


