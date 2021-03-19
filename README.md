# ChessAI
 A chess AI that will be coded in python using the Chess package goal is to implement a neural network and have the AI Hopefully play at ~1800 elo rating 
 
In the current state the program generates random games using a Monte-Carlo tree and using the following formula identifies which nodes are optimal for play 

The reason a Monte-Carlo tree structure was chosen is due to its simplicty and no need for board evaluation functions.

UCB = V + C*sqrt(ln(N)/n)

Where 

V is the percentage of wins the node has seen wins are calculated as +1 for a win -1 for a loss and 0 for a draw 

C is a exploration/Explotation constant the higher the value the more the code favours exploring nodes wheras the lower it is the more it values exploring nodes that it has good confidence in meaning that those nodes lead to high win percentages

N is the amount of times the parent node has been visited in our case we are running 1600 games each time we look for a move 

n is the amount of time the child node has been visted/explored 

The program will pick the node with the highest UCB score to explore 

In its current state it plays deterministically picking the node with the highest UCB after 1600 games have been simulated from the current board state to the conclusion of hte game (win loss or draw). For training the Neural Network it will play against itself where the current model will play deterministically and the challenger model will play stochastically assigning probabilites to nodes where the higer the UCB the greater the probability of play and then it will draw these from a distribution in order to select its move. The challenger model will become the best model if it can win 55% of the games it plays against the best model 

The project is still in its early stages and needs much more fine tuning 

Readings List.

These are some recources that have helped this project

https://towardsdatascience.com/monte-carlo-tree-search-158a917a8baa#:~:text=What%20is%20Monte%20Carlo%20Tree,the%20policy%20of%20the%20game.

https://www.chessprogramming.org/Main_Page

https://kstatic.googleusercontent.com/files/2f51b2a749a284c2e2dfa13911da965f4855092a179469aedd15fbe4efe8f8cbf9c515ef83ac03a6515fa990e6f85fd827dcd477845e806f23a17845072dc7bd

https://medium.com/applied-data-science/alphago-zero-explained-in-one-diagram-365f5abf67e0

TODO List 

1. Implement GUI to play on so that you dont have to call humanmove() function to play 

2. Implement NN and train model (similar to googles alphazero)

3. Make bot playable on Lichess in order to obtain performance rating

