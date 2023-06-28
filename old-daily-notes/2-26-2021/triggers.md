# trigger

- a set of actions that a database performs once the requirements are met
- when a customer data has been added, an email is automatically sent (triggered)

# types of SQL Triggers
- there are ddl, dml, and logon triggers
- ddl, triggers caused by cretae alter and drop statements
- dml event occur on data updates
- logons

-- ddl trigger
- ddl trigger on drop could roll back

- clr ddl trigger
- executes one or more methods written in managed code that are members of an assembly
- 

before, after, instead of with dml triggers
- before
- after(for) triggers run after statement is executed
    - never executed if a constraint violation occurs
- instead of
    - skip a dml statement

- logon events are used to control sql login security
- they log user login activity
- they also 

triggers are useful for 
- auditing
- enforcing business rules
- sort of like stored procedures, but you wouldn't be able to create a record in the database using a sproc
- 
- triggers are more automatic than stored procedures
- 