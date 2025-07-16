# OPTIMIZATION-MODEL

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: SAMRIDDHI PATHAK

*INTERN ID*: CT08DL700

*DOMAIN*: DATA SCIENCE

*DURATION*: 8 WEEKS

*MENTOR*: NEELA SANTOSH

This project is a linear programming (LP) optimization problem designed to model a decision-making scenario in a bakery. The objective is to maximize profits from producing two products: Bowdoin logs and chocolate cakes. Using the PuLP library in Python, the project demonstrates how to formulate and solve a resource allocation problem where constraints are based on limited equipment capacity.

The problem begins by creating an instance of an LP problem using LpProblem, where the goal is to maximize an objective function. The objective is to earn the highest possible profit based on the number of Bowdoin logs and chocolate cakes produced. Two decision variables, x1 and x2, are defined using LpVariable, representing the quantities of Bowdoin logs and chocolate cakes, respectively. These variables are constrained to be non-negative integers, reflecting that partial products are not feasible in real-world bakery production.

The profit function is defined as 10*x1 + 5*x2, meaning each Bowdoin log contributes $10 to the profit, and each chocolate cake contributes $5. This linear combination is added to the LP problem as the objective function. The simplicity of the profit model allows the optimization solver to find the most profitable mix of products efficiently, given the constraints.

Three key constraints are applied to the model, each representing a limitation in bakery resources. The first constraint, 5*x1 + x2 <= 90, models oven time, where each Bowdoin log consumes 5 units of oven usage and each chocolate cake consumes 1 unit, with a total oven capacity of 90 units. The second constraint, x1 + 10*x2 <= 300, simulates food processor usage, where Bowdoin logs use 1 unit and chocolate cakes use 10, with 300 units of total capacity available. The third constraint, 4*x1 + 6*x2 <= 125, models the boiler usage, where the respective usage of the boiler is 4 and 6 units for Bowdoin logs and chocolate cakes, with a maximum limit of 125 units.

Once the problem is fully defined with the objective and constraints, the model is solved using PULP_CBC_CMD, which is an open-source solver integrated into PuLP. The solution provides the status of the optimization, which indicates whether an optimal solution was found. The decision variable values are then printed, showing how many units of each product the bakery should produce to maximize profits without exceeding resource limitations.

The final output displays the optimized values of x1 and x2, representing the number of Bowdoin logs and chocolate cakes to produce. It also displays the optimal value of the objective function, showing the maximum achievable profit under the given constraints. This result provides actionable insights to bakery managers, helping them allocate limited resources efficiently to achieve the best financial outcomes.

This project demonstrates the power of linear programming in operational decision-making. It shows how mathematical modeling and optimization can help businesses determine the best course of action under constraints. The use of Python’s PuLP library makes it accessible and replicable, enabling similar modeling for a wide range of real-world scenarios involving limited resources and profit maximization goals.
