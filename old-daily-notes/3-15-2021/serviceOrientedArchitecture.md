# service oriented architecture week!
- services that applications depend on need to be separated out
    - your frontend doesn't really grow at the same rate as your ui
    - when you don't separate out stuff with service oriented architecture, we basically have a bunch of chefs in a kitchen all putting food into a big pot
    - it's like legos

# monolithic architecture
- describes applications that have everything built into it - ui, bl, dl, etc. all wrapped in one package
# problem
- with asp.net mvc the view is tightly coupled to the processing logic
    - this means the client will have to wait for its request to be processed, and also for the view that the server eventually returns
# solution
- break up the unhealthy codependency!
- decouple logic from backend data from frontend logic
- put them in two different servers
- so even if logic is being processed in backend, user can still do stuff on fronted because they are decoupled
- this also frees up our server to just process bl stuff, so you don't have to worry about presenting stuff to the user - things like looking for a view don't need to happen any more on backend


# soa - service oriented architecture
- architecture style for building software applications that use services available in a network such as a web
- services are an implementation of a well defined business functionality
- we basically treat the whole bl as a service which returns to the client the necessary data to present to the end user

- there are some disadvantages
    - soa is a little complex, because you have multiple separated services
    - eventual consistency of data - have to make sure the data is consistent through all different services
- soa is good for when you want to grow your application for many users
- monolithic is good for simple projects with few users

# soa principles
- standardized service contract - need a standardized document to state what services are available for an api
- loose coupling - services should be independent from each other
- service abstraction - services hide logic they encapsulate from outside world - just say what it does, not how it does it
- service reusability - services should be maximized for reusability - don't create useless services
- service autonomy - service has everything it needs to run, can run independently from other services
- service statelessness - shouldn't be storing info in a service, just process logic
- service discoverability - services should be made available to the application
- service composability - one should never embed all functionality into a single service
- service interoperability - services should be able to work with each other using standards to ensure that communication is fluid

- microservice architecture is an implementation of service oriented architecture

- soap and rest are ways to build soa apps
    - both different architectural styles to build services
