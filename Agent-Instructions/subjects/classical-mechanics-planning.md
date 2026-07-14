### Unit 1: Newtonian Dynamics and Numerical Integration

We start by upgrading $F = ma$ into a computational engine. They will use the numerical solvers (like RK4) from the ODE course to simulate real-world physics that textbooks ignore because the math is "too hard."

* **Notebook 1: Projectile Motion and Aerodynamic Drag.** Textbooks always say "ignore air resistance." Your students won't. They will simulate a cannonball firing, add a velocity-squared drag force, and write an optimization loop to find the perfect launch angle to maximize distance (it's no longer 45 degrees!).
* **Notebook 2: Orbital Mechanics (The N-Body Problem).** Simulating gravity. They will start with the Earth orbiting the Sun, then add the Moon, and finally simulate an entire chaotic asteroid field using vectorized numpy arrays to calculate the gravitational pull between every single pair of objects simultaneously.
* **Notebook 3: Conservation Laws and Collisions.** Simulating a billiards break. They will write an event-driven simulation that detects when two 2D spheres intersect, calculates the transfer of momentum, and bounces them apart perfectly elastically.

### Unit 2: Oscillators and Resonance

Vibrations are the foundation of everything from acoustics to quantum mechanics.

* **Notebook 1: The Driven Damped Oscillator.** Simulating a mass on a spring with friction, while an external motor pushes it. They will slowly sweep the frequency of the motor to discover **resonance**, plotting the massive spike in amplitude when the motor matches the spring's natural frequency.
* **Notebook 2: Coupled Oscillators.** Two masses connected by three springs. They will use the eigenvalues of the system's matrix (tying back to Linear Algebra!) to find the "normal modes"—the specific ways the system can vibrate where everything moves in perfect harmony.
* **Notebook 3: Phase Space.** Instead of plotting position vs. time, they will plot velocity vs. position. They will see that a swinging pendulum draws a perfect circle in phase space, and adding friction causes that circle to spiral inward to a dead stop.

### Unit 3: Rotating Frames and Rigid Bodies

Physics gets weird when you are spinning. This unit deals with the "fictitious" forces and 3D tumbling.

* **Notebook 1: The Coriolis and Centrifugal Forces.** Students will simulate throwing a ball across a spinning merry-go-round. They will plot the ball's path from the perspective of someone on the ground (a straight line) and someone on the ride (a wild curve), proving these forces are just illusions of perspective.
* **Notebook 2: Foucault's Pendulum.** They will simulate a massive pendulum swinging at the North Pole, the Equator, and Paris, watching the rotation of the Earth slowly twist the plane of the swing over a 24-hour simulation.
* **Notebook 3: The Tennis Racket Theorem (Dzhanibekov Effect).** Simulating the 3D tumbling of a rigid body using the Moment of Inertia tensor. They will watch an object spin stably along two of its axes, but violently and chaotically flip back and forth when spun along its intermediate axis.

### Unit 4: Lagrangian Mechanics (The Energy Method)

This is where physics transcends $F = ma$. Instead of tracking forces and vectors, we just look at Kinetic Energy ($T$) and Potential Energy ($V$). The universe always takes the path that minimizes the "Action."

* **Notebook 1: The Principle of Least Action.** A purely computational proof. Students will generate a thousand random, squiggly paths a ball could take when thrown in the air. They will calculate the Action integral for every path, proving the standard parabola is the mathematical absolute minimum.
* **Notebook 2: Automated Equations of Motion.** The Euler-Lagrange equations require brutal calculus derivatives. Students will use Python's `sympy` (symbolic math library) to define $L = T - V$, allowing the computer to automatically derive the differential equations for them!
* **Notebook 3: The Double Pendulum (Revisited).** Using their new Lagrangian powers, they will easily derive the equations for the chaotic double pendulum—a task that is notoriously miserable using standard Newtonian force vectors—and simulate it.

### Unit 5: Hamiltonian Mechanics

The absolute peak of classical physics, and the direct precursor to Quantum Mechanics.

* **Notebook 1: Symplectic Integrators.** A major computational lesson. If you simulate a planet orbiting a star using standard RK4 for a million years, math errors build up and the planet spirals into the sun. Students will build a "Symplectic" algorithm that perfectly conserves the Hamiltonian (total energy) forever.
* **Notebook 2: Liouville's Theorem.** Students will drop a "cloud" of 1,000 random starting conditions into a phase space simulation. As the system evolves, the cloud will stretch and warp into crazy shapes, but they will computationally prove the area of the cloud remains exactly constant.
* **Notebook 3: The Restricted Three-Body Problem.** Simulating a spaceship traveling between the Earth and the Moon. They will use the Hamiltonian to map out the contour lines of effective potential, discovering the exact locations of the five stable Lagrange points ($L1$ through $L5$) where the James Webb Space Telescope currently lives.
