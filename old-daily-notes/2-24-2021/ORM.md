# ORM - Object Relational Mapper

- in DBs, data is stored in tables, in rows and columns
- Dilemma: converting data from DB into something c# would understand (objects!)
- ORMs are used to map data from a DB to an object in your program!!!
- the ORM we use is Entity Framework Core
    - this framework autogenerates partial classes for us that act as a class version of a relationship in your database
    - map objects from database to the models in business logic


# EF Core
- ORM for .net 5 core
- two ways to cconnect DB to your code:
    - db first
        - the DB structure already exists, classes are created based on the existing structure - using this for P0
    - code first
        - you create the db structure based on the classes in the code - using this for next project
        - this is for prototyping. you can regenerate your db structure based on the existing models.
    

# artifacts we'll be working with
- DBContext
    - this is basically our session with the database
    - we need to make our own implementation of this that is specific to our application
- connection string
    - used to connect to the db
    - host, username, password, db name
    - if the dbcontext is the session, the connection string are the credentials to connect to the db
- startup project
    - our project in dotnet!
- project
    - the actual target project we're connecting to. Our data layer!!

# before we begin:
- install stuff listed on ppt!!!
- packages in data layer
    - microsoft.entityframeworkcore.design
    - microsoft.entityframeworkcore.tools
    - microsoft.entityframeworkcore.sqlserver - this can change depending on the server vendor we're using
- startup project
    - microsoft.entityframeworkcore.design
    - microsoft.extensions.configuration.json
        - config file will be getting gitignored
- ef core globally using dotnet tool install --global dotnet-ef
    - for dotnet-ef cli commands

- you want to keep your credential strings in the configuration.json file to avoid security risk

# migration
- dotnet ef database update