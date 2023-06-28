# App Architecture - Organizing your code

# Separation of Concerns
- The concept of organizing your code such that logic that follows a certain theme or follows the same functionality are grouped together
    -Basically: group your code logically to avoid having messy and unreadable code
- We don't want spaghetti code, we want lasagna (layers) :)

# Classes
- blueprints to the actual objects you instantiate in program
- use classes to structure data and encapsulate logic and data that go together
- remember: is-a and has-a relationships!

# Namespaces
- Logical grouping of types (classes, interfaces, structs, enums, etc.) that follow a certain theme of functionality
- using keyword is used for importing different namespaces and class libraries at the top of the page
- if the using keyword is used WITHIN a block of code, it's being used for garbage collection
- the physical grouping of namespaces are called assemblies (when code is compiled)

# Project
- A project contains all files that are compiled into an executable, library, or website
- The project file is an XML document that contains all the information and instructions that MSBuild needs to build your project, including content, platform, metadata, db stuff, etc... sort of like a json config file for a website
- the file extension describes what kind of project you're compiling

# Solution
- A solution is not an "answer", just a container for one or more related projects - final packaging of your application with VS settings.