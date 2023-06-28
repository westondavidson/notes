1. create a service for retrieving and sending saved track data - Weston
1. parse data into the appropriate data structures - David
1. create a service that retrieves and posts sample sets - Joaquin
1. update mixer logic to load in sample sets as a group - Kevin
1. convert add sample dropdown menu to popout menu maybe? - Jake
1. schedule task - update html to show position of sequencer - David maybe after :)

uploadmusic-service
user

backend team has updated the uploadedmusic model - reflect this in our frontend
- readded collections
- switching user isadmin to a stream


tomorrow fred will be here! some time morning and afternoon


- discussing the microservices conversion
- refactoring decisions
    - we will be refactoring a large majority of our step sequencer to allow for dynamic updates to the step sequencer
        - users will be able to load in individual samples load in full sample sets to existing projects, and delete individual samples and sample sets as desired
        - we are replicating our playlist functionality to allow for user created sample sets which will be able to be shared among other users so they can save or share services
    - uploading music and uploading samples will be fleshed out to allow for additional form data like song name to be included when an upload is complete

    - when come back to afternoon meetings, gotta talk to batch as a whole later on today - gonna have to pull us into the main session to have a discussion


    - instead of having isadmin boolean if we had a list of roles, like a string value that's set

- when a pattern is saved, it will be saved as one huge pattern


- updating the upload music page to provide additional form data to backend
- create an upload page for samples
- duplicate playlist page functionality to allow users to create "samplesets"(secretly just playlists of samples basically) and add samples to samplesets
- privacy toggles for songs and samples
- a page that lists samplesets and allows users to add a sampleset to their collection of samplesets
- a page that lists uploaded samples and allows users to add a specific sample to their library of samples 


- sample controller work maybe?
- sample controller in project service


- 4/8/2021
- testing published first frontend tests
- 

get the average of all population in city by each city
- watch the csharp video that douglas posted


delegates
clr
directives
http verbs
ajax
devop


each pattern is going to need

What are delegates: 

Micro services arc vs monolithic arc: 

What is the CLR:

exception handling

what is an observable

structural and attribute directives

What are angular directives:

What are the joins

HTTP Verbs:
(look these up)
Post pull or put
Get
Delete
Fetch
Head

status codes
200 ok
300 redirect

average of population in city
select * where 