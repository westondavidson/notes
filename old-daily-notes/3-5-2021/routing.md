# routing
- how does an http request find the controller/particular action we get to?
- asp.net core controllers use routing middleware to match
- routers find controllers

- routing middleware is run when a request is received, then it locates our controller, gets our controller
- then the controller action that's been called gets displayed

- action methods are methods that handle requests in a controller - basically all methods in a controller
    - could be a view result, data, status, etc (mostly views though i think)
- model binding just means the form data we received makes sense for the logic we want to process
- model validation means the data returned is valid for stuff that was set on our view model
- action methods should contain methods for mapping a request to a business concern.

# model binding
- basically allows to bind stuff on your view to the properties of your models
- automates variable conversion process (string to .net types)
- [httpget("{id}")]


# conventional routing
- inside a call to UseEndpoints() you can create a route by just explicitly defining it

# attribute routing
- this is defined for RESTful APIs
- uses sets of attributes on each controller action to map actions directly to route templates