# Jasmine
- in the world of javascript unit testing there are some commonalities
- there's a test class
- describe the thing you're testing, then have a function
- we have expectations rather than assertions
- i expect the result to be
- jasmine is built into angular by default I think!
- this link will help a lot with testing setup:
- https://jasmine.github.io/tutorials/your_first_suite
- specs and suites, look em up
npx ng test


- karma is the test runner
- tests need to run in browser, karma provides a platform for this
- jasmine can't do this alone
- karma talks to all the different areas, from typescript to jasmine to the web deployment
- all of this is managed inside the karma.conf file
ng test --code-coverage for code coverage
- angular has a lot of advice about writing tests 
    - it was designed to be very testable
- angular has dep inj built in
- guide to unit testing in angular!
    - https://angular.io/guide/testing
- xunit is playing the jasmine role, and vstest is the karma thing more or less

- services are easier to test because they don't have to talk to the dom


- the spec files describe how to unit test a service!!!!! these are basically already written for you!! must rewrite

- integration is how things work together
    - better for testing a few normal cases of integration
- unit test is only one portion of the code

if you're done with looking at the tests, just ctrl c.

- a spy takes an existing object or an empty object and let's you contain some spy functions (?)

- behavioral driven tests
- read the angular docs for more testing !!!