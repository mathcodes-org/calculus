# Python Notebooks: Calculus

Welcome to the **Python Notebooks: Calculus** repository. This curriculum is designed to teach Calculus 1 entirely through code. Instead of memorizing formulas and performing tedious algebraic manipulations by hand, you will learn calculus by building it. By combining numerical methods with a custom-built symbolic engine in Python, you will gain a deep, functional understanding of both mathematics, computer science and some physics.

---

## Topics

### Unit 0: Foundations, Functions, and Limits

* **Representing Functions**: Defining mathematical functions using Python `def` and `lambda` functions.
* **Visualization**: Introduction to `matplotlib` or `plotly`. Graphing functions to visually identify domains, ranges, and asymptotes.
* **Numerical Limits**: Writing functions to evaluate limits as a variable approaches a specific value using decreasing step sizes (e.g., 0.1, 0.01, 0.001).
* **Floating-Point Realities**: A candid lesson on computer limits. Understanding why Python sometimes outputs 0.30000000000000004. Exploring machine epsilon and precision errors when dealing with infinitesimally small numbers.
* **Asymptotes and Infinity**: Handling `ZeroDivisionError` exceptions and utilizing `numpy.inf`.

### Unit 1: The Derivative

* **Secant to Tangent**: Plotting a secant line between two points, then animating a loop where the second point moves closer to the first.
* **The Difference Quotient**: Implementing the formal definition of a derivative numerically: $f'(x) \approx \frac{f(x+h) - f(x)}{h}$
* **Tuning the Step Size**: Experimenting with different values for the step size. Observing how overly large steps create mathematical inaccuracies, while overly small steps introduce floating-point errors.
* **Graphing the Derivative**: Evaluating the numerical derivative across an array of points (using `numpy`) and plotting the derivative alongside the original function to visually connect slopes to y-values.

### Unit 2: Building the Symbolic Framework

* **Expressions as Objects**: Creating Python Object-Oriented Programming (OOP) classes for Variable, Constant, Add, Multiply, and Power.
* **The `.evaluate()` Method**: Giving these classes the ability to compute a final numerical value when the variable is assigned a specific number.
* **The `.derive()` Method**: Implementing the Power Rule inside the Power class, the Sum Rule inside the Add class, and so on.
* **The Product and Quotient Rules**: Expanding the mathematical engine to handle combinations of functions.
* **The Chain Rule**: Teaching the engine how to handle nested objects (e.g., a Power object that contains an Add object).
* **Comparison**: Briefly introducing the `sympy` library to compare your homemade engine against an industry-standard symbolic solver.

### Unit 3: Applications of Derivatives

* **Root Finding (Newton's Method)**: Writing a `while` loop that uses the custom derivative engine to iteratively find where a function equals zero.
* **Optimization (Gradient Ascent/Descent)**: Using a step-size multiplier (learning rate) to computationally "walk" up or down a function to find local maxima and minima, rather than solving algebraically.
* **Curve Sketching via Data**: Writing a script that automatically identifies critical points and inflection points, marks them on a generated plot, and performs function interpolation.
* **Kinematics**: Simulating object motion. Given a position function in code, deriving velocity and acceleration to plot the object's path over time.

### Unit 4: Integration

* **Riemann Sums**: Writing loops to calculate the area under a curve using Left, Right, and Midpoint rectangles.
* **The Trapezoidal Rule**: Implementing a more accurate numerical integration method.
* **Convergence and Error**: Graphing the difference between the numerical integral and the "true" value as the number of rectangles increases.
* **Accumulation Functions**: Creating an array of cumulatively summed areas to plot the integral function alongside the original function.

### Unit 5: The Fundamental Theorem of Calculus & Symbolic Integration

* **The Fundamental Theorem**: Using code to demonstrate that taking the numerical derivative of a numerical integral returns the original function.
* **Expanding the Engine**: Adding an `.integrate()` method to the symbolic classes (limited to basic polynomials and powers, acknowledging the complexity of full symbolic integration).
* **Area Between Curves**: Writing a script that dynamically finds the intersection points of two functions using the Newton's Method solver, then numerically integrates the absolute difference between them.

---

## Guide

### How to open and use notebooks

These lessons are built using Jupyter Notebooks (files ending in `.ipynb`). You have a few options for opening and interacting with them:

* **Cloud (Easiest)**: Upload the notebooks to [Google Colab](https://colab.research.google.com/). This requires zero setup and runs entirely in your browser using Google's servers.
* **Local Application**: Use an IDE like [Visual Studio Code (VS Code)](https://code.visualstudio.com/) with the Jupyter extension installed, or launch JupyterLab directly from your terminal.

### How to install Python (local)

If you choose to run these notebooks locally, you will need Python installed on your machine.

* **Anaconda**: Download and install the [Anaconda Distribution](https://www.anaconda.com/download). It comes pre-packaged with Python, Jupyter, `numpy`, and `matplotlib`, which are heavily used in this curriculum.
* **Standalone Python**: Alternatively, download Python directly from [python.org](https://www.python.org/downloads/). You will then need to install Jupyter and required libraries manually via your terminal using pip (e.g., `pip install notebook numpy matplotlib`).

### How to use Python

While this course teaches calculus, it assumes a basic familiarity with Python. You should be comfortable with:

* Variable assignment and basic data types (integers, floats, strings, lists).
* Control flow constructs (`for` loops, `while` loops, `if/else` statements).
* Writing functions using `def`.
* The basics of Object-Oriented Programming (classes, objects, methods), which will be crucial for Unit 3.

If you are entirely new to Python, consider completing a brief introductory Python tutorial before diving into the calculus notebooks.

Here are some links: 