# devops
- the dilemma:
    - without new features, an app will become stagnant. But with new features, there's a higher chance that we lose our user's trust
- the ops team helps keep the application alive, while the dev team keeps the application updating
- devops is a marriage of development and operations teams
- a culture
- concept of the teams to work together to bring new features to production as fast as possible
- a set of practices that let us roll out features to the customer as fast as possible
- it's slow if the dev team and ops team don't work together to roll out these new features
- has to be a quicker way to respond to bugs or failures in production
- big picture: you get continuous feedback from ops team, and ops continuously integrate those features
- it's very important to keep end users happy - that's a big part of devops mentality

# CI
- stands for continuous integration
- all about continuously integrating new code and testing against existing codebase to see if everything works well with current build.
- makes sure it passes code quality checks that have been set up
- basically automating the whole process of checking against new code
- CI tools:
    - Pipelines - like azure pipelines, github actions, jenkins, aws code pipeline
    - code analysis tools like sonar cloud (more on this later)

# CD
- stands for either continuous deployment or continuous delivery
    - continuous delivery is when someone manually deploys the code to prod after much deliberation
        - this is usually practiced because cont deployment is a bit tricky to set up
    - continuous deployment is when everything is automated to even the deployment of code to prod
- cd is not limited to releasing to production - cd also helps pre prod environments with testing to help find bugs that might come up in an environment different from dev

# achieving devops
1. CI/CD
1. utilizing vcs - version control system (git)
1. agile planning
1. monitoring and logging - if something bad happens, we'll have logs and monitoring to quickly fix the issue
1. designing for scale - design and create code that is scalable and extendable
    - using microservices arch is designing for scale

- feature flags can be used to see if performance or buggy code exists in a new feature
    - by rolling out features to small user groups, you can ease any weird issues that might occur when a feature is rolled out to the general populace

look into topics:
- infrastructure as code
- microservices
- read microsoft docs on what are devops - azure devops
