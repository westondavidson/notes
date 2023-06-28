# docker
- applications need certain things to run on a machine - like a runtime
- when deploying an application you want end users to be able to run the app regardless of their machine
- docker helps set up a uniform environment where our application runs with all the necessary configurations
- basically a single style of instance to guarantee that anyone using the program will have the same configurations

# containerization vs virtualization
- both provide solutions to create a uniform environment across machines
- containerization uses containers, while virtualization uses VMs
- containers virtualize the OS, VMs virtualize a machine - vms still have to install an os to the machine and do the rest of the configs
- containers allocate resources dynamically, while VMs allocate resources statically
    - so, containers only get assigned resources as needed
    - while with a vm, you have to statically declare what the resources are
    - whatever machine the vm is built on, it won't be able to take those resources back

# docker
- is a containerization platform
- lets you to wrap your code into a deployable form (image) and run it anywhere using containers
- tool used to deploy application as an image that runs on containers
- you don't want users to download your codebase, so a container is perfect
- example: a pc wouldn't need the jre installed for a java app since the container contains the jre


# docker packaging
- images
    - the filesystem that contains everything that we need to run an application - contains runtime environments, sdk, scripts, configs, etc.
- containers
    - a process you run on the filesystem you set up with an image
- registry
    - a place that lets you distribute docker images like docker hub - a repo for docker images


# building an image
- you need two things to build an image:
    1. a dockerfile
        - a text document that contains all commands a user could call on the command line to assemble an image
    1. dockerignore
        - like gitignore but for docker
        - helps avoid sending large or sensitive information
            - stuff like build output, connection strings, etc.

# docker architecture
- our commands like docker build, pull, run, all talk to our docker host/daemon, which pulls images from either our machine or a remote repo to run


- look at marielle's notes and the docker docs for more info on stuff like multi-project containerization and dockerfile info!

- marielle also added shortnotes to the toh docker app - check these to reference when working with docker cli