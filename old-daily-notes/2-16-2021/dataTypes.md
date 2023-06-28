# Data Types!
- Data Types structure the data that you process in your program
- Remember - csharp is a typesafe language so data type is important!
    - Setting a data type is a form of validation in this way! ex: only variable type x is allowed for this method param etc.
- All types inherit from the System.Object base class - all types are objects!! even primitives
- There are two major types
    - Value types
    - Reference types

# Common Type System
- The CTS is a standard definition of the types in the .net compliant languages.
- reference types are basically any references to things that appear more "objecty", while value types are things more like data stuff (probably need to research this more)
- CTS exists because of language interoperability
    - projects can be written in multiple .NET compliant languages !!!!
    - You could have a project written in VB.NET and reference that same project in a project written in C#
- CLS common language specification is related but not the same - read the article included in ppt :)
    
# Value Types
- Analogous to java's primitives
- Stored in the stack, NOT the heap
    - stack trace = state of program when exception occurred
    - in stack, you get a value directly and not the object stored in the heap
    - so value types === NOT stored in the heap, just the stack, as they are accessed directly
    - The stack is just a stack, so it gets cleaned up when not being used
    - TLDR: value types are stored in the stack, not in the Heap
- enums, used to define a set of named integral constants
    - suppose you want to define categories for products in store app to recommend additional purchases for someone after they've purchased an item from a category. you could store these categories as an enum. enum should be constant. 
    - consider scalability - is this doable? (maybe don't actually use an enum for this if it isn't scalable)

# Reference Types
- A type that is defined as a class, delegate, array, or interface is a reference type
- The value that a variable reference type holds is null until you instantiate an object and assign the reference in memory.
- The value of the reference variable is technically just the value of the memory where the object is stored in the heap - hence, it is a "reference" to the object in memory
- The value that a variable reference type holds is a reference to the object in the heap
- Strings are technically reference types - a string is basically a list of chars (which are value types) "strung" together in a string object in the string intern