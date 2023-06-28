# kubernetes
- an open-source platform that orchestrates the placement (scheduling), and execution of application containers within and across computer clusters

# Kubernetes Clusters
    - coordinate highly available clusters of computers that are connected to work as a single unit
    - in order to take advantage of clusters, applications are packaged in a way that decouples them from the original host
        - using containerization, we can achieve this.

## Control plane
    - manages a cluster
    - coordinates activities in cluster, like scheduling applications, maintaining state, scaling, and rolling out updates
## node
    - a node is a vm or computer that serves as a worker machine in a kubernetes cluster
    - each node has a kubelet, which manages the node and communicates with the control plane
    - nodes also have either a containerd or Docker to handle containerization

# kubernetes startup process
- when an application is deployed, you tell the control plane to start the application containers
- then, the control plane schedules the containers to run on the cluster's nodes
- the Kubernetes API is used to interact with the cluster

# useful commands
- kubectl - I think this is like "kubernetes control" - the cli for kubernetes
    - uses kubernetes api to interact with the cluster
    - common formatting for a command is `kubectl action resource` - performs the specified action on the specified resource (like node or container)
- kubectl version - see the version of kubectl installed
- kubectl cluster-info - see details about cluster
- kubectl get nodes - see nodes that exist in our cluster
- kubectl create deployment image=<image repository url>
    - deploys app image!!
- kubectl get deployments - see deployments
- kub get - list resources
- kub describe - show detailed info on resource
- kub logs - print logs from a container in a pod
- kub exec - execute a command on a container in a pod
- kub proxy - starts a proxy at a specific ip/port
    - allows us to debug and interact with our pods
- curl <localhost> 
    - the url is the route to the API of the pod
- kub exec <pod name> <action>
    - executes a command directly on the pod
- kub exec -ti podname bash
    - starts a console on the container. we can run our node js app now!
- kub expose - expose a service to external traffic!!!
- kub label pod <podname> <key=value>
- kub get rs - get replica set
- kub scale deployments/deploymentname --replicas=x - scale deployment to x number of replicas
- kub rollout undo - revert to previous known state of a deployment


# kubernetes deployment
- to deploy your app on a cluster, create a kubernetes deployment configuration
    - this instructs kub how to create and update instances of the app
- the control plane schedules app instances to run on nodes in the cluster
- the kubernetese deployment controller monitors the instances of the app - if one node goes down, another node replaces it.
    - self-healing to address machine failure or maintenance
- when creating a deployment:
    - specify container image for the application and the number of replicas you want to run
- pods inside kubernetes are unable to be seen from outside their own network without using kubectl for the kub api
- we will need to make a proxy that forwards communicaations into the private network

# kubernetes pods
- pods host your application instance
- represents a group of one or more application containers, and some shared resources for those containers
- the stuff contained in a pod shares an IP address and port space!
- pods are the atomic unit on the kub platform.
- a deployment creates pods with containers inside them.
- from outside to inside, the structure goes:
    - clusters have nodes and a control plane
    - nodes hold one or more pods, and nodes have a container runtime like docker to pull container image and run app
    - pods hold containerized apps and storage/volume. pods also have an ip address associated with them

# kubernetes services
- pods are mortal. when a node dies, the pods within die too.
- a replicaset can create new pods with the same state to keep the app running
- but, there are differences in each pod like the IP addresses
- there needs to be a way of automatically reconciling changes among pods to the application can function
- a service is an abstraction which defines a logical set of pods and a policy by which to access them
- services enable loose coupling between dependent pods
- services are configured with yaml
- a labelselector sets what pods are targeted by a service
- individual pod ip addresses are not exposed outside the cluster without a service
- services let you expose the pod ip adddresses and receive traffic.
- services are exposed depending on the type set in the servicespec
    - ExternalName sounds useful?? let's you map service contents to a website name for example

# services and labels
- services match a set of pods using labels and selectors, which allow logical operation on objects in kub. labels are key/value pairs attached to objects
- these can be used to designate objects for dev, test, and prod
    - embed version tags
    - classify an object using tags


# running multiple instances of an app/scaling the app up
- when traffic increases, we need to scale the app to keep up with user demand
- scaling is accomplished by changing the number of replicas in a deployment
- services have an integrated load-balancer that will distribute network traffic to all pods in that service.
- a replicaset allows us to create these replicas

# updating an application
- rolling updates allow deployment updates to take place with zero downtime by incrementally updating pods instances with new ones.
- having multiple instances is a requirement to perform rolling updates
- updates are versioned and deployment updates can be reverted to a previous version
- rolling updates promote an application from one environment to another via container image updates
- allows for rollback
- ci/cd of applications with zero downtime
- to update an app, use the set image command

# object config file
- an object config file is a yaml file that determines what you're trying to create, what you want to do with it (kind: Deployment), labels for the object, containers and an image for 

k8s demo after lunch
won't be back morning part because of qc
after freds demo center of excellency will have project handoff for us
by end of day we will have team leads created
tomorrow morning we have a panel tomorrow at 10am est