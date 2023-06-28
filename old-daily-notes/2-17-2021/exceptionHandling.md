# Exception Handling
- an exception is an event that occurs during the execution of the program that disrupts the normal flow of instructions
- an exception is short for an exceptional event!
- could be bad if you're demoing to a client, or good if you're trying to find out a use case you haven't thought of on your own!
- exceptions are different from errors - errors are outside of the applications control/developer's hands.

# throwing exceptions
- you throw exceptions using the throw keyword
- throwing exceptions will let you handle them elsewhere!
- if you make exceptions, you might want to make a separate exceptions project so you can reference those when you need them

# handling exceptions
- exceptions are handled using a try-catch block
- catch more specific exceptions first, then more general ones
- the finally block will run with or without exception - it always runs
- you don't always have to include a finally block, but use it when needed!
- you want more specific exceptions listed before general 

# additional notes
- exception gets thrown in business logic a lot, as it's the connector from the data and frontend