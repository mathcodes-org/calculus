### Unit 1: The Power of Inference (Bootstrapping)

In probability, we knew the exact rules of the universe (e.g., a coin has a 50% chance of landing heads) and predicted the data. In statistics, we only have a tiny sample of messy data, and we have to guess the rules of the universe.

* **Notebook 1: Point Estimates and Sampling Bias.** Students are given a massive dataset (the "population") but are only allowed to randomly sample 100 rows. They will compute the sample mean and compare it to the true population mean, learning about sampling error and bias.
* **Notebook 2: Bootstrapping (The Hacker's Confidence Interval).** Instead of using complex calculus to find confidence intervals, students will write a loop that randomly resamples their 100 data points with replacement 10,000 times. They will plot the resulting distribution to visually find the 95% confidence interval.
* **Notebook 3: The Student's t-Distribution.** Introducing the mathematical backup to bootstrapping. When datasets are extremely small (under 30), normal distributions fail. Students will plot the t-distribution and watch the "tails" get thicker as the sample size shrinks.

### Unit 2: Hypothesis Testing (Simulation First)

Before introducing the classical formulas, teach them the logic of hypothesis testing through computational simulation.

* **Notebook 1: The Null Hypothesis and P-Values.** You give them data from two factory machines. Machine B seems slightly faster. Is it actually faster, or is it just random luck? They will learn how to formally define the Null and Alternative hypotheses.
* **Notebook 2: Permutation Tests (A/B Testing).** The ultimate computational proof. If Machine A and Machine B are truly identical (the Null Hypothesis), then swapping their labels shouldn't matter. Students will write a loop to shuffle all the labels 10,000 times, creating a simulated "Null Distribution." If their original data falls way outside this simulated bell curve, they have discovered statistical significance!
* **Notebook 3: Statistical Power and Type I/II Errors.** Students will write a simulation to test how often their algorithm produces False Positives (seeing a pattern that isn't there) and False Negatives (missing a real pattern), tweaking their sample size to see how "Power" increases.

### Unit 3: The Classical Toolkit (Parametric Tests)

Now that they understand the *logic* of a p-value through permutation, they can use the fast, mathematical shortcuts built into `scipy.stats`.

* **Notebook 1: T-Tests (1-Sample, 2-Sample, Paired).** Translating their permutation tests into single-line Python functions. They will learn how to test if a drug lowered blood pressure by comparing the "Before" and "After" arrays.
* **Notebook 2: ANOVA (Analysis of Variance).** What if we have *three* machines, or *four* drugs? Students will learn why running a dozen separate t-tests is mathematically dangerous (the multiple comparisons problem) and use ANOVA to test multiple groups simultaneously.
* **Notebook 3: Chi-Square Tests.** Moving from continuous data (height, weight) to categorical data (colors, brands). They will test if a casino's roulette wheel is actually fair by comparing expected frequencies to observed frequencies.

### Unit 4: Linear Modeling and Regression

This is where statistics becomes predictive. They built the Gradient Descent optimization in Calculus; now they will use the mathematical shortcuts to fit real data.

* **Notebook 1: Simple Linear Regression & Correlation.** Beyond just drawing a line of best fit. Students will calculate the residuals (the errors) and plot them to ensure the errors are completely random.
* **Notebook 2: Multiple Regression.** Predicting house prices using square footage, age, *and* zip code simultaneously. They will learn how to interpret the coefficients to isolate variables (e.g., "Holding age constant, an extra bedroom adds $50,000").
* **Notebook 3: The $R^2$ Metric and Overfitting.** Does adding more variables always make a model better? Students will see that adding literal random noise to a model can artificially inflate the math, introducing the concept of Adjusted $R^2$ and the danger of overfitting.

### Unit 5: Logistic Regression (The Machine Learning Bridge)

Ending the course by moving from predicting *numbers* to predicting *categories*. This is the direct gateway to Artificial Intelligence classification.

* **Notebook 1: The Sigmoid Function and Odds.** Why you cannot use a straight line to predict a Yes/No outcome (it will predict probabilities greater than 100% or less than 0%). Students will build the S-shaped sigmoid curve to constrain predictions between 0 and 1.
* **Notebook 2: Building a Classifier.** Predicting whether a simulated patient has a disease based on their blood test scores.
* **Notebook 3: The Confusion Matrix.** Evaluating their classifier. They will build a matrix to count True Positives, True Negatives, False Positives, and False Negatives, calculating the ultimate metrics of modern data science: Precision, Recall, and F1-Score.
