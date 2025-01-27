# Data Science Class Notes

## Key Concepts in Data Science
### Mathematical Foundations
- **Calculus**
- **Linear Algebra**
- **Probability and Statistics**

### Computer Science Fundamentals
- Programming
- Data Structures
- Algorithms

## Probability Concepts
### Frequentist Definition of Probability
- Probability is defined as the ratio of the number of favorable outcomes to the total number of trials.
- **Law of Large Numbers**: The more experiments we conduct, the closer the observed probability will be to the true probability.

### Event and Sample Space
- **Sample Space**: The set of all possible outcomes.
- **Event**: A subset of the sample space representing one or more outcomes.

### Dependent and Independent Events
- **Dependent Events**: Events where the outcome of one affects the outcome of another.
- **Independent Events**: Events where the outcome of one does not affect the outcome of another.

## Probability Calculations
### Joint Probability
- Probability of two events occurring together: $$P(A \cap B)$$

### Marginal Probability
- Probability of a single event irrespective of others: $$P(A)$$

### Conditional Probability
- Probability of one event given another: $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$.
- **Similarity to Hypothesis Testing**: Evaluates the likelihood of an event under certain conditions.

## Bayes' Theorem
- **Formula**: $$P(A|B) = \frac{P(B|A) P(A)}{P(B)}$$.
- Components:
  - **Prior**: Initial belief before observing data.i.e  $$P(A)$$
  - **Likelihood**: Probability of observing the data given the hypothesis. i.e $$P(B|A)$$
  - **Marginal**: Probability of a single event irrespective of others. i.e $$P(B)$$
  - **Posterior**: Updated belief after observing data.  $$P(A|B)$$

### Difference Between Conditional Probability and Bayes' Theorem
- **Conditional Probability**: Measures the likelihood of an event given another.
- **Bayes' Theorem**: Incorporates prior knowledge to update probabilities.

## Combinatorics and Distributions
### Combinatorics
- Fundamental in understanding probabilities of complex events.
- **Permutations**: Arrangements of items where the order matters.
  $$P(n, r) = \frac{n!}{(n-r)!}$$
- **Combinations**: Selections of items where the order does not matter.
  $$C(n, r) = \frac{n!}{r!(n-r)!}$$
- **Applications**: Useful in probability problems, such as calculating the number of ways to select subsets or arrange items.

### Binomial Distribution
- Describes the number of successes in a fixed number of independent Bernoulli trials.
- **Formula**:
  $$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$
  Where:
  - n: Number of trials
  - k: Number of successes
  - p: Probability of success in a single trial
- **Example**: Tossing a coin 10 times and counting the number of heads.

### Expected Value
- **Expected Value (E[X])**: The average outcome of a random variable over many trials.
  $$E[X] = \sum x \cdot P(x)$$
- **Variance**: Measures the spread of a random variable around its expected value.
  $$\text{Var}(X) = E[X^2] - (E[X])^2 $$
- **Applications**:
  - Predicting average outcomes.
  - Quantifying risk in uncertain scenarios.


## Information Theory
### Essence of Information Theory
- **Quantifying Uncertainty**: Measures unpredictability in data.

### Entropy
- **Definition**: A measure of uncertainty or randomness in a dataset.
- **Entropy Calculation**:
  $$H(X) = -\sum_{i=1}^n P(x_i) \log_2 P(x_i) $$

### Cross Entropy
- Measures the difference between two probability distributions.
- Useful in classification problems to evaluate predictions against true labels.

---


