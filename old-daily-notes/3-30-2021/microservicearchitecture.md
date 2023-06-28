# Microservices architecture
- we are using msa for p3 and kubernites and other stuff we're learning this week
- simple at first, more complicated as time goes on
- if you want to get better at a specific language, try writing a full-stack X app!
- microservice architecture is just an implementation of soa, but it's more fine grained
    - like a puzzle with 100 pieces vs a puzzle with 1000 pieces
- single responsibility principle - each service is responsible for one thing, and one thing only
- MSA is used by basically all very large applications, and used by big companies.
- for applications with many many users
- monolithic is single unit, soa is coarse-grained, microservices is fine-grained

# MSA Characteristics
- 1. single responsibility principle - a service serves one and only one specific responsibility
- 1. encapsulated - services can only be accessed through a third party - our services shouldn't have access to each other
- 1. independent - data of each service is independent of each other

# benefits of MSA
- scalability!
    - easier to add new features without affecting existing services
    - can take down a service without affecting other services
- deployment
    - easy to deploy because you just deploy that one specific service!
- simplicity
    - easy to deployment
- fault tolerant
    - if one service goes down, it's not the end of the world. you can just start it back up again
- testability
    - easier to test since you're already decoupled dependencies! logic should be simple enough to test
- language agnostic
    - you can code one service in python, one in java, one in c#, etc. and they all work together because they send messages via http
    - huge benefit for working with people who practice different disciplines
    - also a huge benefit if you want to write an app and take advantage of EVERY language!!!

# drawbacks of MSA
- deployment
    - deploying lots of different services all at once can be pretty tricky
    - you could deploy one by one, but what if you need to deploy a bunch at once?
- complexity
    - while the logic of services is simple, the communication and aggregation of different services becomes convoluted
- monitoring
    - monitoring why a service isn't working might be because some other service is down
- eventual consistency
    - because things are divided up, a change in one place might not be placed instantly in another area - multiple services might need to run before
- chattiness
    - too much traffic, too many complicated communication channels in services all talking to each other at once

# service discoverability - service registry
- you have service registries that contain information about the services in your msa ecosystem, and they automate the monitoring of the service.
- your service registers to the registry, which has a registrar, which checks to see if the service is up or down within your system

# gateways
- gateway basically acts as a distribution center for all services, and it sort of acts as the router of the msa ecosystem
- with a gateway, you don't really know the underlying of the msa, since you're just talking to the gateway, it helps with abstraction!

# load balancer
- manages traffic to services, making sure that instances aren't getting called more often than others
- if one service gets used a lot, it might be worth deploying that service more than once (?)

# circuit breaker
- it stops anyone from communicating to a service if one of the services that is heavily dependent is down/broken

# message queues
- register to a service bus and send messages that way over http
- instead of sending a bunch of different httprequests, you can send those messages to a queue where the other services are subscribed and they'll see the update! service bus

# deployment
- we'll be using container orchestration software
- we will be using kubernites for this!
- Kubernites automates a ton of things, like configuration, load balancing, monitoring, resource allocation, etc.
