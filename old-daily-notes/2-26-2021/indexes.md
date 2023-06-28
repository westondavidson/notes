# views
- views are a special version of tables in SQL that show data based on provided key value pairs?
- there are multiple types of views
    - simple, complex, inline, materialized
    - materialized view actually downloads data

- Materialized views
    - replicates data physically to reduce processing time from that view

# Indexes
- indexes are built on one or more columns of a table
- basically provide a pointer to a table

- indexing is sort of like an index in a book
- an index is a pointer to data that is stored within a database
- instead of looking in every row, we can use indexing to find a specific row
- instead of going through every row, we can specify a value to index by
- index creates a pointer to a table where the values that have said index exist

# views optimize searches
- views optimize data that is regularly retrieved

# indexed view
- an indexed view is like a view that is specified by a pointer

- views are stored sql statements

- if data is changing constantly, using an indexed view or view is not as fast as just searching


- schema binding is locking the view that the table is dependent upon so the table doesn't alter or delete columns, since the view is dependent on it.

- efcore and sql server stuff for quiz on monday.