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
- **Dependent Events**: Events where the outcome of one affects the outcome of another. Eg:
  -	Drawing cards from a deck without replacement
  -	Weather and outdoor activities: If it's raining, the probability of playing outdoor sports decreases. The two events, "it's raining" and "playing outdoor sports," are dependent.
  -	Examining a faulty product: If a product is found to be defective, the probability of finding another defective product in the same batch increases.
  -	Traffic conditions and commute time: Heavy traffic can delay your commute time. The two events, "heavy traffic" and "longer commute time," are dependent.
  -	In sports: Two events, “Star player of a team gets injured” and “Team wins the game” are dependent. The occurrence of the first event directly impacts the probability of the second event.

- **Independent Events**: Events where the outcome of one does not affect the outcome of another. Eg:
  -	Tossing a coin twice: The outcome of the first toss (heads or tails) does not influence the outcome of the second toss.
  -	Rolling two dice: The number rolled on one die does not affect the number rolled on the other die. 
  -	Drawing a card from a deck with replacement: If you draw a card, record its value, and then replace it before drawing the next card, the probability of drawing a specific card remains the same for each draw. 
  -	Choosing a random number between 1 and 10: The number chosen in one trial does not influence the number chosen in the next trial. 
  -	Flipping a coin and rolling a die: The outcome of the coin flip does not affect the outcome of the die roll.


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
- Expected value is also referred to as statistical expectation, mean or average, depending on the context:
  - Statistical Expectation: A formal term used in probability and statistics.
  - Mean: Commonly used in statistical analysis to denote the arithmetic average.
  - Average: A more informal term for the same concept.

---
# Information Theory

Information Theory is a branch of mathematics that deals with the quantification of information. It plays a crucial role in areas like data compression, coding theory, and machine learning. Let’s break down some key concepts:

## Essence of Information Theory

The main goal of Information Theory is to quantify uncertainty or unpredictability in data. In real-life scenarios, we often deal with information that is uncertain, like predicting the weather or classifying images. Information Theory provides tools to measure this uncertainty and optimize how we represent and communicate information.

## Quantifying Uncertainty: Measures of Unpredictability in Data

When you’re dealing with any data, there’s always some level of unpredictability. This means that the outcome of an event isn’t always known in advance. In Information Theory, we use a few mathematical tools to measure this uncertainty.

## Entropy

### Definition: A Measure of Uncertainty or Randomness in a Dataset

Entropy is the most important concept in Information Theory. It’s used to quantify how uncertain or random a dataset is. Imagine you are trying to predict the outcome of an event, like rolling a fair six-sided die. The outcome is uncertain, and each roll has an equal chance of resulting in one of six possible values. The higher the entropy, the more unpredictable or uncertain the dataset is.

### Entropy Calculation

The entropy of a random variable $$X$$ is calculated using the formula:

$$H(X) = - \sum_{i=1}^{n} P(x_i) \log_2 P(x_i)$$

Where:
- $$H(X)$$ is the entropy of the dataset $$X$$,
- $$P(x_i)$$ is the probability of each outcome $$x_i$$,
- The sum goes over all possible outcomes in the dataset.

**Example:**

Imagine you have a biased coin that lands heads 70% of the time and tails 30% of the time. The entropy for this coin flip is calculated as:

$$H(X) = - \left[ P(\text{Heads}) \log_2 P(\text{Heads}) + P(\text{Tails}) \log_2 P(\text{Tails}) \right]$$
$$H(X) = - \left[ 0.7 \log_2 0.7 + 0.3 \log_2 0.3 \right]$$
$$H(X) \approx 0.88 \text{ bits}$$
This means that there’s some uncertainty in predicting the outcome of the biased coin, but it’s not as uncertain as a fair coin (which has a higher entropy).

### Why It’s Useful:

Entropy helps in measuring the “amount of surprise” in a dataset. For example, if you're predicting outcomes (like weather), understanding the entropy of your data helps you gauge how unpredictable or chaotic the data is. A high entropy means high uncertainty (lots of unpredictability), while low entropy means low uncertainty (more predictable).

## Cross Entropy

### Definition: Measures the Difference Between Two Probability Distributions

Cross Entropy is a measure of the difference between two probability distributions. In machine learning, it’s used to compare the true distribution of the data (the actual labels) with the predicted distribution (the model's predicted labels). It helps evaluate how well the model is performing by quantifying how different its predictions are from the actual labels.

### Why It’s Useful in Classification Problems

In classification tasks, where you’re trying to predict categories (e.g., spam vs. not spam emails), cross entropy helps evaluate how close your model’s predictions are to the true outcomes. If your model’s predictions are perfect, the cross-entropy will be low. If your model makes incorrect predictions, the cross-entropy will be high.

### Cross Entropy Formula

The cross-entropy between two distributions P (true labels) and Q (predicted labels) is given by:

$$H(P, Q) = - \sum_{i=1}^{n} P(xi) \log_2 Q(xi) $$

Where:
- $$P(x_i)$$ is the true probability of outcome $$ xi $$.
- $$Q(x_i)$$ is the predicted probability of outcome $$xi$$.

**Example:**

Let’s say you have a binary classification problem where you’re trying to predict whether an email is spam (1) or not spam (0). The true label for a certain email is 1 (spam), and the model predicts 0.9 probability that the email is spam.

The cross-entropy would be calculated as:

$$H(P, Q) = - \left[ P(\text{Spam}) \log_2 Q(\text{Spam}) + P(\text{Not Spam}) \log_2 Q(\text{Not Spam}) \right]$$
$$H(P, Q) = - \left[ 1 \log_2 0.9 + 0 \log_2 0.1 \right] \approx 0.15 \text{ bits}$$

The lower the cross-entropy, the better the model's predictions are.

## Summary

- **Entropy** measures the uncertainty or randomness in data. It tells you how unpredictable the data is.
- **Cross Entropy** measures how different two probability distributions are. In machine learning, it’s used to compare predicted outcomes with true labels and evaluate the model’s performance.

Understanding these concepts is essential for working with data, especially in fields like machine learning, where you often deal with classification problems and need to assess the quality of your predictions.




