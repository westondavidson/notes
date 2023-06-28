# Crash course notes
- link: https://www.youtube.com/watch?v=BfEjDD8mWYg

## review notes
- course was okay but focused a lot on how to generate templates and implementation of stuff, and less on theory or building up understanding.
was kind of hard to get anything practical out of this other than "here's how to build an ASP.NET MVC list app"

# what is ASP.NET core?
- framework to build web apps
- plenty of competitors out there, this is just one choice
- asp.net is a popular one
- .net - microsoft's development platform since 2001.
    - runtime environment
- ASP - active server pages - dynamic web pages, connected to db
- core - open source cross platform version of ASP
- .NET is the unified platform
    - uses CLR, common language runtime

# MVC
- model, view, controller design pattern
    - separates the frontend, business logic, and data layers into three separate areas
    - separation of concerns to avoid mixing business logic, frontend logic and data access together.

# View
- a piece of html/css code or similar
- gets a list of data from the controller
- combines data with a template

# Model
- data related
- consists of classes/objects with properties
- uses SQL statements and interacts with DB

# object relation mapper
- this is a system that relates a class to a table. Takes either an existing table and creates a class, or vice versa
- allows computer to generate DB tables without having to know how to write SQL
- Entity Framework is MS ORM
- good for basic applications

# Data access object
- manually create tables
- more traditional method, write your own SQL statements
- DBAs tend to prefer DAOs because it probides more visibility for finding problems

