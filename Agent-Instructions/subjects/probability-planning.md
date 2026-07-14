### Unit 1: The Foundations of Randomness

This unit transitions students from thinking deterministically to thinking probabilistically using basic Python loops and random number generators.

* **Notebook 1: Simulating Reality (The Law of Large Numbers).** Introducing `np.random.choice`. Students will simulate flipping a coin 10 times, then 10,000 times, plotting the running average to visually prove that chaotic short-term results always stabilize into long-term predictability.
* **Notebook 2: Combinatorics (Counting the Universe).** Using Python to calculate permutations and combinations. They will build a card deck simulator to calculate the exact theoretical probability of a poker hand, and then run a Monte Carlo simulation to verify it.
* **Notebook 3: Conditional Probability and Bayes' Theorem.** Moving from independent events to dependent events. The capstone of this unit will be building a rudimentary "Spam Filter" algorithm that updates the probability of an email being spam based on the presence of specific trigger words.

### Unit 2: Discrete Random Variables

Introducing the concept of Probability Mass Functions (PMFs) and mapping distinct events to numbers.

* **Notebook 1: Expected Value and Variance.** Teaching students how to evaluate risk. They will code a simulator for a casino game (like Roulette) to calculate the expected value, proving mathematically why "the house always wins."
* **Notebook 2: The Binomial Distribution.** Modeling success/failure experiments. They will write an algorithm to plot the PMF of flipping $N$ coins, applying it to quality assurance (e.g., the probability of getting exactly 3 defective chips in a batch of 50).
* **Notebook 3: The Poisson Distribution.** Modeling events over time or space. Students will simulate incoming traffic to a web server to find the probability of a system crash due to a sudden spike in users within a single minute.

### Unit 3: Continuous Random Variables

This is where probability shakes hands with the calculus concepts you built earlier. Since they already know numerical integration, this will be a breeze.

* **Notebook 1: PDFs and CDFs.** Transitioning from discrete bars to continuous curves. They will use numerical integration to find the area under a Probability Density Function, proving that the total area is exactly 1.
* **Notebook 2: The Exponential Distribution.** Modeling waiting times. Students will simulate the lifespan of machine parts or the arrival time of a bus, plotting the "memoryless" property of the exponential curve.
* **Notebook 3: The Normal Distribution.** The classic Bell Curve. They will code the Standard Normal PDF and build a `z_score` calculator to find the exact probability of an event falling within a specific standard deviation bracket.

### Unit 4: Joint Distributions (Multi-Dimensional Probability)

Real life rarely involves just one variable. This unit expands their worldview to how multiple random variables interact.

* **Notebook 1: 2D Probability.** Generating 3D histograms to visualize Joint PMFs. Students will learn how to extract the "Marginal Probability" (flattening the 3D graph into 2D) to isolate a single variable.
* **Notebook 2: Covariance and Correlation.** Are two random variables related? Students will generate synthetic scatter plots of data with perfect positive correlation, zero correlation, and negative correlation, and write the algorithm to calculate the Pearson correlation coefficient.

### Unit 5: The Grand Finale (The Limit Theorems)

Ending the course by proving the most magical, unifying concept in all of mathematics.

* **Notebook 1: The Central Limit Theorem (CLT) Sandbox.** The Central Limit Theorem states that if you take enough samples of *any* distribution and average them, the result will always form a perfect Normal Distribution.
* **Notebook 2: The Galton Board (Monte Carlo Finale).** The students will build a massive computational Galton Board (a pegboard where a ball bounces left or right randomly). They will watch a completely chaotic system naturally sort itself into a perfect mathematical bell curve, bridging the gap between Unit 1's coin flips and Unit 3's continuous calculus.
