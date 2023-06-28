using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using MixerModels;

namespace MixerBL
{
    public interface IMixerBL
    {

        Task<List<UploadMusic>> GetUploadedMusicAsync();

        Task<List<User>> GetUsersAsync();

        Task<List<SavedProject>> GetSavedProjectsAsync();

        Task<List<Sample>> GetSamplesAsync();

        Task<List<Track>> GetTracksAsync();

        Task<List<Pattern>> GetPatternsAsync();

        Task<UploadMusic> GetUploadeMusicByNameAsync(string name);

        Task<User> GetUserByIDAsync(int id);

        Task<SavedProject> GetSavedProjectByIDAsync(int id);

        Task<Sample> GetSampleByIDAsync(int id);


        Task<Track> GetTrackByIDAsync(int id);


        Task<Pattern> GetPatternByIDAsync(int id);

        Task<UploadMusic> AddUploadedMusicAsync(UploadMusic uploadedMusic);


        Task<User> AddUserAsync(User user);

        Task<SavedProject> AddSavedProjectAsync(SavedProject savedProject);


        Task<Sample> AddSampleAsync(Sample sample);

        Task<Track> AddTrackAsync(Track track);

        Task<Pattern> AddPatternAsync(Pattern pattern);



    }
}



    static int queensAttack(int n, int k, int r_q, int c_q, int[][] obstacles) {
    //approach: we are given all the info we need upfront. we just need to 
    //populate a 2d array and iterate through given the queens moveset,
    //incrementing the number of squares the queen can attack.
    //once the queen meets an obstacle, we stop iterating in that direction and return to
    //original queen position
    
    
    //first, create a 2d array for n - number of rows and columns on board
    int[,] board = new int[n,n];
    //queen's position is given by r_q and c_q - place queen on board.
    //I will represent queen with the value 2.
    board[r_q, c_q] = 2;
    
    //then, place the obstacles on the board
    //I think we need to iterate through the obstacles array to place these
    //k is the number of obstacles
    //once we have finished placing obstacles, stop adding obstacles
    for(int i=0; i<k; i++)
    {
        int row = 0;
        int column = 0;
        obstacles[i,0] = row;
        obstacles[i,1] = column;
        
        board[row, column] == 1;
    }
    
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
                    
                    if(board[uphelper, righthelper] == 0)
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
                    if(board[downhelper, lefthelper] == 0){
                        queenAttacks++;
                        downhelper--;
                        lefthelper++;
                    }
                    else{
                        break;
                    }
                }
                
                //traverse up and left
                int uphelper = i;
                int lefthelper = j;
                while(uphelper < n){
                    if(board[uphelper, lefthelper] == 0){
                        queenAttacks++;
                        uphelper++;
                        lefthelper--;
                    }
                    else
                    {
                        break;
                    }
                }
                
                //traverse down right
                int downhelper = i;
                int righthelper = j;
                while(downhelper >= 0){
                    if(board[downhelper, righthelper] == 0){
                        queenAttacks++;
                        downhelper--;
                        righthelper++;
                    }
                    else{
                        break;
                    }
                }
                
                //traverse right
                int rowhelper = i;
                int righthelper = j;
                while(righthelper < n)
                {
                    if(board[rowhelper, righthelper] == 0)
                    {
                        queenAttacks++;
                        righthelper++;
                    }
                    else {
                        break;
                    }
                }
                
                
                //traverse left
                int rowhelper = i;
                int lefthelper = j;
                while(lefthelper >= 0)
                {
                    if(board[rowhelper, lefthelper] == 0)
                    {
                        queenAttacks++;
                        lefthelper--;
                    }
                    else
                    {
                        break;
                    }
                }
                
                //traverse up
                int uphelper = i;
                int columnhelper = j;
                while(uphelper < n)
                {
                    if(board[uphelper, columnhelper] == 0)
                    {
                        queenAttacks++;
                        uphelper++;
                    }
                    else
                    {
                        break;
                    }
                }
                
                //traverse down
                int downhelper = i;
                int columnhelper = j;
                while(downhelper >= 0)
                {
                    if(board[downhelper, columnhelper] == 0)
                    {
                        queenAttacks++;
                        downhelper--;
                    }
                    else
                    {
                        break;
                    }
                }
                
                
                
            }
        }
