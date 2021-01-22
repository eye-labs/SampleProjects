This is a model written in the Wolfram Language to solve the Rubik cube.

The Rubik cube is a combinatorial puzzle with a large number of possible states, 
so a brute force approach will not work. There is only one goal state which
makes the objective well defined.

Broadly speaking, this solution approach works in the following way:
We begin by generating the data to train the model.
1) Start with the cube in the solved state and randomly rotate the faces of the cube.
2) Keep track of the number of rotations (called the score) and after a given number of rotations,
record the state of the cube. 
3) Repeat this process multiple times till we have enough data points.
4) Develop a deep learning model to estimate the number of moves required to get the cube
back to the goal state which is called the score.

If we can accurately estimate the score, then we can generate moves that lower the score and 
bring us closer to the solution.

To solve the cube from a random starting state, we randomly generate moves and estimate
the score of the cube. We then randomly generate moves that reduce the score until the score 
is zero which corresponds to the goal state.

Some of the data files are too large to be uploaded. If you would like the data files, please 
contact me at cnathaide@yahoo.com.
