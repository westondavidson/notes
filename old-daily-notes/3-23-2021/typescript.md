# Typescript
- typescript is "transpiled" to javascript
- because it is transpiled, there are some parts of ts that reflect how compiled languages work
- just a superset of JS - all valid js is valid TS
- statically typed, not strongly typed
    - types are checked before runtime, but types can still be changed at runtime
- cannot be run in the browser, has to be transpiled, browsers only support javascript!
- compilation is transforming one language from another - c# to intermediate language
- transpilation transforms languages with the same level of interaction - both high level, human readable languages

# types in ts
- all valid js types are ts types
- some special types ts introduced:
    - any - literally any type - let js take over and infer the type for you
    - unknown - a type-safe any. Ensures someone using the type declares what the type is
    - void - a function that returns undefined or no return value

# structural typing
- a core principal of TS is that type checking focuses on the structure that objects have
- the compiler only checks that at least the variable names required are present in args passed and that they match the types required
- this is called "structural typing"
- you use interfaces for these in TS

# interfaces
- the "contract" aspect of interfaces in TS refers to the structure of the object. all objects of the interface type must follow the structure and type composition of that interface.
- because interfaces are contracts that must be followed, the contract you're setting is with regards to object structure in TS
- you use them to impose a structure to any class or object that would want to implement them
- note that interfaces in TS are the same as interfaces in C#

# composing types
- ts is still just js under the hood
- you can have multiple types for a single variable, you do these using union or the | sign
- so if you have a proprerty that could be null or string, you can just say let x : null | string

# classes
- same as JS classes, but TS classes has access modifiers
    - public, private, and protected. work same way as c#
- so ts developers can work in a more oop way
- also has extends keyword for inheritance

# modules in TS
- modules are used to split off scripts into different files, used to organize code
- modules in ts have additional features
    - able to alias imports, import multiple modules from a single script file, only import types etc.
    - helps in organizing your code in their own files to use them in different places
- export and import keywords can let you use or send something to another file


## achievements yesterday
- Completed our REST API with most basic CRUD implementations for most aspects of the project
    - this will very likely need to be frequently revised to ensure accurate implementation for our project needs
    - fixed bugs involving our API controller (Jack)
    - completed implementation of BL and DL, reworked some methods to accept different types of parameters (Weston & Jack)
- Frontend team members began implementing front-end design in separate repo
    - completed a proof-of-concept drum machine demo to build off of as the sequencer progresses (David)
    - began reworking a pre-existing angular template to meet project needs (Tate)
## Goals for Today
    - deploy our backend service
    - seed DB data
    - set up OKTA authentication for service
## Current Blockers
    - amazon S3 bucket setup for media file storage/retrieval
        - we are still working on this, we have an AWS account + storage ready to go and understand how to embed media for playback in our application
        - we need to figure out uploading/removing from bucket