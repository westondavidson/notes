# angular
- angular is a front end framework used to create SPAs (single page applications)
- modularized in nature
- front end design revolves around the idea of components making up a page

# SPAs
- single page applications are webapps that are contained in a single page
    - this means, when you access that webapp for the first time, you are served a page from the server, and any other interaction with that page, JS takes care of and manipulates the page via the DOM. you have this illusion of interacting with a different page, but it's actually just the same page being updated over and over again
- advantages
    - no more server roundtrips! and page will always be responsive
    - they are very easy to deploy!!
- disadvantages
    - startup load time will take a while because everything you need for the page will be loaded at the point of access
    - also, learning pains - it takes a while to get into angular

# angular architecture
- Modules
    - containers for a cohesive block of code dedicated to an application domain, a workflow, or a closely related set of capabilities
        - in a nutshell: modules are a way to encapsulate code/logic that go together.
        - angular modules are based on modules in es6, but they have metadata.
    - to declare a module, you use the @NgModule decorator
- components
    - basically views with logic!
    - when scaffolding a component, the ng cli gives you 4 files:
        1. css file - styling
        1. html file - structure/template
        1. ts file - logic
        1. spec.ts - unit testing
    - in actuality, a component only needs two files:
        1. html file
        1. ts file
    - a component is just a view with logic. you define a class as a component by using the @component decorator

- Templates
    - just the html file. defines the structure of your component!

- services
    - logic that is shared between components or other services. you can use services to separate out logic in a reusable way. Components should just have view specific logic generally.
    - logic that is shared or not related to the view, you store in services. Sort of your BL if components are views.
    - services have the @Injectable decorator that allows them to be injected as dependencies in components or other services

- decorators
    - used to distinguish the functionality of your classes. Like @NgModule - declares a class as a module.
    - decorators

# directives
- help you with dom manipulation
- we have attribute directives
- and structural directives! add or remove or replace elements in the dom
- components are technically structural directives because they change the structure of your page!
- we will be mostly using structural directives (ngfor, ngif, ngswitch)

# observables
- okta uses observables to see who is logged in and who isn't
- observables are like promises in that they both represent async operations
    - BUT, 



- REVIEW PIPES, FILTERS, AND EVENTS ON OUR OWN
- ALSO REVIEW PROMISES VS OBSERVABLES