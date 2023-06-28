# SQL
- structured query language
- used to manipulate and define data in a database
- used to provide structure to your database

# SQL sublanguage vs SQL dialect
- a dialect refers to the SQL variat used by a database vendor
- we'll be using sqlserver, so the dialect we'll be using is sqlserver
- sql sublanguages refer to the different categories of statements/commands in SQL
    - DDL, DML, DCL, TCL
        - some vendors say "SELECT" is a part of a 5th category, DQL, Data query language

# DDL
- data definition language
- used for creating database tables, define database structure
    1. create - creating tables
    1. alter - add column, constraints, etc
    1. drop - deletes table and drops data

# DML
- all operations on individual rows
- manipulating actual data in rows
    1. select
    1. insert
    1. update
    1. delete
- there are 3 commands asked aobut in QC
    - what's the difference between drop, delete, and truncate?
        - truncate means dropping all rows
        - drop destroys table structure and all data related to it
        - delete can be a single row, or all rows
        - delete deletes row by row, while truncate destroys everything
        - you can rollback from delete, but not truncate because truncate doesn't keep a record of deletions, but it's a faster process

# DCL
- Data Control Language
- for DB admin, changes db permissions
- grant and provoke

# TCL
- transaction control language
- groups sql commands and executes them as a batch
    1. commit
    1. savepoint
    1. rollback
    1. transact


