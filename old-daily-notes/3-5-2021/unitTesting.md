# testing
- unit testing is all about testing a single unit of code to make sure it behaves as it should
- when unit testing, your environment should be pristine - other factors shouldn't affect the test
- example - our controller class is dependent on the bl and the mapper - we need to have instances of these two classes in order to function   
    - when creating a proper unit test, the method needs to be isolated
    - we want to create a fake environment where the only real logic we're processing is the unit test
    - these are our controlled variables
    - we set up objects that behave like actual dependencies of the real unit
    - test doubles are a term for test dummies/mocks that we use to fake the dependencies

- we have 3 types of test doubles
    - mocks - a specific type of test double that mocks inputs? if a function opens and closes a door, we just want to test against a mock door to see if the function will be able to open the real door later
    - stubs - an object that holds predefined data and uses it to answer calls during test. - to test bl layer, we create a repository stub because using the actual repo would query database. We would set up a mock repository that gives a fixed response so we can assert the bl is working as it should
    - fakes - have working implementations but not same as production, mimic/simplified code

# integration testing
- testing how multiple units work together
- takes longer than unit tests as there is a lot of overhead
- external components such as client requests and db responses are simulated
- don't worry about this right now lol
