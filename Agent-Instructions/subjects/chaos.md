### Unit 1: The Onset of Chaos (1D Dynamics)

We start with the simplest possible equations: 1D iterative maps. How does a single equation, repeatedly fed into itself, destroy predictability?

* **Notebook 1: Cobweb Plots and Fixed Points.** Students will code the Logistic Map $x_{n+1} = rx_n(1-x_n)$, which models population growth. They will write an algorithm to draw "Cobweb Plots," visually tracing the path of a population as it spirals into a stable fixed point or a repeating cycle.
* **Notebook 2: The Bifurcation Diagram.** The iconic tree of chaos. Students will write a massive loop that sweeps the growth rate $r$ from 1 to 4, plotting the final states of the population. They will visually discover the "Period-Doubling Cascade" and zoom in to computationally prove the fractal nature of the diagram.
* **Notebook 3: The Butterfly Effect (Lyapunov Exponents).** What exactly *is* chaos? Students will simulate two starting populations separated by only $10^{-8}$. They will plot the distance between them over time, watching it grow exponentially. They will calculate the Lyapunov Exponent, proving that a positive exponent guarantees sensitive dependence on initial conditions.

### Unit 2: Symbolic Dynamics (The Math of the Shift)

This is where continuous math becomes discrete computer science. We can map chaotic real numbers perfectly to strings of letters!

* **Notebook 1: Itineraries and The Tent Map.** Students will divide the domain of a chaotic map into a "Left" (L) and "Right" (R) side. As they iterate a point, they will record an $L$ or $R$ depending on where it lands, generating an infinite string of characters. They will write code to prove that every starting decimal produces a perfectly unique barcode of $L$s and $R$s.
* **Notebook 2: The Shift Space.** Instead of doing math on numbers, students will do math on strings. They will write the "Shift Operator" (which simply drops the first letter of a string) and build a custom distance function between two strings.
* **Notebook 3: Topological Conjugacy.** The ultimate bridge. Students will computationally prove that iterating the continuous, chaotic Logistic Map is mathematically identical to just randomly flipping a coin and shifting a sequence of $L$s and $R$s. They will use Python dictionaries to translate the continuous chaos perfectly into discrete symbol shifts.

### Unit 3: The Geometry of Chaos (Fractals)

Chaos in time produces fractals in space. Because chaotic systems never repeat, their orbits draw infinitely detailed geometric shapes.

* **Notebook 1: Recursive Monsters.** Students will use recursive Python functions to generate classical mathematical fractals: the Cantor Set, the Koch Snowflake, and the Sierpinski Gasket.
* **Notebook 2: Fractional Dimension (Box-Counting).** How can a shape be 1.26 dimensional? Students will write a "Box-Counting" algorithm. They will feed images of the coast of Britain, a circle, and a fractal into their algorithm. The code will lay grids of decreasing sizes $\epsilon$ over the image, counting the intersecting boxes $N$, and use linear regression on a $\log(N)$ vs $\log(1/\epsilon)$ plot to extract the exact fractal dimension.
* **Notebook 3: The Chaos Game (Iterated Function Systems).** A mind-bending probabilistic proof. Students will define three fixed points. They will drop a random dot, pick a point at random, and move the dot exactly halfway there, leaving a trail. They will watch random, chaotic coin flips magically draw the perfectly structured Barnsley Fern on their screen.

### Unit 4: Strange Attractors and Continuous Chaos

Moving from 1D loops to 2D and 3D differential equations.

* **Notebook 1: Stretching and Folding (The Hénon Map).** Chaos requires two things: stretching (to separate close points) and folding (to keep them trapped in a boundary). Students will simulate the 2D Hénon map, visualizing a blob of data points getting stretched like taffy and folded like a baker's dough into an infinitely layered strange attractor.
* **Notebook 2: Slicing the Lorenz Attractor.** The famous 3D weather model. Students will simulate the Lorenz butterfly, but 3D plots are messy. They will write an algorithm to create a **Poincaré Section**—placing a 2D "pane of glass" in the middle of the 3D space and only plotting a dot when the trajectory smashes through it, revealing the hidden 1D structure inside the 3D chaos.
* **Notebook 3: Basin Boundaries.** If a system has two stable resting places, how does it decide which one to go to? Students will simulate a magnetic pendulum hovering over three magnets. They will color the starting grid based on which magnet the pendulum eventually lands on, revealing a Wada Basin—a fractal boundary where all three colors touch at every single point.

### Unit 5: Cellular Automata and the Edge of Chaos

We end by leaving equations entirely behind. Can purely discrete, localized rules generate universal complexity?

* **Notebook 1: 1D Automata (Wolfram's Rule 30).** Students will create a 1D array of 0s and 1s. They will write an algorithm where each pixel looks only at its immediate neighbors to determine its color on the next row. They will discover Rule 30, which turns a single black pixel into an aperiodic, chaotic triangle (used historically by Mathematica as a random number generator).
* **Notebook 2: Conway’s Game of Life.** The most famous 2D cellular automaton. Students will build the engine for Life using vectorized `numpy` operations (via `scipy.signal.convolve2d` for speed). They will code "Gliders," "Gosper Glider Guns," and prove that simple birth/death rules can simulate a Turing machine.
* **Notebook 3: Langton's Lambda (The Edge of Chaos).** Students will write a script that randomly generates cellular automata rules based on a parameter $\lambda$. They will sweep $\lambda$ from 0 to 1, watching the systems transition from rigid, dead crystals ($\lambda < 0.2$), into chaotic static ($\lambda > 0.4$). Right at the phase transition ($\lambda \approx 0.27$), they will discover the "Edge of Chaos"—the narrow band where all complex, life-like computation actually occurs.

