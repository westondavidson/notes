we will be continuing revmixer!!!

- we have a zoho board, and we need to write tests beofre writing code to pass those tests lol
- we have a revature style guide
- keep documentation up to date
- we want to be able to scale application horizontally
- domain splits - where we would like to split it up into different microservices
- before implementing microservices, refactor existing code

Kenneth.davis@revature.com
koala as profile picture
- we will talk with kenneth whenever we need to reach out to higher up during p3 basically
- don't spend money during P3 process!!

- next week there will be a checkpoint meeting to see how things are going, make sure the workload is about right
- presentation is on the 22nd, we have 3 ish weeks to work on this
- marielle will collect excel sheet

we will be leading design meeting

- core csharp and core sql

- intro to panels tomorrow


- how revmixer is structured
- what things do what
- revature resource group
- lay out what team members need to do before we code
- probably use separate trello board for specific group

- azure blob stuff, look into sharing
- presentation
    - here's how we store media
- 
- ask team members to clone and mess with repo tonight
- rich will set up a trello board
- each team will break out into groups and determine microservices


- the part is what contains all the events
- theres the notes that are played and the time they are played
- transport orchestrates the toggle play etc

- team leads after panel will talk with marielle brieflu
code challenge and query challenge

- restrict certain branches so that main branches can't be directly pushed to
- make sure code is well documented, we might be passing legacy code off to them, like document everything
- set up early communication stream
prepare needed documentation to present vision/design for the project

- progress 
- sa


- change save pattern to save project button
- change 

- implement feature to allow projects themselves to be subscribed to and called by


Plans for 5/7/2021
- discuss TDD, understand workflow of how to approach from a TDD perspective with a large team
- Kenneth meeting - ask questions about pricing, project goals, etc. probably pretty short - 2:30 cst
    - try to prepare notes for this beforehand
- standup with marielle hopefully
- approach: determine what methods need to be implemented, what dependencies/properties are taken in by these methods, and what the expected output is of these methods.


- jonathan is in main room
- tomorrow afternoon finalizing details for p3
- probably won't be able to be there in the morning
- thursday might have another k8 session with fred
- marielle will show us how to deploy to aks on thursday as well - might just have people who are interested come

- friday, marielle will be available most of the day
- thursday she'll be here as well
- thursday/friday 1 on 1
- friday soft skills training session

- when a user selects a sample set to load, a small divider with a name is placed above the sample set and all the samples/tracks therein are loaded
- users can either delete the divider or delete the sample set entirely from the project

1. create a service for retrieving and sending saved track data
1. implement service and parse data into the appropriate data structures
1. create a service that retrieves and posts sample sets
1. update mixer logic to load in sample sets as a group
1. 