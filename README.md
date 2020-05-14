# ChessAI
 A chess AI that will be coded in python using the Chess package goal is to implement a neural network and have the AI play at ~1800 elo rating 
 
In the current state the bot uses Monte-Carlo tree search in order to genereate games and find moves with high Upper Confidence bounds in order to pick moves that are good.

The project is still in its early stages and needs much more fine tuning 

TODO List 
0.5. Fix board eval function to actually use the peice square tables properly 
1. Add to board eval function a factor for mobility (how many legal moves are available)
2. Add to board eval function a factor for doubled pawns and side by side pawns 
4. implement GUI to play on so that you dont have to call humanmove() function to play 
5. Implement NN and train model (similar to googles alphazero)
6. Make bot playable on Lichess in order to see actual rating for 5+0 blitz 
