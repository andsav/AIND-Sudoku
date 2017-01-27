# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint propagation means using local constraints to reduce the search space for the whole problem. In the case of the naked twins strategy, we use the following constraint: if two boxes in the same unit have the same two digits, we can conclude that those digits will appear in either one of those boxes and nowhere else in that unit. Therefore, we can remove them from every other box in the unit, and reduce the search space. The local naked twins constraint has an impact on the unit and on the whole board, reducing the number of possibilities we need to consider in every subsequent step. 

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The diagonal sudoku problem is the same as the regular sudoku problem with two new units added to the original one (the two diagonals forming an "X" on the sudoku board). Since we are adding those two units, we are increasing the number of peers for boxes on the diagonals. This is a new local constraint (a box cannot have the same digits as one of its peers) which reduces the search space.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.