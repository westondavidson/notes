# javascript
- there is no correlation between javascript and java
- js is loosely typed - variables can be reassigned to any type at any time
- js is interpreted, not compiled, since it runs from the browser

# ECMASCRIPT
- standardization of js
- like how html has html5, js has es6, the latest standardized version

# scopes in js
- the scope of a variable describes where it exists
- 3 scopes:
    - function
    - global
    - block

- hoisting makes variables declared using var have a global scope
- when u declare variable using let, it limits the scope of a variable to the block it is declared in
- it's better to use let, not var, to ensure proper scoping
    - let is block scoped to the statement
- https://itnext.io/var-let-const-javascript-es6-feature-series-pt-1-fa603567809e

# other types of variable declarations
- const prevents variable value from being changed
- put stuff in {} for objects
- put stuff in [] for arrays
- to declare object, use object literal syntax


# truthy and falsy
- in js, all values have a boolean equivalent
    - you can evaluate actual values instead of boolean expressions
        - example: if person - can evaluate to true or false if object person exists
- falsy values - FUN0NE
    - values that evaluate to false
        - false, undefined, null, 0, NaN, empty string
- truthy values
    - anything else
- undefined means you haven't defined a value yet, but null means it's been defined and set to null;
- == checks if value is same, === is checking type
- == converts type (type coersion)

- difference if you use closer with a basic function as opposed to use it with an IIFE?
    - iffe's are immediately invoked and values are shared, whereas with basic functions you can make new closures to have different instances of the basic function running.


# functions in js
- basic function
    - methods - outside of class, they're called functions
- callback function
    - function within a function
- arrow function
    - anonymous function
        - lambda expression basically
- IIFE
    - pronounced iffy
    - immediately invoked function expression


# encapsulation in js
- since js is not OO, it has no access modifiers
- you can still achieve encapsulation using closure
- closure is when you have a function within a function


# inheritance in JS
- before ES6, classes weren't a thing in js, but there was such a thing as prototypal inheritance
- there are now classes in js!! They basically abstract prototypes into keywords that relate to other oop languages.

