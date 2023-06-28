# Design Patterns

-   Similar to mathematical formulas, we have design patterns in programming
-   If formulas help you solve problems that follow a particular variable set and problem type, then design patterns help you with common programming design issues.
-   

# Design patterns we've used
-   Repository DP
    - the business logic shouldn't be concerned with how the data layer is storing stuff.
    - you wrap the data access logic in a repository class that takes care of storage and retrieval of information.

-   Facade DP: wrapping a complex subsystem and presenting a simple interface that only contains the methods utilized by the end user.
    - example - our herorepo design in TOH

# Design patterns we could use
-   Singleton design Pattern:
    - Creating a single instance and only one, and utilizing that single instance throughout program life cycle.

-   Factory Design Pattern
    - This common superclass, create a factory class that produces certain implementations of that superclass depending on some input.
    - Example - if you have menus that inherit from one menu interface, use a menu factory and showcase a different menu to the end user.
    - Another example -  you want to create log in functionality. you have customer object and manager object. they both inherit from a person superclass. we have a person factory. Your factory can create an object for you and pass that to the user depending on their login.