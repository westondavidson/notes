(depth x height x width)

make a wall of height n and width m


-figure out the possible ways to configure a single row of a wall
- then, get the number of ways to configure a wall of width and height
- then

1) (a-b)%p = (a - b + p)%p

2) (a+b+c+d)%p = (a%p + b%p + c%p + d%p)%p;


steps to take probably:
1. find the modulus of the total stuff
1. find the wall height


we need to find how many different setups for our blocks can exist without dividing two sets of blocks on top of one another to be the same thing



I found the crux to this problem was to first figure out the number possible ways to configure a single row of a wall of width W.

From this, you can get the number of ways to configure a wall of with W and height H. I call this function totalWalls(W, H)

Lets call the function for non-breakable walls (the question the problem asks for), unbreakableWalls(W, H).

We have a base case of

unbreakableWalls(1, H) = 1 for all H

There's a recurrence you can find between unbreakableWalls and totalWalls, but I won't spoil that since that's half the fun!


recursive way to find a number of permutations in a single row
because we have 4 types of bricks, if we're at the 7th position, in order to end up at the final edge, the final edge has to be a 1, 2, 3, 4 wide. it has to start at position 3 4 5 or 6
if you're in position seven
each one of those is unique from each other so you need to place a different brick to get there
you can treat the number of permutations to reach a 7 wide wall

fibonnacci adjacent thing, I have a picture
for anything higher than four, it's the sum of the last four

possibly 

then multiply that pic by number of rows to get permutations for that wall

second step is finding how many breaks there are
can't have a clean break through the whole wall, treat that as two separate walls
subtract number of total walls that you can create
figure out how many 7 wide walls there are then figure out how many ways you can have a combination
it doesn't matter if you have multiple breaks for internal things since the container for the width has a full thing


1. find permutations for one row (for each width beyond 4 ) given width m
2. multiply that permutation value by the number of blocks high the wall is (height) given height n
3. iterate through data finding all situations where modulus is 0, add these to a counter
4. subtract this final count from the original total number of permutations that was found prior to finding the locations which modulus is 0
5. congrats, you have a total count of all valid permutations!


we were supposed to approach it with a dynamic solution

SHRKD
someone found something in c++, trying to convert to csharp