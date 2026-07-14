### Unit 1: Visualizing 4D Space (Domain Coloring)

Before we can do calculus on complex functions, we have to invent a way to look at them.

* **Notebook 1: The Complex Plane and Iteration.** Introducing `np.complex128`. Students will map a grid of complex numbers and apply iterative functions like $z_{n+1} = z_n^2 + c$. By tracking which numbers explode to infinity and which stay bounded, they will computationally construct the Mandelbrot Set.
* **Notebook 2: Domain Coloring.** The ultimate 4D visualization tool. Students will write an algorithm that assigns the **Phase** (angle) of the output to a color hue, and the **Magnitude** (distance from origin) to the brightness. Suddenly, $f(z) = z^2$ or $f(z) = e^z$ becomes a beautiful, readable heatmap of spiraling rainbows.
* **Notebook 3: Roots of Unity and Polynomials.** Solving $z^n = 1$. Students will plot the roots on the unit circle and build a script to visualize the Fundamental Theorem of Algebra, showing how a polynomial of degree $n$ always has exactly $n$ "color wheels" (roots) in its domain plot.

### Unit 2: Holomorphic Functions (The Geometry of Math)

Complex derivatives are unimaginably strict. A function is only "holomorphic" (complex-differentiable) if it preserves the shape of the universe.

* **Notebook 1: The Cauchy-Riemann Equations.** Students will computationally test functions by writing numerical partial derivatives for $u(x, y)$ and $v(x, y)$. They will see that non-holomorphic functions (like $f(z) = \bar{z}$) completely fail the Cauchy-Riemann checks.
* **Notebook 2: Conformal Mapping.** Holomorphic functions preserve local angles. Students will define a Cartesian grid of horizontal and vertical lines in the input plane. They will run this grid through $f(z) = z^2$ or the Joukowsky Transform (used in aerodynamics) and plot the output. The grid lines will bend and warp wildly, but they will computationally prove that the lines *still intersect at exactly 90 degrees everywhere*.
* **Notebook 3: Möbius Transformations.** The geometry of spheres. Students will code $f(z) = \frac{az+b}{cz+d}$ and create interactive sliders to change the parameters, watching how these transformations map circles to circles (or straight lines) across the complex plane.

### Unit 3: Contour Integration (The Magic of Cauchy)

This is where complex analysis becomes magical. Integrating in $\mathbb{C}$ means walking along a path.

* **Notebook 1: Path Integrals in $\mathbb{C}$.** Students will parameterize a curve $\gamma(t)$ and write a numerical integration loop to sum up $f(z) dz$ along the path.
* **Notebook 2: Cauchy's Integral Theorem.** The greatest theorem in complex analysis. Students will integrate a holomorphic function like $f(z) = z^2$ along a closed loop (a circle, a square, a crazy scribble). The loop will always output exactly $0 + 0i$. Then they integrate $f(z) = \frac{1}{z}$ and suddenly the answer jumps to exactly $2\pi i$, computationally discovering a "hole" at the origin.
* **Notebook 3: Cauchy's Integral Formula.** A spooky theorem that says if you know the values of a function on the boundary of a circle, you know its value everywhere inside. Students will write a script that only evaluates $f(z)$ on the edge of a circle, and uses an integral to perfectly predict the exact value at the center.

### Unit 4: Singularities and Residues

What happens when math breaks? In the complex plane, breaking is highly organized.

* **Notebook 1: Taylor and Laurent Series.** Taylor series approximate with positive powers. Laurent series use negative powers (like $\frac{1}{z^n}$) to handle singularities. Students will truncate these infinite series and plot their domain coloring, watching the approximation slowly wrap around the true function.
* **Notebook 2: Picard's Great Theorem.** Classifying singularities (Removable, Poles, and Essential). Students will domain-color the essential singularity $f(z) = e^{1/z}$. Picard's theorem states that near an essential singularity, a function takes on *every possible complex value infinitely many times*. The visualization for this is mind-blowing—an infinitely dense, repeating rainbow vortex.
* **Notebook 3: The Residue Calculus.** Students will numerically calculate the "Residue" (the coefficient of the $\frac{1}{z}$ term) at a pole. They will then use this complex trick to solve notoriously impossible real-world integrals, like $\int_{-\infty}^\infty \frac{1}{1+x^6} dx$, by throwing a semicircular contour into the complex plane.

### Unit 5: The Multi-Valued Universe

Tackling functions that give multiple answers at once, forcing us to redefine what "space" means.

* **Notebook 1: Branch Cuts.** What is the square root of $i$? Or the natural log of $-1$? Students will domain-color $f(z) = \sqrt{z}$ and $\ln(z)$ and find a "Branch Cut"—a violent, discontinuous tear in the colors where the math snaps.
* **Notebook 2: Riemann Surfaces.** To fix the tear, we must add dimensions. If 2D space isn't enough, we build a spiral staircase. Students will use 3D `plot_surface` to construct the Riemann surface for $\sqrt{z}$, showing how winding 360 degrees around the origin doesn't bring you back to where you started; it smoothly transitions you to a different "sheet" of the universe.
* **Notebook 3: Analytic Continuation.** How math discovers the unknown. Students will start with a Taylor series that only converges in a small circle. They will calculate its values near the boundary, generate a *new* Taylor series from that edge to step outside the circle, and computationally "discover" the rest of the function step-by-step (this is the exact math used to extend the Riemann Zeta function for the famous $1+2+3... = -1/12$ phenomenon).

