## notes for youtube video: container orchestration explained - https://www.youtube.com/watch?v=kBF6Bvth0zw

# why is container orchestration important?
- A developer's main worry are the "primary" pieces of an application - they are worried about frontend, backend, and database layers, along with the compatible os and dependencies of said layers.
- However, the operations team is more worried about the actual deployment, scaling, and networking of said application's "total package"
- with container orchestration, all of these areas are achieved whithout the need for manual setup:
1. Deployment
    - Within a containerization platform, a cluster is taken advantage of and containerized versions of your services are deployed on one or more worker nodes
1. Scaling
    - these deployed containerized apps can then be replicated and scaled out among multiple worker nodes to provide greater resources for each service
1. Networking
    - The containerization platform handles exposure of network endpoints like IP addresses as needed
        - example: the front end might be exposed with a public IP address, while the other layers are only exposed internally where necessary within the cluster
1. Insight
    - A containerization platform can allow operations team members to log information about how each service is interacting with one another.
        - example: a network trace performed by operations team indicates that the front end service is interacting with the data access service directly, even though those communications should be going through a business logic service.

# kubernetes!
- an orchestration tool!

# statefulsets
- manages stateful applications
- maintains a sticky identity for each pods - these pods are not interchangeable - each has a persistent identifier that it maintains across any rescheduling
- to provide persistence in an application (a stateful application), you use a statefulset as part of the solution
- 