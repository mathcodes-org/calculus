This is a fascinating pivot. Designing a computational course for *Pure Mathematics* requires a completely different philosophy than applied math or computer science.

In applied math, we use computers to find numerical answers (like simulating a bouncing ball or minimizing a cost function). But for a pure math major preparing for Real Analysis and Abstract Algebra, the computer cannot *prove* an infinite theorem for them.

Instead, the computational goal here is **Falsification and Visualization**. We use Python to search for counterexamples, build finite models of abstract algebraic structures, and create visual sandboxes for the hardest definitions in mathematics (like $\delta-\epsilon$ proofs).

Here is a brainstorm for a five-unit Computational Intro to Proofs curriculum tailored strictly for pure math majors:

### Unit 1: Logic, Quantifiers, and Counterexamples

Pure math relies heavily on understanding the difference between "For all" ($\forall$) and "There exists" ($\exists$). Students struggle with the order of quantifiers.

* **Notebook 1: Truth, Vacuous Truth, and Implication.** Moving beyond basic AND/OR gates. Students will write Python functions to evaluate conditional statements ($P \implies Q$). They will computationally explore "Vacuous Truth" by writing a loop over an empty list and proving that any universal statement about an empty set evaluates to True.
* **Notebook 2: The Quantifier Sandbox.** Exploring the difference between $\forall x \exists y$ and $\exists y \forall x$. Students will write nested loops over finite integer domains to evaluate complex logical propositions. They will visually prove that swapping the order of the loops completely changes the truth value of the mathematical statement.
* **Notebook 3: The Counterexample Engine.** To disprove a universal statement, you only need one counterexample. Students will write brute-force search algorithms to test famous conjectures (like Euler's sum of powers conjecture or basic prime number claims), forcing the computer to hunt for the single integer that breaks the rule.

### Unit 2: Functions, Cardinality, and Infinity

Preparing students to think about mappings and the sizes of infinity, rather than just treating functions as formulas.

* **Notebook 1: Injections, Surjections, and Bijections.** Students will write code to mathematically check if a dictionary mapping between two finite sets is one-to-one or onto. If it fails, the code must explicitly print the elements that break the definition (e.g., "Not injective: elements A and B both map to C").
* **Notebook 2: Composition and Inverses.** They will define abstract functions as Python objects, compose them ($f \circ g$), and computationally verify the theorem that a function only has an inverse if it is bijective.
* **Notebook 3: Cantor's Diagonalization.** A computational simulation of the most famous proof in mathematics. Students will write an algorithm that takes a generated list of infinite binary strings (represented as long arrays), walks down the diagonal, flips the bits, and constructs a brand new string that is mathematically guaranteed to *not* be in the original list.

### Unit 3: Relations and Abstract Structures

This unit is the direct bridge to Abstract Algebra, teaching them how to group numbers into equivalence classes.

* **Notebook 1: Equivalence Relations.** Students will write functions to test if a given mathematical relation (like "has the same parity as" or "divides") is Reflexive, Symmetric, and Transitive over a specific domain.
* **Notebook 2: Partitions and Quotients.**  The fundamental theorem of equivalence relations states that they partition a set into disjoint classes. Students will write an algorithm that takes a set and a relation, and automatically groups the elements into a list of disjoint subsets, physically constructing the quotient set.
* **Notebook 3: Modular Arithmetic (Building a Ring).** Instead of just using the `%` operator, students will build a custom Python class for $\mathbb{Z}_n$. They will overload the addition and multiplication operators to build their very first finite mathematical "Ring," computationally generating Cayley tables to visualize the algebraic structure.

### Unit 4: The Architecture of the Reals ($\mathbb{R}$)

Preparing students for Real Analysis by exploring exactly what makes the Real numbers different from the Rationals ($\mathbb{Q}$).

* **Notebook 1: Supremum and Infimum.** The Least Upper Bound property is the bedrock of Real Analysis. Students will generate bounded sequences of numbers and write algorithms to find the supremum. They will contrast this with the concept of a "Maximum," computationally proving that a set can have a supremum without actually containing it.
* **Notebook 2: The Density of the Rationals.** A visual exploration of the theorem that between any two real numbers, there is a rational number. Given two incredibly close floating-point numbers, students will write an algorithm that constructs a fraction $\frac{p}{q}$ that fits perfectly between them.
* **Notebook 3: Cauchy Sequences.** What does it mean for a sequence to converge without knowing the limit? Students will simulate sequences, writing a script to measure the distance between terms $a_n$ and $a_m$ as $n, m \to \infty$, watching the "tail" of the sequence crush together into an infinitely dense point.

### Unit 5: The $\delta-\epsilon$ Limit Sandbox

The absolute terror of second-year math majors. This notebook turns the rigorous definition of a limit into a dynamic, visual game.

* **Notebook 1: Visualizing $\epsilon$-Tubes.** Students define a function $f(x)$ and a proposed limit $L$. They will use `matplotlib` to draw a horizontal tube of width $2\epsilon$ around $L$. They will instantly see that if they zoom in close enough, the function might break out of the top or bottom of the tube.
* **Notebook 2: The $\delta$-Response Algorithm.** The definition of a limit is a game: "You give me an $\epsilon > 0$, I give you a $\delta > 0$." Students will write an algorithm that takes any $\epsilon$ and computationally searches for the correct $\delta$ window on the x-axis that perfectly traps the function inside the $\epsilon$-tube.
* **Notebook 3: Continuous vs. Discontinuous.** Using their new $\delta-\epsilon$ engine, they will test a continuous function and a piecewise discontinuous function (like the Dirichlet function). They will watch the algorithm easily find a $\delta$ for the continuous curve, but completely crash and fail to find one for the discontinuous curve, visually proving the failure of the limit.
