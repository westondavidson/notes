# Value Types and Reference Types
- Link: https://www.youtube.com/watch?v=ldq7ZByB4p8
## Value Types
- You have a bunch of different value types
- structs is one
- a struct is a value type that can encapsulate data and related functionality
- Value types contain the instance of a type itself, NOT A REFERENCE
- Value types contain a DIRECT instance of a type
- this means, in a value type, when a variable value is altered, it is copied on assignment to a new location
- for example
    - if you assign a struct to another struct, these become two separate structs, one copying values when instantiated but then being totally separate after
        - because values have now been copied to a new location
    - these are completely independent of each other at this point, because there is no REFERENCE between the two

## Reference types
- in the example provided above, if the struct is simply a class instead, assignment will cause a REFERENCE to the data already provided in the heap.
- all we're doing is creating a new pointer to the data that is in the back, it's just another reference to the instantiated class!!

## Stack
- static data - the data we know for sure at compile time
    - we know an int requires 32 bits, double has 64 bits, so we know how to assign these in the stack right away
- holds three pieces of info
    1. the variable name
    1. the type of data
    1. the actual data
- the stack pointer will then move up 32 bits (if it's an int)
- keep allocating stuff into the stack and it's nice and efficient!
- when something is "deleted" from the stack, it isn't actually deleted, the pointer is just moved down 
- so when a new thing comes in, it overrides the old data
- by knowing how large the incoming data is with it's type, the stack is very fast and efficient with assignment and deleting/rewriting wherever the pointer is at.
- Stack was made for super fast allocation and deallocation, but only works with fixed data size


## Heap
- allows data to grow and shrink in size most of the time
- at compile time we have no idea how much size will be needed
- When a class is instantiated, the stack WILL have a new value added, but it will just be the variable name, the type, and a POINTER/REFERENCE to a location in the heap
- Pointers made in the stack have a specific size
- when the instantiated reference type is out of scope and deallocated, garbage collection will happen some time in the future.


## when to use value type vs reference type
- you might think "why not use value types all the time if they're so memory efficient?"
- refer back to the stack example earlier, where a new value was created for every single input and added on top of the stack!!
    - For a recursive function in which we are referencing a value type instead of reference, we are allocating a new piece of memory to the stack every time the recursion is run. 32 bits each time.
    - while we still need to allocate a new reference each time for a recursive function with a reference type instead, the pointers are all still just looking at the same data in the heap, and therefore it's more efficient IF the reference type is bigger than a double/8bytes/64bits
    - but, if for example, the value holder has more than the 64 bits, then a reference type is better.
        - if a class has 128 bits of data, it would be twice as fast as a struct in a recursive function!

## additional notes and facts
- the stack has a 1 MB limit on 32 bit and 4MB on 64 bit
- that's why if you write an infinite loop, you'll run out of memory and hit a stackoverflow exception!
- in a multithreaded application, every thread has it's own stack allocation - 1MB each that can't be shared across threads
    - they can access the heap together though
- value types don't always go in the stack
    - a list of integers - a list is a reference type so would go in the heap
- if you have value types inside a class, they'd also go on the heap (obviously)
- if you box a value type it goes into the heap.
- strings are reference types but we don't really want them to act as reference types, because they tend to have similar comparisons and operations to value types (equality, adding on, removing, comparisons etc)
    - they're like an anomoly that's in between
    - strings are immutable
        - if you add something onto a string, it discards the old one and then creates a new one
        - string builders are good because they don't do allocations until the very end.
