# databases
- the better way to store things!
- organized collection of structured information or data, stored electronically.
- controlled by a database management system DBMS
    - serves as an interface between your database and the end users
    - the DBMS actually manages how things are retrieved and manipulated
- together, the data and the DBMS, along with applications associated with them are referred to as a database system, often shortened to just database.

# relational databases
- type of database that stores and provides data based on the data being related to one another
- stores data into relations/tables
- if our data is wrapped in an object in C#, it probably means that's the relation/table in the DB!

# SQL
- structured query language
- used by all relational databases to query, manipulate, and define data, and to provide access control
- sql lets you talk to your db :) both manipulate and retrieve
- it is declarative
    - say what we want! we don't care how it's done, just that it's done - this is determined by the DBMS
- SQL architecture
    - query processing translates from our high level queries to low level expressions that can be used at physical level of file system. The query language processor converts your query from our language to the computer's language for execution
    - DBMS engine provides access to the data in the database
    - then the physical database is accessed through the DBMS
    