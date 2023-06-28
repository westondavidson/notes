# .NET
- a free, open-source dev platform
- a collection of libraries
- the SDK includes everything you need to build and run - .net core applications, cli tools and editor
- the runtime includes just the resources required to run existing applications. The runtime is included in the SDK
- .NET standard is the base class library AKA all the base class resources that come in .NET
    - basically out of the box APIs and libraries
- .NET base classes work with all .NET compliant languages! csharp, fsharp, etc. will all work with the .NET standard
    -dealing with string and primitive types, database connections, IO operations, etc. are all included as operations within the   .NET standard library
- BCL = base class library


CLR
    - CLR or common language runtime provides memory management, JIT compilation, and exception handling support
    - .exe and .dll are the output types in our output folders - the CLR then compiles these and executes those.
    - AOT-compiler is ahead-of-time compiler and it's different than a JIT compiler, read up on it!
    - msbuild is our compiler engine. It compiles the code into a .exe or dll which is the intermediate language
    - then THAT goes into our CLR, which uses a JIT compiler to compile to native code depending on machine type


Managed Code
    - Code whose execution is managed by a runtime
    - The CLR manages this code, and
    - Code that is not managed by the CLR is unmanaged code - examples include c, etc. because it's up to the dev to handle memory management, garbage collection and other tasks that would be handled by a runtime.

Garbage Collection
    - Provides automatic memory management of your heap memory
        - checks objects in the managed heap and performs necessary operations to reclaim memory
    - IDisposable interface with the dispose() method can dispose resources that don't clean up normally using a garbage collector
    - You can also use using blocks and statements for clean up.
    - Garbage Collection process is generational garbage collection, so each generation back is checked less frequently. The shorter something's life cycle, the more often garbage collection checks the use of the value.
