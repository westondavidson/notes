# request response lifecycle
- process that goes from browser, to server, to database

# http request
- send from client to server
- 3 parts
    1. start line
        - method - describes action to be performed
        - target - describes where to send the request
    1. header
        - meta data
        - example: content type- what data type body has
    1. body
        - the actual content of the request

# http verbs/methods
    - get
        - show resource
    - post
        - create new resource
    - put
        - update resource
    - delete
        - delete reseource
    - head
        - returns just the headers
- note - html forms only support get and post methods, you have to use js to use other verbs

# safe and idempotent
- safe methods
    - considered safe if it does not change state of resource (data in your database)
    - get, head
- idempotent
    - the state of the resource is only affected once by any changes implemented by the method
    - even if you send 10 delete requests on one thing, the thing will only delete the one thing
    delete, put, head, get

# HTTP response
- from server to client
- 3 parts:
    - status line
        - contains http status codes of describing what happened when interacting with the server
    - headers
    - body

# HTTP status codes
- status codes give a short description of whether an interaction is successful or not
- status codes are grouped by their number
    - 1xx - informational
    - 2xx - communicating success
    - 3xx - redirection
    - 4xx - errors that are client's fault, client side errors
    - 5xx - errors that are the server's fault, server side errors
- 405 is method not allowed/no way to handle it, 501 is method not implemented
- 405 is client side, 501 is server side

# DNS
- domain name system - the phonebook of the internet
- domain names are things like nytimes.com, google.com, etc... while web browsers interact using IP addresses
- DNS translates domain names to IP addresses so browsers can load internet resources
