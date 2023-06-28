# Data Access
- select statement
    - used for retrieving data from database
    - select statement has many clauses
        - select
        - from - specifies what table to query
        - where - defines a condition, filtering out rows
        - group by - aggregates multiple rows into one, if they have the same values (group by last name, dept, etc)
        - having - defines a condition for filtering after group by
        - order by - specifies the sort order of the results
    - these clauses go in order from top to bottom


# Joins
- combine data back together in a query that was spread out in multiple tables
- kinds of joins
    - full - every row in left table to every row in right table
    - inner - only join data that matches condition
    - left - left table to data that exists on right table
    - right - right table to data that exists on left
    - cross join - implements the cartesian product - everything ?

# set operations
- used to combine results of select queries
- joins combine data from different tables, set operations combine result sets
- union
    - gives all rows that are found in either query without duplicates
- union all
    - gives you all rows found in either query
- review to see others


# subqueries
- use one query to filter results, and then do another to filter those results!
- sometimes, the most natural way to express a query is with condition based on another query
- list these out


