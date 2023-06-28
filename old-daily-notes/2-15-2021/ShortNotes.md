## MD is a markdown file

# CLR (Common Language Runtime)
-   runtime that manages a bunch of stuff, garbage collection, etc.
-   JIT - (Just In Time) compiler
    - Takes in code, transforms code into machine code so machine can run your code.
obj, bin folders
-   build output
-   result of running dotnet build
dotnet run
-   dotnet build + dotnet run (the code)
dotnet build
-   compiles code but doesn't run it

### TLDR the compiilation process:
1. .cs file
1. Compiled using MSBUILD to an EXE or DLL
1. IL (Intermediate Language)
1. Passed into CLR (common language runtime) on program execution
1. Processed by JIT (Just-In-Time Compiler) determinant of what platform the program is being executed on 