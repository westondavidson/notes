# REST - used in p2!!
- REST stands for REpresentational State Transfer
    - you're using a representation of a resource state to an application state
    - you're going to use json to represent a resource from a server to pass data to our service, or from our service to our client
- an architectural style to design your services
    - not actual rules, just a guideline
- guiding principles of REST:
    - client-server
    - stateless
    - cacheable
    - uniform interface
    - layered system
    - code on demand (optional)

# uniform interface
- your service would have an interface defined by four interface constraints
    - identification of resources
        - your resources should be well defined
    - manipulation of resources through representations
        - use appropriate action verb to access and manipulate your resources
            - get should be used for accessing, post should be used for updatinng, delete for deleting, etc.
    - self-descriptive messages
        - make sure that when a response is sent, make sure that the format is easy for the client to serialize
    - hypermedia as the engine of application state (HATEOAS)
        - not really implemented apparently
        - whenever you try to access a resource, you also get a list of methods that you could use on that resource

# client server and layered system
- client server:
- the client app must evolve separately from the server app without any dependency on  each other
- decoupling services from each other
- as long as endpoints remain the same, services can be developed separately
- layered system:
    - constraining the interactions of your components to the ones in the next layer
    - example ui components should never be able to access your data layer services

# stateless and cacheable
- stateless:
    - server isn't responsible for storing client state
    - server will not store anything about the latest HTTP request the client made
    - every request is new
    - no session, no history
    - let the clients store their own client state
- cacheable:
    - resources from the server can be cached if applicable, these resources themselves must delcare themselves cacheable
    - cacheable request:
        - get requests
    - non cacheable requests:
        - delete requests

# code on demand (optional)
- allows client functionality to be extended by downloading and executing code in the form of applets or scripts
- we can send executable script on the client side to render a part of the UI
- normally we just send static resources in the form of json or xml, but we can send scripts too technically


# richardson maturity model
- a way to describe how REST compliant your service is
- grades api according to the constraints of REST according to levels
    - level 0
        - uses http, single URI, one method (usually post)
        - example: a soap service is a level 0 rest service
    - level 1
        - meets level 1 but with multiple URIs
        - unique URI for each unique resource
    - level 2
        - uses HTTP, multiple URIs, various http methods
        - operations depend on the action method used
        - this is the easiest level to implement up to
        - 
    - level 3
        - uses HTTP, multiple URIs, various http methods, and HATEOAS
    

    # rest vs soap
    - rest can be any format, soap is xml
    - rest is stateless, while soap could be stateful
    - rest has good caching support, soap doesn't support caching at the http level
    - rest is contract based on http standards and conventions, while soap is based on wsdl document
    - rest defines errors by 400 and 500 status codes, while soap has faults
    