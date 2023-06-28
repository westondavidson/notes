# MVC Concepts
- Model-View-Controller
- separates application into three main groups of components
- Helps achieve separation of concerns
- Models is logic, view is UI, controller is thing between the model and view that handles traffic
1. 
- http request gets routed/handled by a router. The router is in charge of building the appropriate controller object with the appropriate action that you would actually use.
    - when http request gets to our server the first thing that handles it is a router that THEN creates a controller to set up the appropriate model and view given the action.
- model is used to perform actions or return results of queries (your BL is held inside this).
- the controller takes data from your model, and then sends it to your view

# MVC Mode
- the model is sort of our state that contains our BL, and DL.
- bl and dl are encapsulated 

Model is bl, view is UI, controller is go between
- view and controller are both dependent on model

# MVC - View
- views are responsible for presenting content through the user interface
- views use razor view engine that compiles stuff we need to send back

- controller handles and responds to user requests.

- by using loose coupling

- asp.net core is not just limited to mvc applications, but also provides pattern based way to build dynamic websites
    - can also use it to create RESTful apis
- asp.net mvc
