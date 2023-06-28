# SOAP
- soap used to be popular "back in the day" because of xml
- no app is an island
    - soap lets you use web services that are coded in other languages
    - to use a web service, you only need to know the endpoint and what type of request to send/format requests the service expects
- soap stands for Simple Object Access Protocol
- technically, soap is a messaging protocol
    - soap is a way to send standardized messages between two services
- soap services describes services that uses SOAP to communicate with other applications
- soap is protocol independent - you can send soap messages via http, https, etc.
- platform and language independent
- works on basis of dumb endpoints, smart pipelines
    - highly documented, 
- soap wsd - list of available services
- soap envelope/message - order to service

# wsdl
- stands for web service definition language
- describes a web service, specifies endpoints and methods
- user guide for your soap service
- contains the address, binding, and contract of your soap service - ABC
    - address - url address to connect to soap service
    - binding - how service is bound to service SOAP - rpc remote procedure call, and something else
        - how you're able to call the actions
        - binding also has protocol, security procedures
    - contract - rules of soap service - what inputs methods take, outputs, etc.

# contract first vs contract last
- soap services are highly documented, what is written in your wsdl is what you get
- not easily changable in a soap service
- when you create a soap service you can do:
    - WSDL first (contract first)
    - or create service first and then WSDL after
- service is basically the concrete class, while the wsdl is the interface
- some IDEs let you generate a wsdl file for your web service

# SOAP message
- if the wsdl is the menu, the message is your actual order
- an xml document containing
    - an envelope element that identitifes the xml document as a soap message
    - a header that contains header info
    - a body element that contains call and response info
    - a fault element containing errors and status info - all the exceptions that occurred
        - we define exceptions using these faults

# XML namespace
- soap services rely heavily on XML
- xml namespaces are used to declare tag structure in soap
- used to format what the service is sexpecting
- a standardized tag structure helps in parsing data

# creating a soap service
- to create soap services
- dotnet core/dotnet 5 doesn't support these
- wcf is the package to install to make these - wcf service application

