# OOP Pillars
-   abstraction
-   encapsulation
-   inheritance
-   polymorphism

# abstraction
-   a technique for dealing with complexity by providing users with a simple interface to hide complex details of an operation
-   example: when we have a menu and options to select, we don't know what's happening under the hood. Hiding the underlying complexity of the program
-   we implement abstraction using interfaces and abstract classes, as well as additional seperation of concerns

# interfaces
-   contain definitions for a group of related functionalities that a non-abstract class or a struct must implement
-   interfaces are basically just a list of methods
-   do not have constructors
-   they can have static methods
-   methods are implicitly abstract in an interface
-   in 8.0, interfaces can define some things inside methods

# abstract clasess
-   abstract classes can have constructors!!! interfaces can NOT

# when to use which
-   abstract classes impose hierarchy/format
    - fields and methods, properties, etc.
-   interfaces are used to implement functionality or behavior
    - just methods!

# polymorphism
-   the whole point of polymorphism is that one interface can have many implementations
-   sort of related to abstraction as well
-   presenting the same view for the end user but the input params could be differe, type could be different, etc.

# implementation
-   hard to understand, read up on this lol - basically different types of polymorphism

# inheritance
-   establishes an is-a relationship between objects
-   promotes code reusability
-   IS A IS A IS A IS A
-   you can inherit from multiple interfaces but you can only inherit from one class

# Composition
- composition describes has-a relationship
- the child cannot exist independent of the parent
    -   example an order has multiple line items
# aggregation
- aggregation describes a relationship between two or more objects where one object contains multiple instances of other objects
- the child can exist independently from the parent
    -   a department has many employees

# association
- association describes a uses-a keyword
- the lifecycles of the two objects are entirely separate from one another
    - example: a computer uses a keyboard


# encapsulation
-   treat related data/behavior as a single unit/capsule
-   implemented via data hiding and wrapping (grouping logic in classes, assemblies, and namespaces)
-   wrapping focuses on encapsulating the complex data in order to present a simpler view for the user.
-   data hiding focuses on (?)

# Access Modifiers
-   access modifiers SPECIFY access levels
-   public - available to everything!
-   private - available only to itself/declared class
-   protected - only available in the declared class and in derived/child classes
-   internal - available to anything in the same namespace
-   protected internal - same namespace AND derived/child classes in other namespaces
-   private protected - check over recording, missed this one
