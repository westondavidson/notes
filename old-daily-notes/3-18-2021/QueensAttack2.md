- square chess board
- one queen, multiple obstacles
- figure out how many squares the queen can attack


each square is referenced by a tuple to describe row and column where square is located



- int n: the number of rows and columns in the board
- nt k: the number of obstacles on the board
- int r_q: the row number of the queen's position
- int c_q: the column number of the queen's position
- int obstacles[k][2]: each element is an array of  integers, the row and column of an obstacle


The first line contains two space-separated integers  and , the length of the board's sides and the number of obstacles.
The next line contains two space-separated integers  and , the queen's row and column position.
Each of the next  lines contains two space-separated integers  and , the row and column position of obstacle[i].


- storage buckets for data
- 3rd party api to identity users
- what other functionalities
- include collaboration aspect in functionality
- include section for state of mvp, any stretch goals to add to mvp, prioritize
- have a section where people could make their own
- some sort of interaction between users
- metadata for 
- admin role for approval of user ideas possibly
- maybe consider making it more social media esque
- search users by emails, add them as friend, see current projects
- user collaboration
- prioritize stretch goals - don't just stop once we're finished
- possibly include audio api

- playlist


int row = 0;
        int column = 0;
        row = obstacles[i][0];
        column = obstacles[i][1];
        Console.WriteLine(row);
        Console.WriteLine(column);
        




 //after having added obstacles to board, iterate through each direction
    //and add up attackable squares
    //if an obstacle is met, break from that pathing and continue counting
    int queenAttacks = 0;
    for(int i=0; i<n; i++)
    {
        for(int j=0; j<n; j++)
        {
            //once we find the queen on board, begin iterating in different directions
            if(board[i,j] == 2)
            {
                //traverse up and right
                int uphelper = i;
                int righthelper = j;
                while(uphelper < n){
                    
                    if(board[uphelper, righthelper] == 0 || board[uphelper, righthelper] == 2)
                    {
                        queenAttacks++; 
                        uphelper++;
                        righthelper++;
                    }
                    //once an obstacle is met, break from traversing this direction
                    else 
                    {
                        break;
                    }

                }
                
                //traverse down and left
                int downhelper = i;
                int lefthelper = j;
                while(downhelper >= 0){
                    if(board[downhelper, lefthelper] == 0 || board[downhelper, lefthelper] == 2){
                        queenAttacks++;
                        downhelper--;
                        lefthelper++;
                    }
                    else{
                        break;
                    }
                }
                
                //traverse up and left
                int uphelper2 = i;
                int lefthelper2 = j;
                while(uphelper2 < n){
                    if(board[uphelper2, lefthelper2] == 0 || board[uphelper2, lefthelper2] == 2){
                        queenAttacks++;
                        uphelper2++;
                        lefthelper2--;
                    }
                    else
                    {
                        break;
                    }
                }
                
                //traverse down right
                int downhelper2 = i;
                int righthelper2 = j;
                while(downhelper2 >= 0){
                    if(board[downhelper2, righthelper2] == 0 || board[downhelper2, righthelper2] == 2){
                        queenAttacks++;
                        downhelper2--;
                        righthelper2++;
                    }
                    else{
                        break;
                    }
                }
                
                //traverse right
                int rowhelper3 = i;
                int righthelper3 = j;
                while(righthelper3 < n)
                {
                    if(board[rowhelper3, righthelper3] == 0 || board[rowhelper3, righthelper3] == 2)
                    {
                        queenAttacks++;
                        righthelper3++;
                    }
                    else {
                        break;
                    }
                }
                
                
                //traverse left
                int rowhelper4 = i;
                int lefthelper4 = j;
                while(lefthelper4 >= 0)
                {
                    if(board[rowhelper4, lefthelper4] == 0 || board[rowhelper4, lefthelper4] == 2)
                    {
                        queenAttacks++;
                        lefthelper4--;
                    }
                    else
                    {
                        break;
                    }
                }
                
                //traverse up
                int uphelper5 = i;
                int columnhelper5 = j;
                while(uphelper5 < n)
                {
                    if(board[uphelper5, columnhelper5] == 0 || board[uphelper5, columnhelper5] == 2)
                    {
                        queenAttacks++;
                        uphelper5++;
                    }
                    else
                    {
                        break;
                    }
                }
                
                //traverse down
                int downhelper6 = i;
                int columnhelper6 = j;
                while(downhelper6 >= 0)
                {
                    if(board[downhelper6, columnhelper6] == 0 || board[downhelper6, columnhelper6] == 2)
                    {
                        queenAttacks++;
                        downhelper6--;
                    }
                    else
                    {
                        break;
                    }
                }
                
                
                
            }
        }
    }
    return queenAttacks;
    