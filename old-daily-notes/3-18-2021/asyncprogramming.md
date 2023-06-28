# asynchronous programming
- async programming is enabling code that reads like a sequence of statements, but executes in a more complicated order based on external resource allocation and when tasks complete
- implemented using the task parallel library

- tasks: tasks are an abstraction over threads managed by the clr
- task and a thread - a task is something to accomplish, a thread is what's working on the task - the line of development that's going to get that thing done
    - that's why tasks are just an abstraction over threads, because a 

# async vs parallel
- async programming is sometimes confused with parallel processing
    - async is not necessarily multithreaded
    - you can sometimes asynchronously complete tasks without multithreading
    - because async is abstracted for us, it's possible that multithreading is not being used

# making your program async
- use async versions of methods
- await those methods
- make methods async and return tasks
- bubble up
task is an asynchronous operation that can return a value