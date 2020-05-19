# ChessAI
 A chess AI that will be coded in python using the Chess package goal is to implement a neural network and have the AI Hopefully play at ~1800 elo rating 
 
In the current state the program generates random games using a Monte-Carlo tree and using the following formula identifies which nodes are optimal for play 

The reason a Monte-Carlo tree structure was chosen is due to its simplicty and no need for board evaluation functions.

UCB = V + C*sqrt(ln(N)/n)

Where 
V is the percentage of wins the node has seen wins are calculated as +1 for a win -1 for a loss and 0 for a draw 
C is a exploration/Explotation constant the higher the value the more the code favours exploring nodes wheres the lower it is the more it values exploring nodes that it has a good confidence in
N is the amount of times the parent node has been visited in our case we are running 1600 games each time we look for a move 
n is the amount of time the child node has been visted/explored 

The program will pick the node with the highest UCB score to explore 

In its current state it plays deterministically picking the node with the highest UCB after 1600 games have been played. For training the Neural Network it will play against itself where the current model will play deterministically and the challenger model will play stochastically assigning probabilites to nodes where the higer the UCB the greater the probability of play and then it will draw these from a distribution in order to select its move. The challenger model will become the best model if it can win 55% of the games it plays against the best model 

The project is still in its early stages and needs much more fine tuning 

TODO List 
1. Implement GUI to play on so that you dont have to call humanmove() function to play 
2. Implement NN and train model (similar to googles alphazero)
3. Make bot playable on Lichess in order to see actual rating for 5+0 blitz 
4. 
