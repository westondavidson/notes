# stuff happening today
- Xunit unit testing
- short tdd activity creating calculator class that takes in inputs, use TDD to take in those inputs
- debugging in VSCode
- using breakpoints, logging, app monitoring, etc.
- solid principles?

# unit testing
- all about testing
- many different types of testing, integration testing, etc.
- unit testing is testing the smallest units of our code - our methods.
- then go a step further to make sure application as a whole works as it should
- it's recommended to test your logic, not so much your UI - the UI will be tested by simply navigating the program, and is part of integration testing.
- good code is readable and also self documenting
- name your test class after whatever the class you're testing against is
- name test methods based on what you're testing for
- 3 parts of a unit test
    - arrange - all about setting up the things you need for the unit test
    - act - doing the thing you want to test
    - assert - comparing the actual results to your expected outcome

# We are using Xunit as our unit testing framework



# test driven development
- write unit tests first without writing the methods
- we will have a calc thats just empty
- create unit tests without methods first
- then create methods that pass those tests
- does tdd help? questions will be asked after activity
1. write tests that fail
1. implement code to make tests pass

- factory design pattern for menus might be helpful
- P0 requires 10 unit tests
- dotnet new xunit -o ToHTest
- xml comments are required for p0

- create a calc class that does the following
    - add two numbers
    - subtract two numbers
    - multiply two numbers
    - divide (should have exception handling for divide by 0) - exceptions should be thrown - two numbers
    - give nth fibonachi number
        - example - fibonachi starts with 0, 1 1 2 3 5 8...
        - if input is 0, then output should be 0
        - basically find where the number is in the fibonachi sequence
    - prime number checker - check if numbers are prime

    - stretch goal: check if an equation is balanced - if you input 3 + 4 + (5 this should output false
        - but if you input (3 + 4) + 5 this should output true
        - look into regex

- first thing is to create calc class
- output int for lots of stuff - first five parts of the calc class
- output should be boolean for prime number checker and equation balancer


calculator class

{
    Add(){}

    Subtract(){
    }

    Multiply(){}

    Divide(){
    }

    FibonacciCalc(){

    }

    
}

# marielle instructions


Calculator App
Create a calculator class that does the following:
1.	Add two numbers
a.	Outputs int
2.	Subtract two numbers
3.	Multiply two numbers
4.	Divide two numbers
a.	Exceptions should be thrown
5.	Give the nth Fibonacci number
a.	0 1 1 2 3 5 8 …
b.	If input = 0, output = 0
6.	Checks if number is prime – output boolean
7.	(Stretch goal) check if an equation is balanced
a.	If I input 3 + 4 + ( 5 output false
b.	If I input ( 3 + 4 ) + 5 output true
c.	*look into regex
Calculator class
{
	Add(){}
	Subtract(){}
	Multiply(){}
	.
	.
	.
	EquationBalanced(){}

}
# do TDD!!!
- Write code that fails (obv), and then code that passes the unit test
- https://devops.com/the-benefits-of-test-driven-development/
- https://andrewlock.net/creating-parameterised-tests-in-xunit-with-inlinedata-classdata-and-memberdata/
- codesignal is a good code practice site :)