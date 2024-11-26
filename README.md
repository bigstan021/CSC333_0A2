## Project Description
This project implements a linear programming solver using Python. The objective of the LP problems addressed in this project is to optimize a linear objective function, subject to a set of linear constraints. This can be applied in various fields such as operations research, economics, and engineering to maximize profits or minimize costs.

### Objectives of the LP Problems
- **Optimization**: To find the best possible solution (maximum or minimum) for a given objective function.
- **Constraint Satisfaction**: To ensure that the solutions meet all specified constraints.
- **Feasibility**: To determine whether a solution exists that satisfies all constraints.

## How It Was Solved
The LP problems were solved using the `scipy.optimize` library in Python, which provides functions to handle optimization tasks. The following steps outline the solution approach:
1. **Define the Objective Function**: Specify the function to be maximized or minimized.
2. **Set Up Constraints**: Define the constraints in terms of inequalities or equalities.
3. **Use Optimization Function**: Apply the `linprog` method from `scipy.optimize` to find the optimal solution.

### Example Code Snippet
Here’s a simplified example of how the LP problem is set up and solved:

```python
from scipy.optimize import linprog

# Coefficients of the objective function
c = [-1, -2]  # Maximize x + 2y

# Coefficients for inequality constraints (Ax <= b)
A = [[1, 1], [1, -1], [-1, 0], [0, -1]]
b = [4, 1, 0, 0]  # Constraints

# Solve the linear programming problem
result = linprog(c, A_ub=A, b_ub=b)

print('Optimal value:', result.fun)
print('Optimal solution:', result.x)
```

## Installation Instructions
To run this project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/lp-solver.git
   cd lp-solver
   ```

2. **Install Required Packages**:
   Ensure you have Python installed. Then install the necessary libraries using pip:
   ```bash
   pip install scipy numpy
   ```

3. **Run the Code**:
   Execute the main script (e.g., `main.py`) to see the results:
   ```bash
   python main.py
   ```

## Usage Instructions
- Modify the coefficients in the code snippet above to solve different LP problems.
- Adjust constraints as necessary to fit your specific optimization scenario.

## Features
- Solves standard linear programming problems.
- Outputs optimal values and solutions.
- Easy to modify for various applications.
