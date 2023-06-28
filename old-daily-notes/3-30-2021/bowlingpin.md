# problem breakdown/scenario
- there are a given number of pins in a horizontal row
- two players are playing, alternating
- whoever knocks down the last pin, the current user wins
- one pin, or any two adjacent pins
- some moves have already been played


# representations:
- I represents a position containing a pin
- X represents a position where a pin has been knocked down

# input breakdown
- the number of test cases that will be input (t)
- the user inputs the number of pins for test case 1 (n)
- the user inputs a string representing the current pin combo: example: IXXI, where n is 4

# end result
- given the current configuration of pins, if you both play optimally, determine whether you will win this game or not

# game theory aspect

# possible approach
- given the current representation, find the optimal combination to result in 0 pins remain standing
- determine if number of plays for optimal combination results in an even or odd number
    - even means you win, odd means the opponent loses
- loop through above logic for each set of user input for n pins and string representation


- when there is only one possible outcome
- when theres only one possible approach to achieve victory
- else, you lose 