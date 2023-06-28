# week 1 content review
- notes taken are on practice questions/categories I don't feel completely confident in


# SOLID Principles
- SOLID principles are used to enforce software design structure and avoid design problems
- S: Single Responsibility Principle
    - any class should only have a single responsibility
    - small is good!
    - example: simply separate tasks into different classes to avoid one class/interface handling all calculations
- O: Open Closed Principle
    - a software entity should be open for extension, but closed for modification
- L: Liskov Substitution Principle
    - an extension of the open closed principle
    - a base class should be interchangable with it's subtype without breaking program functionality
    - you can assign a base class type to a subclass when the subclass has the same implementation as it's base class with extended functionality
- I: Interface Segregation Principle
    - break interfaces into smaller interfaces so different implementations can work for specific situations
    - example: if multiple different objects have functionality that differ from object to object, but still all need to implement specific methods, having interfaces that break these implementations down to smaller blocks will allow for more clean code
        - remember, a class can inherit multiple interfaces
- D: Dependency Inversion Principle
    - one should depend upon abstractions, not concretions
        - high level modules should not depend on low level modules - both should depend on abstractions
    - example: implement a repository layer between a business logic and database layer

# collections
- IEnumerable
    - IEnumerable interface exposes an enumerator, which supports simple iteration of a non-generic/generic collection
    - IEnumarable is also the root interface of the collections hierarchy

# out keyword
- allows one to send a parameter to a method call which does not yet have a value assigned to it
- this means the method will return the value of the out after processing

# ref keyword
- passes a direct reference in a parameter instead of just the value
- by default, c# just passes the value but not the reference!

# arrange, act, assert

- covariance - anything that can go UP to a certain class
- contravariance - anything that can go DOWN to a certain class
- invariance - nothing can go up or down to a certain class


- is operator for runtime, typeof operator for compile time