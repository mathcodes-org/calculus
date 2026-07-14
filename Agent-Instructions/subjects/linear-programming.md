Linear Programming (LP) is an incredible topic to teach computationally. In a traditional Operations Research or Business Math class, students spend weeks drawing 2D polygons by hand or grinding through Simplex tableaus, fraction by agonizing fraction. It is pure arithmetic misery.

But computationally, Linear Programming is the engine that runs Amazon's supply chain, Delta's airline scheduling, and the global power grid. By using Python, students can skip the manual arithmetic and focus on formulating complex models and understanding the economic insights (like shadow prices) hidden inside the matrices.

Here is a brainstorm for a five-unit Computational Linear Programming curriculum:

### Unit 1: The Geometry of Optimization

Before we introduce matrices or solver libraries, students need to physically see what "optimization" actually means in space.

* **Notebook 1: Inequalities and the Feasible Region.** Students will use `matplotlib.pyplot.fill_between` to graph multiple linear inequalities (constraints like factory labor and materials). They will visually discover the "Feasible Region"—the polygon containing all legally allowed manufacturing combinations.
* **Notebook 2: The Objective Function and Corner Points.** We introduce the profit equation (e.g., $Z = 3x + 5y$). Students will plot the objective function as a contour line. They will write a loop to animate the line "sliding" across the graph, visually proving the Fundamental Theorem of Linear Programming: the optimal solution always lives on a corner!
* **Notebook 3: High-Dimensional Solvers.** Transitioning from 2D graphs to $N$-dimensional space. Students will learn to translate word problems into standard matrix form (the cost vector $\vec{c}$, the constraint matrix $A$, and the bounds $\vec{b}$). They will feed these into `scipy.optimize.linprog` to instantly solve a massive 10-variable production problem.

### Unit 2: Under the Hood (The Simplex Algorithm)

They know how to use the black-box solver; now they will build the black box.

* **Notebook 1: Standard Form and Slack Variables.** Inequalities ($\le$) are mathematically messy. Students will write a Python script that automatically injects "slack variables" to turn every inequality into a perfect system of linear equations, preparing the starting matrix.
* **Notebook 2: The Simplex Engine.** Instead of doing tableaus by hand, students will write a `while` loop that executes the Simplex algorithm. They will code the "Minimum Ratio Test" to find the pivot row, and use Gaussian elimination (from their Linear Algebra tools) to jump from corner to corner until the profit stops increasing.
* **Notebook 3: Degeneracy and Edge Cases.** What happens when the math breaks? Students will simulate scenarios where the solver gets trapped in an infinite loop (cycling), where the feasible region is open to infinity (unbounded), or where an entire line segment of perfect solutions exists.

### Unit 3: Duality and the Value of Resources

This is where LP transitions from pure math into economics.

* **Notebook 1: The Primal and the Dual.** Every maximization problem (the Primal) has a mirrored minimization problem hidden inside it (the Dual). Students will transpose their $A$ matrix, swap their $\vec{c}$ and $\vec{b}$ vectors, solve both problems, and computationally verify the Strong Duality Theorem: $Z_{max} = W_{min}$.
* **Notebook 2: Shadow Prices (Marginal Value).** If a factory is capped at 100 hours of labor, how much should the boss pay to unlock the 101st hour? Students will write a "Sensitivity Analysis" loop, incrementally increasing a constraint limit and plotting the change in total profit to discover the exact monetary value of the bottleneck (the shadow price).
* **Notebook 3: The Diet Problem.** The classic 1930s optimization problem. Students will scrape real nutritional data and formulate an LP to minimize the cost of a daily diet while hitting all FDA vitamin constraints. They will analyze the Dual variables to discover which vitamins are the most mathematically "expensive" to fulfill.

### Unit 4: Network Optimization (Routing the World)

LP isn't just about factory production; it's about moving things through networks.

* **Notebook 1: The Transportation Problem.** Moving goods from 3 factories to 5 warehouses. The challenge here is translating 2D flow variables ($x_{i,j}$) into a flattened 1D array. Students will write an algorithm to automatically generate the massive, sparse $A$ matrix required to minimize global shipping costs.
* **Notebook 2: Maximum Flow.** Formulating water flowing through pipes (or data through servers) as an LP problem. They will use the "Incidence Matrix" of a graph to enforce a strict Conservation of Flow constraint (Flow In = Flow Out) at every single intersection.
* **Notebook 3: The Assignment Problem.** Matching $N$ Uber drivers to $N$ riders to minimize total wait time. Students will discover a miraculous property of network LP matrices (Total Unimodularity): even without forcing the computer to use integers, the LP solver will naturally output perfect $1$s and $0$s!

### Unit 5: Integer Programming (The Hard Problems)

What happens when you cannot have a fraction of a solution? You can't build 2.5 airplanes.

* **Notebook 1: The Continuous Relaxation Trap.** Students will attempt to solve an integer problem by just running a standard LP and rounding the decimals to the nearest whole number. They will graphically prove that rounding often violates the constraints, pushing the solution outside the feasible region, or results in a terrible sub-optimal answer.
* **Notebook 2: Branch and Bound.** Students will write a recursive algorithm to solve Integer Programs. If the continuous solver outputs $x = 3.4$, their code will split the universe into two new LP problems ($x \le 3$ and $x \ge 4$), building a massive decision tree and pruning branches until it finds the mathematically perfect integer solution.
* **Notebook 3: The Knapsack Problem.** The ultimate capstone. A thief has a backpack with a 50 lb limit and a room full of items of varying weights and values. Students will formulate this as a Binary Integer Program ($x \in \{0, 1\}$). They will solve it, touching the very edge of NP-Hard computer science problems!

---

This course takes a subject that is often perceived as dry and turns it into a high-powered toolkit for solving massive, real-world logistical puzzles.

