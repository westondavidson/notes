# SOLID Principles
- simply good design principles for OOP
- used to create understandable, flexible and principle
    - Single Responsibility - Classes should only really have one purpose
    - Open-Close - open for extension, closed for modification
        - you shouldn't need to rework everything in your program to add new stuff!
    - Liskov Substitution Principle - derive objects should be suitable for their implementation
        - if you inherit from a base class, that class should be substitutable for that base class
    - Interface Segregation - users of inerfaces should not be dependent upon methods they do not use
        - keep your interfaces purpose and functionality as specific as possible
        - you have multiple inheritance for interfaces so you can keep them separate!
    - Dependency Inversion Principle - Concrete implementations should be based upon abstract definitions
        - dependency injection!!!!

- asp.net framework has built in features for dependency injection

- ```new``` is glue :) for layers that are dependent on each other, be careful not to make dependencies glued together and tied to specific implementations.
- you want implementations to be loosely coupled enough to where you could change implementations in a single simple place, if possible


