# filters
- filters are used for cross-cutting concerns
- why attach filters before and after actions are run?
- if the code being run is not related to the action itself, but needs to be run
- instead of having a redundant block of code, you can have, for example, a logging filter
- you can use this to your advantage by placing filters to guarantee logging/results etc.
- used when you've already been routed to a controller/action

- authorization, action, result, exception

# helpers
- helpers are used to add logic to your views
- after being compiled using the razor view engine, these helpers become plain html
- tag helpers have similar syntax to actual html tags
- html helpers have a different format but accomplish same thing
- tag helpers are suggested because the syntax is written in html rather than weird html helpers


# data binding
- bind an action/view to a model, and apply the validation logic/structure stated in the model
- strongly bound models to views can use tag helpers for validation, and labels, because we are strongly bound
- data annotations like [required] are recognized because the view is strongly tied to the model
- set validation in your model using data annotations!!!
- binding a view to a model ^^^

- controller side - once we receive a value from a view, we can bind that data to a model - this is model binding
    - whatever falls into our () for our action method
    - [HttpPost] data annotation recognizes that this is responding to a post request from client
- you can validate the model that is passed to your controller from client side to guarantee that the model passed in is in a valid state
- binding data or a model to an action in a controller ^^^

# dependency injection
- 


- prep an mvc applet that we might want to deploy
    - build a little blog page in mvc and then take the baby application and deploy it on docker
- we're going to deploy our application via a container
- the container is just a process we're running on a virtual file system - it's our webapp!!
- we'll deploy the webapp using dockerhub, then we can send docker image links to each other and people can build that very quickly!
- this will let us deploy our code without having to deploy our codebase