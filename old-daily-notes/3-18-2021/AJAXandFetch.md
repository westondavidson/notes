- httpclient
    - a way for your api in csharp to make http requests and get responses from other apis

# AJAX & Fetch API
- getting data from the client side using AJAX and fetch - the js way
- ajax stands for asynchronous javascript and XML
    - this is a technique used for updating your page with information from a server without reloading it
- the xml part of ajax is there because traditionally, the data sent across networks use xml as a format
- but you can now send data in JSON format!!!

# how does ajax work?
- an event occurs, an httprequest with an xmlhttprequest object is sent to server, server processes this, and then returns to browser

# xmlhttprequest
- object that is used to send a request to the server and receive the response

# fetch API
- js interface for making http requests and processing server responses
- uses promises to achieve asynch
    - promises represent eventual completion or failure of an async operation
    - these are similar to tasks
    - promises are objects in js - you can treat them like objects once they get back
1. a promise is triggered, then either fulfilled or rejected
    - so you can do a .then(onFulfillment) or a .then(onRejection)
1. then the actions/object is returned to the promise
    - then u do a .then again
- call a promise, upon completion you define what you'll do to the promise
