# K8s is a container orchestration system
- we are able to handle scalability, networking, maintainability, and state management by using orchestration!
- orchestration is nothing more than an environment where we control all those pinpoints that we have
- in the environment, we'll have modules that handle network, state, scheduling, health, etc.
- because the environment can provide these, any containers within the environment will be handled by those modules.
- we have the data plane, and the control plane
    - the data plane is where the containers are, the stuff we're creating
    - the control plane is where we have the modules that control our data/containers
- k8 represents the orchestrator that controls the environment
    - checks that all modules are performing the way they're supposed to perform
- we talk to the head to manage the system!

# k8 will have
- a cluster within, that then contains nodes, which then contain pods, which then contain containers
    - cluster > nodes > pods > containers
    - cluster also has:
        - state, network, scheduling, health/monitoring (because it's the part that orchestrates within the control plane)
    - a node also has:
        - services!!!
        - services let pods connect to each other, and also with the outside world!!

- minikube for local dev
- we will use azure aks for prod
- minikube will allow us to create a small orchestration environment in our machine
- pods are logical units of work

commands to set up minikube on desktop:
inside ubuntu terminal:
set up username/password - keep password simple
sudo apt update
sudo apt upgrade -y

minikube package:
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.debm
minikube start --driver=docker --cpus=2 --memory=2G
at this point, we have a cluster running
- kubectl should be installed
- do `kubectl config get-contexts` command to see minikube running
- `kubectl config current-context`
- in the world of k8, you can have as many context as you want on a single machine. A context is just a cluster from a k8 perspective
- `kubectl get nodes` gives us how many nodes we have in our cluster

- kubectl run nginx --image=nginx
    - could give more information, but this is good for now
- `kubectl expose pod nginx --port=80 --target-port=80 --type=NodePort`
    - port is where we'll connect, target port is where we connect in service
    - type is nodeport, so it's publically accessible!!

- in the world of k8, there are 3 types of networks (or at least main ones)
    - cluster IP
        - accessible within the cluster only!!!
        - good for pods talking to other pods, because you don't want it exposed to the rest of the world
    - node port
        - accessible to outer world!
        - a node is nothing more than a server. if you have access to a node, you have access to the server itself
    - load balancer
        - accessible behind a load balancer, or an OSI 4 - a tcp connection, not just http connection - more low level than http

- we'll use node port for everything for now, but load balancers are the way to go when going for prod
- curl is a command line connection checker

minikube service nginx lets us open the port on our machine outside of minikube
minikube dashboard!!

- rather than having one pod that scheduled multiple containers, one deployment can schedule multiple pods - that's what a deployment is i think

# training materials
- https://kubernetes.io/docs/tutorials/kubernetes-basics/
- https://training.play-with-kubernetes.com/
