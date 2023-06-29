# C sharp 9 hour full course
- link: https://www.youtube.com/watch?v=M5ugY7fWydE

## Namespaces
- namespaces are groups that have classes which have functions that can be used in your app
- we make our own namespaces as well for the same purpose, to import these classes to other parts of your app

## classes
- allow you to model something
    - provide attributes, methods, etc


- Static
    - this function can run without creating an object previously
    - this function doesn't need to be instantiated to be used if it's declared static
- void
    - will not return anything


- conversion
    - explicit conversion
        - when you lose data, it's an explicit conversion
    - implicit conversion
        - when you're converting from a smaller to a larger data type, so nothing is being lost

- strings
    - store a number of characters
    - basically a bunch of chars in a row :)

- arrays
    - boxes inside of a bigger box
    - contains multiple values of the same data type
    - have fixed sizes
- multidimensional arrays
    - a single dimensional array is stacked vertically in a column
    - a multidimensional can be visualized as having columns and rows
- three dimensions
    - imagine a stack of spreadsheets with rows, columns, and sheets represented as [row, column, sheet]

- for loops
    - a way to iterate through a block of code given a condition

- in conditions, there are relational and logical operators
        - relational operators: > < >= <= == !=
        - logical operators: && - and || - or ! - not

- if else and else if
    - if (a condition is met), do this thing
    - else if (a different condition is met), do this thing
    - else none of the conditions are met, do this thing


- Ternary operator
    - ?:
    - evaluates a boolean expression and retrns the result of one of the two expressions depending on if it evaluates to true or false.
    - ``` numberSize < 10 ? "one digit Number" : "bigger number" ```
    - 

- switches
    - a switch will allow you to choose between a number of options depending on the case

- While loops
    - your index will be outside the looping structure
    - while (condition) do this thing

- do while loops
    - starts with the thing to do before asking about the while condition
    - this guarantees at least one run happens before exiting the loop

- exception handling
    - used to catch errors that could crash our program
    - use try catch blocks to catch errors that are thrown
    - use throw keyword tho throw an error
    - try to catch only problems that you expect so you can easily solve them. Don't catch the generic exception class unless you absolutely need to.
    - use a finally block to define something that will always execute in a try catch block.
        - finally {do something}


- String builders
    - allow you to change text directly in memory instead of copying the whole string before
    - StringBuilder class
    - basically turns the string into a real class instead of being the weird half and half value reference type thing of a normal string

- signatures for functions and methods
    - basic layout: access specifier, return type, method name(parameters) {
        body
    }
    - 

- access specifiers
    - determines level of access from another class
        1. public - can be accessed from another class
        1. private - can't be accessed from another class
        1. protected - can only be accessed by itself and derived classes
