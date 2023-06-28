# Variance
- a form of polymorphism

# Type Variance
- a type that can be substituted with another type!
- basically, if a child or parent object of a type wants to be a type of their child or parent, they CAN
- covariance - if a superclass wants to be it's sub type
- contravariance - if a sub class wants to be it's parent type
- invariance - basically if a class can't be another class because of it's typing

# Type Casting
- Boxing (or autoboxing) is casting to a supertype, or is an UPcast
    - think of it like putting the type into the container that is the bigger type
- Unboxing is DOWNcasting, or casting to a subtype. Uses explicit type casting <>
    - like taking the type out of the box, so you have a smaller box
- if you might potentially use data, the compiler will make you use explicit type casting.

# Type checking
- the ```is``` operator is used to check if the runtime type of an object is compatible with the given type.
    - if the object ```is``` the same type, returns true
- ```typeof``` is used to get type at compile time
    - ```Object typeof OtherObject```
    - not the same thing as ```GetType()``` method of an object