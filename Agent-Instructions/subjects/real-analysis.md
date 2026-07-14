 It is very easy to accidentally turn a "Computational Real Analysis" course into a standard "Numerical Analysis" course, but they are fundamentally different beasts.

Numerical Analysis is about **approximation and hardware limitations**. It asks: *How do we calculate $\sqrt{2}$ when a CPU only has 64 bits of memory? How do we invert a matrix without floating-point rounding errors destroying the answer?*

Computational Real Analysis, on the other hand, is about **using the computer as a microscope to look at the fabric of the real numbers**. We aren't trying to approximate an answer for an engineering problem; we are writing code to construct pathological functions, visualize metric spaces, and watch point-set topology behave in real-time.

Here is a brainstorm for a five-unit Computational Real Analysis curriculum that avoids the Numerical Analysis trap and stays rigorously pure:

### Unit 1: The Topology of $\mathbb{R}$

Before we talk about functions, we have to talk about the strange structure of the real line itself.

* **Notebook 1: Open Covers and Compactness.** Students write an algorithm that generates a massive collection of random, overlapping open intervals. They will write a function to test if this collection successfully "covers" a target interval $[a, b]$, and then write an extraction algorithm to pull out a finite subcover, visually demonstrating the Heine-Borel theorem.
* **Notebook 2: The Cantor Set.** Students write a recursive algorithm to generate the Cantor Middle-Third set. By plotting the iterations and calculating the remaining length, they computationally prove it has a "measure" (length) of exactly zero, yet somehow contains an uncountable number of points.
* **Notebook 3: Connectedness and Density.** A visual exploration of dense sets. Students will generate arrays of floating-point numbers to simulate $\mathbb{Q}$ and $\mathbb{R} \setminus \mathbb{Q}$, showing how they interleave infinitely tightly without ever actually touching.

### Unit 2: Sequences of Functions

In standard calculus, we take the limit of a sequence of numbers. In analysis, we take the limit of a sequence of entire graphs.

* **Notebook 1: Pointwise vs. Uniform Convergence.**  Students will plot the sequence of functions $f_n(x) = x^n$ on the interval $[0, 1]$. They will animate the graph as $n \to \infty$ and visually witness a sequence of perfectly continuous, smooth curves violently snap into a discontinuous cliff, proving that pointwise convergence does not preserve continuity.
* **Notebook 2: The Uniform Metric.** To fix the problem in Notebook 1, students code the "Supremum Norm" (the maximum vertical distance between two functions). They will write an $\epsilon$-tube algorithm to test if a sequence of functions converges uniformly, safely preserving continuity.
* **Notebook 3: Power Series and the Radius of Convergence.** Students computationally explore why the Taylor series for $f(x) = \frac{1}{1+x^2}$ works perfectly between $-1$ and $1$, but violently explodes outside that radius, even though the original function is completely smooth and continuous everywhere.

### Unit 3: Pathological Monsters

Real Analysis was largely invented because mathematicians kept discovering "monster" functions that broke all the rules of calculus. Python is the perfect tool to summon them.

* **Notebook 1: The Popcorn Function (Thomae's Function).** A function that is continuous at every irrational number, but discontinuous at every rational number. Students will code this using the fractions module and plot it as a scatter plot, seeing the "raindrops" or "popcorn" shape emerge.
* **Notebook 2: The Weierstrass Function.**  The ultimate monster: a function that is continuous everywhere, but differentiable *nowhere*. Students will code the infinite sum of shrinking cosines, zoom in on the plot 10,000x, and see that it remains completely jagged at every microscopic level.
* **Notebook 3: Space-Filling Curves.** Is a 2D square "bigger" than a 1D line? Students write a recursive algorithm to draw the Hilbert curve. They will watch a single, continuous 1D string fold in on itself until it perfectly colors in a solid 2D square, breaking their intuition about dimensions.

### Unit 4: Measure Theory and the Lebesgue Integral

The Riemann integral (slicing area into vertical rectangles) is fundamentally broken for pathological functions. We need to upgrade to Lebesgue integration (horizontal slicing).

* **Notebook 1: Outer Measure.** Students write an algorithm that tries to wrap a set of points in the smallest possible boxes, calculating the "Lebesgue Outer Measure." They will test this on the Cantor set and the rational numbers.
* **Notebook 2: Breaking the Riemann Integral.** Students will attempt to use a standard Riemann sum algorithm on the indicator function of the rationals (the Dirichlet function). They will watch the area oscillate wildly between 0 and 1 depending on where the rectangles fall, proving Riemann's failure.
* **Notebook 3: The Lebesgue Integral.** Students write a new integration algorithm that groups the function by its $y$-values instead of its $x$-values (measuring the "size" of the pre-image). They will apply it to the Dirichlet function, instantly outputting the correct area of $0$.

### Unit 5: Metric Spaces

Generalizing the concept of "distance" beyond the standard ruler.

* **Notebook 1: Alternate Geometries.** Students define custom Python distance functions for the Euclidean metric, the Taxicab (Manhattan) metric, and the Discrete metric. They will write code to plot a "circle" (all points a distance of 1 from the origin) in each metric, watching the circle become a square, a diamond, or a single dot.
* **Notebook 2: Completeness.** What does it mean for a space to have no "holes"? Students simulate Cauchy sequences (sequences whose terms get closer and closer together) in $\mathbb{Q}$ and watch them "converge" to $\sqrt{2}$, which doesn't exist in $\mathbb{Q}$, proving the space is incomplete.
* **Notebook 3: The Banach Fixed-Point Theorem.** The capstone of the course. Students write a "Contraction Mapping" algorithm. They will drop a random starting point into the function and iteratively feed the output back into the input, proving that it will always inevitably get sucked into a single, inescapable "black hole" (the fixed point).
