# travelling salesman DB edition
- we have a table with no real normalization!
- let's convert it to normal form

- one table for products
fields: primary key product name
- routes
fields: primary key route

salesman:
fields:
name


- one salesman can have many products, and many products can be sold by one salesman

- one salesman can have many routes, and routes can be taken by many salesman

- salesman fields:
SalesmanID PK
name
phone number

- product fields:
ProductID PK
ProductName 


- route fields:
RouteID
routeName


Conjoined tables:

Composite Route table:
Salesman Table FK
RouteID FK
composite key - salesman plus routes FKs

Composite Product Table
ProductID FK
SalesmanID FK