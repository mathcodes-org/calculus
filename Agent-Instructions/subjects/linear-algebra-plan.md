### Unit 1: The Geometry of Vectors

Traditional classes often start with matrices, but we should start with vectors to build spatial intuition.

* **Notebook 1: Vectors as Arrows and Data.** Transitioning from arrows in 2D space (physics) to lists of numbers in 100-dimensional space (computer science). Using `matplotlib` to draw vector additions.
* **Notebook 2: The Dot Product and Similarity.** Teaching the dot product not just as a geometric projection, but as a measure of similarity. This is the perfect place to introduce a micro-project on "Recommendation Engines" (e.g., finding the angle between a user's movie preferences and an item's tags).
* **Notebook 3: The Cross Product and Planes.** Expanding into 3D. Calculating normal vectors to define planes and visualizing them with `plot_surface`.

### Unit 2: Linear Transformations (The Core Intuition)

This is where the matrix is introduced, not as a spreadsheet of numbers, but as a mathematical function that warps space.

* **Notebook 1: Matrices as Movers.** Multiplying a 2D matrix by a grid of vectors. Students will animate a square grid shearing, rotating, and scaling.
* **Notebook 2: Matrix Multiplication (Composition).** Proving computationally that multiplying two matrices is just applying one transformation followed by another. Proving that $AB \neq BA$ by visually rotating then shearing versus shearing then rotating.
* **Notebook 3: The Determinant.** Visually proving that the determinant is simply the scaling factor for area/volume. If the determinant is zero, the 2D grid collapses into a 1D line!

### Unit 3: Solving Systems ($A\vec{x} = \vec{b}$)

Connecting transformations back to classic algebra.

* **Notebook 1: The Inverse Matrix.** If a matrix transforms space, the inverse simply plays the tape in reverse. Students will write code to transform a dataset, then use `np.linalg.inv` to perfectly reconstruct the original data.
* **Notebook 2: Gaussian Elimination (The Engine).** Having them code a basic row-reduction algorithm so they understand what `np.linalg.solve` is doing under the hood.
* **Notebook 3: Overdetermined Systems.** What happens when you have 100 equations and only 2 variables? Introducing Least Squares Regression via the pseudo-inverse to fit a line to noisy data.

### Unit 4: Eigen-Everything

The most important, yet notoriously confusing, concept in the subject made purely visual.

* **Notebook 1: Eigenvalues and Eigenvectors.** Finding the special vectors that don't get knocked off their line during a transformation. Students will plot a transformation and overlay the eigenvectors to see them perfectly scale without rotating.
* **Notebook 2: PageRank (Google's Secret).** A massive real-world application. Using the dominant eigenvector of a web-link matrix to rank the importance of simulated websites.
* **Notebook 3: Markov Chains.** Simulating state changes over time (e.g., weather prediction or stock market trends) using matrix exponentiation.

### Unit 5: The Data Science Finale

Ending the course by proving that linear algebra is the engine of modern computing.

* **Option A: Principal Component Analysis (PCA).** Taking a high-dimensional dataset (like housing data) and using the covariance matrix to project it down to 2D for visualization, preserving the most variance.
* **Option B: Image Compression via SVD.** Using Singular Value Decomposition to break a high-resolution image into matrices. Students drop the lowest singular values and reconstruct the image, watching the file size shrink while the image remains recognizable.
