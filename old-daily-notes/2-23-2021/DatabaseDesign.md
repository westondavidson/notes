# Database Design
- how do we actually design these tables?

- data definition languages, DDL, remember it's create alter drop!

# constraints - what data belongs to a column!
- you can't put an incorrect type in a column that enforces a type!

1. data type
1. not null
1. unique
1. check - add some logic to check some constraint - salary, check you can't input negative values in it
1. Exclusion
1. primary key - unique and not null
1. foreign key

- PK and FK establish relationship in database

# keys
- keys are used to identify a data set, and to establish relationships between entities
- candidate key
    - minimal set of columns in a table that every other column depends on
    - a key that can uniquely identify a row in a table
- primary key
    - unique identifier for a row in a table
    - we make our candidate key our primary key
- foreign key
    - a foreign key is some other table's primary key to establish a relationship to another row in another table
- composite key
    - any key that's more than one column


# referential integrity
- refers to the accuracy and consistency of a data within a relationship
- whenever a foreign key value is used it must reference a valid, existing primary key in the parent table
- you always want to reference a valid existing primary key in the related table


# relationships in SQL
- relationships in SQL are defined by multiplicity!
- 1:1 
    - two sets of data are unique to each other
    - ex: a wizard can have one apprentice, and an apprentice can only follow one wizard
    - separate the entities with a FK reference that is unique and not null
1:m
    - one set of data can have many instances of the other data set
    - ex: a wizard can have many apprentices, but apprentices can only follow one wizard
    - two tables, FK that is not unique
m:m
    - both data sets can have many instances of each other
    - in a wizard school, a wizard can teach many apprentices, and apprentices can learn from many wizards
    - you would use 3 tables, one of which is a join/junction table.
        basically a 1:m relationship from the wizard table, and a 1:m relationship from the apprentice table
        - example: relating the location and the product, you can store a quantity in your junction table!


# ER Diagram
- shows the relationships of entity sets stored in a database
- use crows feet notiation to show relationships
- look back at ppt for example of ER diagram
- circle means 0, crows feet means many

# why separate out data?
- can't insert some data without having some other data
- forced to delete some data in order to delete other data
- redundancy can mean accidential data consistency on updates
- if you store everything in one table, it can become convoluted
    - accidentially replace some data fields with incorrect names
- we want to refactor least number of lines possible, change at very top and then nothing else. Single record get changed, but nothing else has to!

# Normalization
- designing a database in a certain way to ease data management
- the art of decluttering data!
- there are 6 Normal Forms, but we mostly use only the first 3
1. 1NF
    - Atomic Values - shouldn't have like a "list" in a single column. Each column should have one value.
    - No repeating groups of columns
    - No duplicate rows - must have some sort of unique identifier for each row - a primary key!
1. 2NF
    - Has to be 1NF
    - no partial dependencies - every column in your row shouldn't depend on a part of the composite key for it to change. at some point, with different combinations of the two things, you'd have duplicate data.
    - no composite keys means you're 2NF by default
1. 3NF
    - has to be 2NF
    - no transitive dependencies - 
        - transative dependencies mean that multiple things inside a row would need to be altered for a single thing to be changed in that table


# normalization in a nutshell
- the table must depend on the key (1NF), the whole key (2NF), and nothing but the key (3NF)

- in a similar way we want to depend on abstractions rather than concrete implementations in c#, we depend on normalization in a DB to avoid having to rework multiple data entries entirely when a single change is made