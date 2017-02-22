# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: When two boxes in the same unit have the same 'twin' values, i.e. two digits only, the probabilities of these twin boxes to be filled with one the digits are 50%. For the rest of the boxes in the same unit the probablity become 0%. This form the basis of the constraint in behind the Naked Twins strategy, and we enforce it by visiting each box in the same unit and remove all the digits that are contained in the twin boxes. Applying this operation repeatedly for all the unresolved boxes propagate the constraint across the board.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: By identifying diagonals in the grid and link them to the boxes that intersect with them. Then using Elimination and Only Choice strategies, diagonals will be considered in these operation and digits with 0% probability will be removed.

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
