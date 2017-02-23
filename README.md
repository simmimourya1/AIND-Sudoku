# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint propogation works only because it tries to reduce the number of possibilties for every position using different constraints to minimize the search space.
As we know the constraint behind Naked twins algorithm is that no squares outside the two naked twins squares can contain the twin values. Which means if any square outside the twins contain common values then it is eventually going to lose it resulting in a simpler state space. 
If we consider naked twins algorithm as one of our local constraint then just like elimination and only choice constraint we may assume that the current search space is propogating towards a smaller search space.

In my implementation, the function tries to find all the naked twins and then one by one, it deletes the 'twin values' from all the common peers of the naked twins.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Diagonal sudoku imposes one extra constraint alongside all the previous ones. One nice approach could be to add extra diagonal units alongwith classic sudoku units. Hence the solver now will consider this constraint as well. It will reject the solutions which donot follow diagonal rules. 

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