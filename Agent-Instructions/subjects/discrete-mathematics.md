### Unit 1: Logic and State Machines (The Hardware of Math)

We start at the absolute rock bottom of computing: True and False.

* **Notebook 1: Boolean Algebra and Logic Gates.** Students will use Python's bitwise operators (`&`, `|`, `^`) to simulate physical AND, OR, and XOR gates. They will combine these simple gates to build a "Half-Adder" and a "Full-Adder," proving that simple true/false logic can perform mathematical addition.
* **Notebook 2: Truth Tables and the SAT Problem.** Instead of drawing truth tables by hand, students will write a script using `itertools` to generate truth tables for massive logical propositions. We will introduce the Boolean Satisfiability Problem (SAT)—explaining why finding a "True" in a massive grid of logic is one of the hardest problems in computer science.
* **Notebook 3: Finite State Machines (Automata).** Students will code a Deterministic Finite Automaton (DFA). They will build a simulated "vending machine" or a "password validator" that transitions between states based on input, which is the foundational math behind how computers parse code and text.

### Unit 2: Set Theory and Relations

Moving from True/False to collections of objects.

* **Notebook 1: Sets and the Power Set Explosion.** Using Python's native `set` structures to visualize unions, intersections, and differences. They will write a recursive algorithm to generate a Power Set (the set of all subsets) and plot its size, visually proving the terrifying $2^n$ exponential explosion.
* **Notebook 2: Relations as Matrices.** A mathematical relation (like "is greater than" or "is a sibling of") can be represented as a 2D grid of 1s and 0s (a Boolean matrix). Students will write code to check these matrices for Reflexivity, Symmetry, and Transitivity.
* **Notebook 3: Hashing and the Pigeonhole Principle.** The Pigeonhole Principle says if you have 10 pigeons and 9 holes, one hole must contain two pigeons. Students will prove this computationally by generating thousands of random numbers and feeding them into a Hash Map, watching "hash collisions" inevitably occur (the Birthday Paradox).

### Unit 3: Combinatorics and Complexity (Counting and Scaling)

How many ways can we arrange things, and how long will the computer take to do it?

* **Notebook 1: The Traveling Salesperson (Factorial Limits).** Students will use `itertools.permutations` to brute-force the shortest path between a list of cities. They will see it run instantly for 5 cities, take a few seconds for 10 cities, and completely freeze their computer for 15 cities, proving why $O(n!)$ algorithms are practically impossible.
* **Notebook 2: Recurrence Relations and Dynamic Programming.** We will look at the Fibonacci sequence. They will write a naive recursive function and watch it choke on $F(40)$. Then, they will introduce "Memoization" (saving previous answers to a dictionary), instantly solving $F(1000)$ and proving the power of algorithmic optimization.
* **Notebook 3: Big-O Visualization.** They will code a terrible sorting algorithm (Bubble Sort) and a great one (Merge Sort). Using Python's `time` module, they will race them on lists of increasing sizes and plot the runtimes, physically drawing the $O(n^2)$ and $O(n \log n)$ curves.

### Unit 4: Graph Theory (Networks and Routing)

Nodes and edges. This is the math of the internet, GPS, and social networks.

* **Notebook 1: Adjacency Matrices and Traversals.** Students will map a network of computers as a matrix. They will code Breadth-First Search (BFS) to simulate a computer virus spreading outward step-by-step, finding the shortest unweighted path to every node.
* **Notebook 2: Dijkstra's Algorithm.** What if the edges have weights (like traffic on a highway)? Students will code Dijkstra's Algorithm to find the absolute fastest route from Point A to Point B on a complex graph, mirroring how Google Maps actually works.
* **Notebook 3: Minimum Spanning Trees.** A telecommunications company needs to lay fiber optic cables to connect 20 cities as cheaply as possible. Students will implement Kruskal’s or Prim’s algorithm to find the absolute minimum amount of cable required without creating any redundant loops.

### Unit 5: Number Theory and Cryptography

The grand finale. All the discrete math comes together to secure the modern internet.

* **Notebook 1: Modular Arithmetic and the Sieve.** Students will build the Sieve of Eratosthenes to generate prime numbers. They will plot these primes on a Ulam Spiral, visually hunting for patterns in the most mysterious sequence in mathematics.
* **Notebook 2: The Euclidean Algorithm and Inverses.** They will write a highly optimized recursive Euclidean Algorithm to find the Greatest Common Divisor (GCD) of two massive numbers, and then reverse it to find the Modular Inverse—the mathematical "skeleton key" needed for decryption.
* **Notebook 3: RSA Encryption.** The ultimate capstone. Students will generate public and private keys using large prime numbers. They will take a secret string of text, convert it to ASCII integers, encrypt it into absolute mathematical garbage using someone's public key, and then successfully decrypt it back to readable text using the private key!

This curriculum guarantees that by the end of the course, students won't just view discrete math as an arbitrary set of rules, but as the literal source code that makes modern software possible.