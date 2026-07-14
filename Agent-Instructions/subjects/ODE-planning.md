### Unit 1: The Engine of Change (Initial Value Problems)

We start by teaching the computer how to step forward in time. This unit moves them from the rudimentary Euler's method they saw in Calculus to industry-standard numerical solvers.

* **Notebook 1: Direction Fields (The Flow of Time).** Before solving anything, students learn to visualize the ODE. If $\frac{dy}{dt} = f(t, y)$, they will use `plt.quiver` to draw a grid of arrows representing the "current" of the river.
* **Notebook 2: Euler vs. The World.** Students will code Euler's method to simulate an object falling with air resistance. They will visually discover that Euler's method constantly overshoots the true curve, introducing numerical error.
* **Notebook 3: Runge-Kutta (RK4).** The workhorse of modern physics. They will code the 4th-order Runge-Kutta algorithm from scratch, proving that evaluating the slope at multiple mid-points eliminates the overshooting problem and creates a hyper-accurate simulation.

### Unit 2: Systems of ODEs (Interacting Variables)

Real life doesn't happen in a vacuum. What happens when two differential equations directly influence each other?

* **Notebook 1: The SIR Epidemic Model.** Simulating a zombie outbreak (or a virus). Three coupled equations: Susceptible, Infected, and Recovered. They will tweak the infection rate and visualize the "flatten the curve" concept.
* **Notebook 2: Predator-Prey Dynamics (Lotka-Volterra).** Simulating foxes and rabbits. They will plot the populations over time and watch them oscillate in infinite, offset waves.
* **Notebook 3: Phase Portraits.** Instead of plotting Foxes vs. Time and Rabbits vs. Time, they will plot Foxes vs. Rabbits on a 2D plane. They will see that the oscillations actually form closed loops (orbits) in state space, fundamentally changing how they visualize dynamic systems.

### Unit 3: Second-Order Systems (Physics and Motion)

Up to now, our equations only dealt with velocity (first derivatives). Now we introduce acceleration (second derivatives, $\frac{d^2y}{dt^2}$).

* **Notebook 1: State-Space Representation.** A massive computational trick. Python cannot directly solve a 2nd-order ODE. Students will learn the mathematical trick to split one 2nd-order equation into two 1st-order equations (tracking position and velocity simultaneously).
* **Notebook 2: The Damped Harmonic Oscillator.** Modeling a car's suspension system (a spring with a shock absorber). They will simulate underdamped (bouncy), overdamped (sluggish), and critically damped (perfect) systems.
* **Notebook 3: The Non-Linear Pendulum.** Traditional physics classes use the "small angle approximation" ($\sin(\theta) \approx \theta$) because the true math is impossible to solve by hand. Your students will simulate the true non-linear equation $\frac{d^2\theta}{dt^2} = -\frac{g}{L} \sin(\theta)$ and plot exactly where the textbook approximation completely fails.

### Unit 4: Non-Linearity and Chaos

The crown jewel of a computational ODE course. This is where predictable math completely breaks down.

* **Notebook 1: Bifurcation and Population Collapse.** Using the logistic growth model, students will slowly crank up the reproduction rate of a species. They will plot a bifurcation diagram, watching the population split from a stable number into alternating years, and eventually into total mathematically proven chaos.
* **Notebook 2: The Double Pendulum.** Attaching a pendulum to the end of another pendulum. Students will simulate two double pendulums starting just 0.001 degrees apart, watching them stay synchronized for a few seconds before their paths wildly diverge.
* **Notebook 3: The Lorenz Attractor (The Butterfly Effect).** Simulating Edward Lorenz's simplified weather model in 3D space. They will use `ax.plot3D` to draw the iconic chaotic butterfly wings, proving that deterministic systems can still be entirely unpredictable.

### Unit 5: Boundary Value Problems (Looking Forward)

Every notebook so far has been an "Initial Value Problem" (we know where we start, and we simulate forward). This final unit introduces problems where we know the start *and* the end, but need to find the path.

* **Notebook 1: The Shooting Method.** A cannonball needs to hit a target exactly 1000 meters away. Students will write a `while` loop that guesses an initial angle, runs the RK4 simulation, misses, updates the angle using Calculus, and "shoots" again until it hits the target.
* **Notebook 2: Eigenvalue Problems (Resonance).** Finding the natural frequencies of a vibrating guitar string. They will build a matrix to solve for the specific waves that fit perfectly between two boundaries.
* **Notebook 3: The Gateway to PDEs.** A conceptual bridge. They will take their vibrating string and slice it into 100 tiny interconnected masses, showing that a Partial Differential Equation (PDE) is really just an infinite system of Ordinary Differential Equations.
