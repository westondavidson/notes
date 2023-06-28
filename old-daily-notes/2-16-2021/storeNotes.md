# P0 requirements
### Store App Overview:
- The store app is a software that helps customers purchase products from your business. Designed with functionality that would make virtual shopping much simpler!

# Functionality:
- [ ] add a new customer
- [ ] search customers by name
- [ ] display details of an order
- [ ] place orders to store locations for customers
- [ ] view order history of customer
- [ ] view order history of location
- [ ] view location inventory
- [ ] The customer should be able to purchase multiple products
- [ ] Order histories should have the option to be sorted by date (latest to oldest and vice versa) or cost (least expensive to most expensive)
- [ ] The manager should be able to replenish inventory

# Models:
- [ ] Customer
- [ ] Location
- [ ] Orders
- [ ] Product
- Note: add as much models as you would need for your design

# Additional requirements:
- [ ] Exception Handling
- [ ] Input validation
- [ ] Logging
- [ ] At least 10 unit tests
- [ ] Data should be persisted, (no data should be hard coded)
- [ ] You should use SQLServer DB
- [ ] DB structure should be 3NF
- [ ] Should have an ER Diagram
- [ ] Code should have xml documentation

# Tech Stack:
- C#
- SQLServer DB
- EF Core
- Xunit
- Serilog or Nlog


# Additional Details
- copy new requirements into notes
- have most of the user structure finished by next week!!!
search customer, add customer, navigate and view location inventory, try to have a placeholder order functionality done. Models, business logic should be working. files, static collections, keep data layer far away from business logic if possible.
- do something similar to class for data stuff with toh
- set up logging as you go with serilog

- should allow multiple products and multiple KINDS of products in a single order
# P0 Notes
-   Have a theme! Make your store unique.

# Example Application
-   Marielle is using a whiteboard to create a wireframe to sketch out her Application
-   She lists the functionality requirements
-   She has the methods she wants, so how will she go about designing her application?
-   Think about design before implementation or anything else
-   Consider things like classes, interfaces that will be implemented based on what sort of things will be needed (relationships, is-a, has-a relationships, properties etc.)
-   When you're prototyping, try to limit your properties. You want to lay groundwork more than you want to create full implementation. Full implmementation can come later.
-   Keep your models lean - don't add unnecessary properties
-   This is also a test of scalability once you want to add additional properties or elements

## Classlib declaration for a project in dotnet can be used as a class library which your primary application references :)

# Store App Notes
-   Naming format: FirstName_LastName-P0
-   Include a readme in your github repo for the project
-   Required to provide an MVP - a minimum viable product
-   Try to meet as many of the minimum requirements as possible - what should a store app be able to do?
-   Don't just reach the minimum requirements - go further beyond!
-   If you don't have the whole project planned beforehand, do vertical development instead of horizontal
    -   Build things as you need them - jump between things and you won't get bored when developing business logic
-   Don't forget about exception handling!
-   Due Date - March 3rd!
-   This week - logic and UI
-   Next week - database (probably since it's SQL week)
-   Week after that - Presentation prep!

# log to a JSON file, and every time you run program at a certain date, sorta show that in that folder maybe - new requirements for the project



# presentation tips:
- introduce yourself for presentation!
- make sure in groups, you communicate setup beforehand
