# p1 requirements
- should be deployed and hosted on app service in azuer
- code pipeline should be built for it
- using azure pipelines
- should use asp.net MVC - DO THIS FIRST i think
- code first approach to the db


# other p1 notes
- for our p1, only requirement for aesthetics is that we implement a different color scheme for the template lol
- I want to do more than that
- might want to look into setting up sessions since our views and model are tightly coupled, it's our front end that's in charge of keeping client state - maybe???
- controllers get recreated for each request and response, so if you want to save data and you're navigating different views to choose those, you'll need to find a way to save them, so sessions are highly recommended
- the views we have in our app get compiled by the razer engine - what the client is interacting with isn't the view in the web app, rather an html version that's been compiled
- when we request again from our server, we'll have to send data from our compiled html page to our controller.
- views get compiled to html, html renders on browser, user/client sends html response to our server after

- to update we will need 
- an update view derived from the herocontroller

- Edit my tohmvc app on GitHub to be able to edit hero details. That means: 
- build the heroDL method, and also 
- the views related to it and also, 
- the actions related to it. 
- Use the HeroCRVM as a viewmodel

# Things we'll learn next week:
- cicd build pipeline
- how to publish app to internet

- we should look into 20 unit tests
- due on march 17th
- an mvp for p1 has to be functional and has to be deployed. Data should be persisted to a db.


# more p1 notes - 3 5 2021
- LOOK INTO PARTIAL VIEWS, IT WILL HELP A LOT
- use sessions to persist data between multiple request response lifecycles!!
- to set up sessions you set it up in your startup.cs
    - app.UseSession()
    - and then in services you put services.AddSession();
- topic list in the trainer github for p1 requirements and topics that we will need to review for QC