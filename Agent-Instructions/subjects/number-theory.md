### Unit 1: The Prime Frontier (Hunting for Indivisibility)

Primes are the atoms of mathematics. We start by teaching the computer how to find and count them efficiently.

* **Notebook 1: The Sieve of Eratosthenes.** A brute-force `for` loop checking divisibility is incredibly slow. Students will build the Sieve using a boolean `numpy` array, visually knocking out multiples to generate millions of primes in milliseconds, proving the computational power of $O(n \log \log n)$ algorithms.
* **Notebook 2: The Prime Number Theorem.** How dense are the primes? Students will write a counting algorithm $\pi(x)$ and plot it alongside the function $\frac{x}{\ln(x)}$. They will computationally witness the two curves perfectly merging as numbers get larger, proving Gauss's legendary approximation.
* **Notebook 3: The Ulam Spiral.** A purely visual sandbox. Students will map the integers onto a 2D spiral and color in only the primes. They will discover eerie, unexplained diagonal lines where primes naturally clump together, showing that the "random" primes actually harbor deep geometric secrets.

### Unit 2: Modular Arithmetic (The Math of Clocks)

Transitioning from standard algebra to finite fields, where numbers wrap around in circles.

* **Notebook 1: Fast Modular Exponentiation.** How do you calculate $7^{100} \pmod{13}$ when $7^{100}$ is too large to fit in a computer's memory? Students will write a "Repeated Squaring" algorithm, allowing Python to instantly calculate massive modular powers without ever calculating the massive actual number.
* **Notebook 2: Euler's Totient Function.** $\phi(n)$ counts how many numbers are relatively prime to $n$. Students will write an algorithm to calculate $\phi(n)$ by brute force, plot the scatter plot, and then discover the beautiful, lightning-fast shortcut: $\phi(p) = p - 1$ for primes.
* **Notebook 3: Fermat's Little Theorem.** Students will computationally verify Fermat's claim that $a^{p-1} \equiv 1 \pmod{p}$. Then, they will use this rule as a rudimentary "Prime Detector," writing a script that attempts to guess if a massive 50-digit number is prime without actually factoring it.

### Unit 3: Congruences and The Skeleton Keys

What happens when you need to "divide" in a math universe that doesn't have fractions?

* **Notebook 1: The Extended Euclidean Algorithm.** Students will upgrade the basic GCD algorithm to work backwards. They will write a recursive function that finds the exact linear combination (Bézout's identity), which acts as the computational skeleton key for finding Modular Inverses.
* **Notebook 2: The Chinese Remainder Theorem (CRT).** A 2,000-year-old puzzle: "Find a number that leaves a remainder of 2 when divided by 3, and 3 when divided by 5." Students will write a solver that takes arrays of remainders and moduli, using their modular inverse tool to instantly reconstruct the hidden number.
* **Notebook 3: Discrete Logarithms.** Finding $x$ in the equation $g^x \equiv h \pmod{p}$. Students will write a brute-force search and watch their computers completely freeze as the prime gets larger. They will mathematically experience why this "one-way function" is the bedrock of modern passwords.

### Unit 4: Primality and Factorization (Breaking the Code)

The cat-and-mouse game of cryptography: making big numbers and trying to break them apart.

* **Notebook 1: Carmichael Numbers (The Liars).** Students will use their Fermat prime detector from Unit 2, only to discover numbers like 561. 561 mathematically "fools" the test into thinking it is prime, even though $561 = 3 \cdot 11 \cdot 17$. They will build the Miller-Rabin Primality Test—a probabilistic algorithm that traps these liars.
* **Notebook 2: Pollard's Rho Algorithm.** Trial division is too slow. Students will write an algorithm that simulates a random walk on a modular graph. Using Floyd's "Tortoise and Hare" cycle-finding trick, they will crack composite numbers much faster than brute force.
* **Notebook 3: Quadratic Sieves (Conceptual).** Students will write a script to factor a number $N$ by searching for a difference of squares: $x^2 - y^2 = N$. This introduces the core mechanism behind the algorithms used to officially break RSA keys.

### Unit 5: Modern Cryptography (The Grand Finale)

We put all the tools together to build the systems that secure bank transfers and text messages.

* **Notebook 1: Diffie-Hellman Key Exchange.** How do two people agree on a secret password while screaming across a crowded room? Students will simulate Alice and Bob exchanging public numbers, combining them with their private numbers, and mathematically arriving at the exact same shared secret key.
* **Notebook 2: RSA Encryption.** The ultimate culmination of the course. Students will generate two massive primes, calculate the Totient, find the modular inverse to create public/private keys, and send an encrypted message that is mathematically impossible to decrypt without the prime factors.
* **Notebook 3: Elliptic Curve Cryptography (ECC).** Moving beyond simple integer primes. Students will graph an Elliptic Curve ($y^2 = x^3 + ax + b$) and write code to "add" two points together by drawing a secant line and reflecting it. They will see how this strange geometric pool table creates a cryptographic system that is exponentially harder to crack than RSA.

