Combinatorics is the ultimate computational playground. It is the mathematics of counting, arranging, and structuring discrete objects. In a traditional class, students are forced to write out endless strings of letters to understand permutations or memorize obscure binomial identities.

But computers are the undisputed masters of counting. By teaching combinatorics computationally, students can use Python's `itertools` to literally generate entire universes of possibilities, search them, and empirically prove theorems that feel like magic.

Here is a brainstorm for a five-unit Computational Combinatorics curriculum:

### Unit 1: The Art of Counting

We start by building the basic combinatorial toolkit, moving from brute-force loops to elegant Python libraries.

* **Notebook 1: Permutations and the Factorial Explosion.** Students will write their own nested loops to arrange letters, then graduate to `itertools.permutations`. They will attempt to generate all permutations of a 12-letter word and watch their RAM max out, computationally proving the sheer violence of $O(n!)$ growth.
* **Notebook 2: Combinations and Pascal's Triangle.** Order no longer matters. Students will use `itertools.combinations` to draw poker hands. They will write a recursive algorithm to generate Pascal's Triangle and use `matplotlib` to plot it as a grid, coloring in the odd and even numbers to instantly reveal the fractal Sierpinski Triangle hidden inside!
* **Notebook 3: The Stars and Bars Method.** How do you distribute 10 identical candies to 3 distinct children? Textbooks use a confusing visual metaphor of stars and dividing lines. Your students will write an algorithm to partition integers, computationally proving that the number of ways to do this matches the exact binomial coefficient formula.

### Unit 2: Advanced Counting and Sieves

What happens when the rules get complicated and sets start to overlap?

* **Notebook 1: The Principle of Inclusion-Exclusion (PIE).** Students will use Python's native `set` logic (`&`, `|`, `-`) to calculate the exact number of integers between 1 and 10,000 that are divisible by 2, 3, or 5, dynamically adding and subtracting the overlapping regions.
* **Notebook 2: Derangements (The Hat Check Problem).** If 100 people throw their hats in a pile and grab one at random, what is the probability that *nobody* gets their own hat back? Students will write a simulation to generate derangements, plotting the probability as the number of people grows. They will watch in awe as the curve instantly flattens out and perfectly converges to $1/e$ (about 36.7%), linking combinatorics directly to continuous calculus!
* **Notebook 3: The Pigeonhole Principle.** A foundational logic tool. Students will simulate a room of people generating random birthdays. They will computationally prove that you only need 23 people in a room to have a 50% chance of a shared birthday, graphing the collision probabilities to explain why cryptographic hashes fail.

### Unit 3: Recurrence and Generating Functions

Moving from counting static sets to counting sequences that grow over time.

* **Notebook 1: Dynamic Programming and the Catalan Numbers.** The Catalan numbers count the number of valid parentheses combinations or triangulations of a polygon. Students will write a recursive recurrence relation to generate them, optimize it using memoization, and plot the staggering growth rate.
* **Notebook 2: Generating Functions (Polynomial Counting).** A massive theoretical leap. Students will use the `numpy.poly1d` object to multiply massive polynomials together. They will discover that the coefficients of the resulting polynomial magically hold the exact answers to complex coin-change and partition problems.
* **Notebook 3: Integer Partitions.** How many ways can you add numbers together to make 50? Students will build a recursive partition generator and computationally verify Ramanujan's incredible congruence theorems (e.g., the number of partitions of $5n + 4$ is always divisible by 5).

### Unit 4: Graph Theory (Combinatorial Structures)

Combinatorics isn't just counting lists; it's counting connections.

* **Notebook 1: Trees and Cayley's Formula.** Cayley's formula states there are exactly $n^{n-2}$ ways to connect $n$ labeled nodes into a single tree without loops. Students will write an algorithm to generate labeled trees and computationally verify this bizarre, beautiful formula.
* **Notebook 2: Graph Coloring and Bipartite Sets.** Students will map out a conflict graph (like scheduling final exams without overlapping students). They will write a "Greedy Coloring" algorithm to assign colors to nodes, computationally finding the Chromatic Number of the graph.
* **Notebook 3: Eulerian Paths (The Bridges of Königsberg).** Can you trace a shape without lifting your pencil and without crossing the same line twice? Students will write an algorithm that checks the degree (number of connections) of every node, proving Euler's theorem that a path only exists if there are exactly zero or two nodes with an odd degree.

### Unit 5: Extremal and Symmetrical Combinatorics

The grand finale. Pushing structures to their absolute limits and counting under symmetry.

* **Notebook 1: Ramsey Theory (The Party Problem).** Ramsey Theory states that true chaos is impossible; if a structure is large enough, order *must* exist. Students will computationally brute-force color the edges of a 6-node graph red and blue. They will write a checker to prove that out of all 32,768 possible colorings, it is mathematically impossible to avoid creating a solid red or solid blue triangle.
* **Notebook 2: Combinatorial Designs (Magic Squares).** Students will write backtracking algorithms to construct 3x3 and 4x4 Magic Squares (where all rows, columns, and diagonals sum to the same number), treating combinatorics as a constraint-satisfaction puzzle.
* **Notebook 3: Burnside's Lemma.** How many unique ways can you color the 4 corners of a square using 3 colors? (If you rotate the square, it counts as the same coloring). Students will define the symmetry group of a square (rotations and reflections) as arrays, and write an algorithm that counts the "fixed points" of each transformation, writing code to perfectly filter out the duplicate symmetries.

---

This course transforms combinatorics from a frustrating game of "did I overcount?" into an absolute powerhouse of algorithmic generation and pattern discovery.
