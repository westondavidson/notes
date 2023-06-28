# Schedule - presentation on 2/17/2021 Morning!!!
-   first five groups, delegates actions events functions predicates will be delivering their presentation in the morning on friday
-   later on, the seralog and endlog groups will go
-   to include in presentation:
    1.  advantages of events
    1.  business use cases of delegates/events
    1.  general overview of events process

# Teamwork delegation!
-   Angela will be refactoring a previous Java project into C# for code demo purposes
-   Alex and Weston will be separating topics from the following article:
https://www.tutorialsteacher.com/csharp/csharp-event
-   Alex will be covering the first half of the topics.
-   Weston will cover "Passing an Event Data" and downwards


# Events
-  Events are the types of members that you can define in a class
-  They are a type of object that can notify other objects about some specific situation that has occurred with it or it's objects
-   a class can define an event on an action
-   Events are a simple and easy way for a class to notify others about a change in status
-   event model is built based on delegates
-   you use the event keyword to declare an event
- declaration is done in the following format:
    - [access modifier] [event] [event type] [event name]
    - event type is the delegate type of the event.
    - events follow the observer design pattern
-   the class that raises events is called the publisher, and the one who receives notifications of the event is called subscriber
-   an event is an encapsulated delegate

# how does an event work? Lifecycle
-   a class which contains the definition for the event is considered the "publisher", while any classes that subscribe to that event are "subscribers"
-   the delegate defines the signature for the event handler method of the subscriber class
-   an event handler signature must match in both the publisher and subscriber class
-   when an event is triggered, a response is sent from the publisher to the subscriber classes, at which point the designated event handlers in the subscriber classes handle events as needed

# how do you declare an event?
-   to declare an event, you use the following format:
    -   [access modifier] [event keyword "event"] [delegate name/event type] [event name]
-   the class containing the declared event is the publisher

# how do you raise an event?
-   to raise an event, declare the event(the event handler) in another class with the same signature as the initial event.
-   typically, you will want to define the

# Start on passing an Event Data


