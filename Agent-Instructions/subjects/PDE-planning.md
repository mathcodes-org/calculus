### Unit 1: Discretizing the Universe (Finite Differences)

Before we can simulate physics, we have to teach the computer how to chop space and time into a grid.

* **Notebook 1: The Finite Difference Method.** Students revisit the difference quotient from Calculus 1, but apply it to matrices. They will build the numerical tools to calculate $\frac{\partial u}{\partial x}$ and $\frac{\partial^2 u}{\partial x^2}$ across an entire 1D array.
* **Notebook 2: The 1D Advection Equation.** The simplest PDE. Simulating a blob of dye moving down a river at a constant speed. They will write their first "Explicit Time-Stepping" loop.
* **Notebook 3: The CFL Condition (When Math Explodes).** A crucial lesson in computational stability. Students will try to make time step $\Delta t$ too large and watch their simulation violently shoot to infinity. They will learn the mathematical speed limit of simulations (the Courant-Friedrichs-Lewy condition).

### Unit 2: Parabolic PDEs (Heat and Diffusion)

Modeling how things spread out and smooth over time.

* **Notebook 1: The 1D Heat Equation.** A metal rod heated at one end. They will use the second spatial derivative to watch the temperature slowly diffuse across the rod until it reaches equilibrium.
* **Notebook 2: The 2D Heat Equation.** Expanding to a flat plate. They will code the exact 3D simulation you teased at the end of the Calculus course, dropping a massive spike of heat in the center and watching it dissipate using `plt.contourf`.
* **Notebook 3: Implicit Solvers (Matrix Magic).** Explicit loops are slow because the CFL condition forces tiny time steps. Students will use Linear Algebra to invert a massive matrix, solving for the entire next time step simultaneously (the Backward Euler or Crank-Nicolson method), allowing them to fast-forward the simulation safely.

### Unit 3: Hyperbolic PDEs (Waves and Sound)

Moving from things that slowly diffuse to things that propagate and reflect.

* **Notebook 1: The 1D Wave Equation.** Simulating a plucked guitar string. Unlike heat, waves require the second derivative of *time* ($\frac{\partial^2 u}{\partial t^2}$), meaning the computer has to remember both the current time step and the previous time step to calculate momentum.
* **Notebook 2: Boundaries and Interference.** What happens when a wave hits a wall? Students will code "Dirichlet" (fixed) and "Neumann" (free) boundary conditions, watching waves reflect, invert, and pass through each other to create standing waves.
* **Notebook 3: The 2D Wave Equation (The Ripple Effect).** Dropping a simulated pebble into a square pond. They will use `plot_surface` to watch the ripples expand in a circle, bounce off the square walls, and create complex interference patterns.

### Unit 4: Elliptic PDEs (Steady-State and Potentials)

What happens when time stops? If you leave a simulation running forever, it settles into a "steady state." These PDEs have no time derivative at all.

* **Notebook 1: Laplace's Equation.** If a square metal plate is permanently frozen on three sides and boiling on the fourth, what does the temperature look like in the middle? Students will write an iterative solver (Jacobi iteration) that just averages every point with its four neighbors until the grid stops changing.
* **Notebook 2: Poisson's Equation.** Laplace's equation, but with a source. Students will simulate the electrostatic potential around a positively charged particle and a negatively charged particle on a 2D grid.
* **Notebook 3: Solving via Linear Algebra.** Iterative `while` loops are slow. Students will flatten their 2D grid into a massive 1D vector and construct a sparse matrix to solve Laplace's equation instantly using `np.linalg.solve`.

### Unit 5: Non-Linear PDEs (The Gateway to Fluids)

The grand finale. When a PDE multiplies a variable by its own derivative, the math gets wild, creating shockwaves and patterns.

* **Notebook 1: Burgers' Equation.** The bridge between waves and fluid dynamics. Students will simulate a wave where the top moves faster than the bottom. They will literally watch the wave steepen and "crash" into a vertical shockwave, which is the exact math used to model traffic jams.
* **Notebook 2: Reaction-Diffusion (Turing Patterns).** How does a leopard get its spots? Alan Turing proposed it was two chemicals (a predator and a prey chemical) diffusing and reacting. Students will simulate this coupled PDE system and watch random static organically resolve into stunning biological stripes and spots.
* **Notebook 3: The Shallow Water Equations.** A simplified version of the legendary Navier-Stokes equations. Students will simulate a dam breaking inside a 2D box, watching the water slosh, reflect, and swirl.
