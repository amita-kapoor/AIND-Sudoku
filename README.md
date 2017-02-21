# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In naked twin is a strategy to solve sudoku, it is based on the fact that if two boxes in a unit have same possible 'pair' of digits, then we can safely assume that this 'pair of digits will not occupy any other box within that unit.
To implement this for each unit (in present case all rows and column units), we first identify the boxes which contain digit pairs. If in a unit we can find two boxes with same digit pairs, then we have found our "naked twins". The next step is then to eliminate the values of these two digits from the remaining boxes of the units.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: In Diagonal Sudoku the additional constraint is that the two diagonal units viz: (A1,B2,C3.D4.E5,F6,G7.H8,I9) and (A9, B8, C7,D6,E5,F4,G3,H2,I1)
can have the digits '123456789' only once. To make this possible in the solution we modify the total unitlist to include these two diagnal units. After this, using the process of elimination and only choice we are able to satisfy the respective constraint.

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