# cloud computing
# What is the cloud?
- the cloud is a collection of servers owned by some service provider
    - 3 main cloud service providers are
        1. aws by amazon
        1. azure by microsoft
        1. gcp by google
- these platforms are used so other companies and individuals don't have to worry about maintaining the servers themselves
    - basically, being able to use services without using your own resources


# benefits of cloud computing
- cost
    - pay-as-you-go, don't have to worry about costs for maintenance, electrical bills, more people etc.
- scalable
    - easy to scale up
    1. horizontal scaling
        - scaling by adding or removing instances of a service, resource, or application
            - buying more servers!
        example: deploying web app across different servers
    1. vertical scaling
        - scaling by increasing the specs of the currently existing servers
        - example: increasing the ram of the server your app runs on
        - buying high end hardware can be more expensive than getting new servers - horizontal scaling is probably cheaper!
- security
    - these platforms offer robust security to protect data, apps, and infrastructure from threats

# cloud setup
- regions - places that have 3 or more availability zones
- availability zones - places that have servers that are geographically separate
    - even if one server goes down, you have other servers to handle those requests
- service level agreements - guarantee of a certain amount of uptime for the servers
    - if an outage results in data loss, they might compensate you

# cloud service types
- what are the different services that these cloud providers actually give you?
- these are only some of the different options:
1. IaaS
    - Infrastructure as a service
    - basically us asking for a server that we'll configure ourselves
    - we're renting out hardware
1. PaaS
    - platform as a service
    - removes both hardware and operating systems from the picture
    - allows you to focus on app deployment and management of application
1. SaaS
    - Software as a Service
    - provides you a completed product that is run and managed by the service provider
    - examples include gmail, outlook, word online, office 365, etc.
    - dont care about anything other than getting certain functionalities out of them

# cloud deployment models
- when you're deploying a system in the cloud
- private
    - could be on premise or provided by a service provider, but the resources are only accessible by you
- public
    - cloud services and servers that are open for use by the general public
- hybrid
    - some stuff is private, some stuff is hosted publically
- community
    - share resources among areas, example: universities cooperating in certain areas of research
- government
    - cloud for the whole country or something
