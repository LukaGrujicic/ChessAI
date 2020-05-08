# ChessAI
 A chess AI that will be coded in python using the Chess package goal is to implement a neural network and have the AI play at ~1800 elo rating 
In the current state there are 2 functions that the AI can use to play 
1. randomM() makes a random move from the list of legally available move 
2. movegen() uses the evaluation function boardEval() that returns an int value for the value of the peices of the board and peice position this then makes the move that increases the boardEval() function the most on that move (ie it will always capture even if it means that it will lose that peice on the next move) 

The project is still in its early stages and needs much more fine tuning 

TODO List 
1. Add to board eval function a factor for mobility (how many legal moves are available)
2. Add to board eval function a factor for doubled pawns and side by side pawns 
3. Create tree algorithm and pruning to check up to x moves deep in order to optimize algo 
4. implement GUI to play on so that you dont have to call humanmove() function to play 
5. Implement NN and train model (similar to googles alphazero)
6. Make bot playable on Lichess in order to see actual rating for 5+0 blitz 
