# Inferential Statistics

## Binomial Distribution
- A discrete probability distribution used for a fixed number of trials, where each trial has only two possible outcomes (success or failure).
- Example: Tossing a coin 10 times and counting the number of heads.

---

## Probability
- **Definition**: The likelihood of an event occurring.
- Central Limit Theorem: As the number of trials increases, the distribution becomes more like a bell curve.
- **Example**: Calculating the probability of rolling a 6 on a die.

---

## Gaussian Distribution
- Also known as the **Normal Distribution**.
- A continuous probability distribution that is symmetric and bell-shaped.
- Commonly observed in natural phenomena, such as heights, test scores, and measurement errors.

---

## Sampling
- **Definition**: Selecting a subset of data from a population to make inferences about the entire population.
- **Use Case**: Conducting a survey of 1,000 people to understand the opinions of a city’s population.

---

## Central Limit Theorem (CLT)
- **Key Concept**: Regardless of the population's distribution, the sampling distribution of the sample mean approaches a normal distribution as the sample size increases.
- **Importance**:
  - Forms the foundation of inferential statistics.
  - Justifies the use of normal distribution for hypothesis testing.

---

## Hypothesis Testing/Court: Evidence based approach (Null Hypothesis vs Alternate Hypothesis)
- "court" is a metaphor used to illustrate the concept of evidence-based decision-making. It draws a parallel between a court trial and hypothesis testing in statistics.

-In a courtroom setting:
  - The Null Hypothesis (H₀): The defendant is innocent.
  - The Alternative Hypothesis (H₁): The defendant is guilty.
  - The Evidence: The data collected during the trial (witnesses, facts, proof, etc.).
  - Decision: Based on the evidence, the court either fails to reject the null hypothesis (innocent) or rejects it in favor of the alternative hypothesis (guilty).

-In hypothesis testing:
  - The Null Hypothesis (H₀): The default assumption (e.g., "no effect," "no difference").
  - The Alternative Hypothesis (H₁): The claim we aim to support (e.g., "there is an effect," "there is a difference").
  - The Evidence: The sample data analyzed using statistical methods.
  - Decision: Based on the p-value and the chosen significance level (𝛼), we either fail to reject 𝐻0 (no sufficient evidence) or reject 𝐻0 in favor of 𝐻1 (sufficient evidence exists).

## Significance Level (Alpha Value)
- **Definition**: The threshold for rejecting the null hypothesis.
- **Common Value**: 0.05 (5%).
- Represents the probability of making a Type I error (rejecting a true null hypothesis).

---

## P-Value
- **Definition**: The probability of obtaining results at least as extreme as the observed results, assuming the null hypothesis is true.
- **Key Points**:
  - If 𝑃 > 𝛼, fail to reject the null hypothesis.
  - If 𝑃 &le; 𝛼, reject the null hypothesis.
- **Example**:
  - Null Hypothesis: A new drug has no effect.
  - Alternate Hypothesis: The new drug improves patient recovery.

---

## Z-Test
- **Used When**:
  - Sample size is large (n &ge;30).
  - Population standard deviation is known.
  - Data is approximately normally distributed.
- **Example**: Comparing the mean test scores of two large student groups to evaluate teaching methods.

---

## T-Test
- **Used When**:
  - Sample size is small.
  - Population standard deviation is unknown.
- **Types**:
  - **One-sample T-test**: Compares the sample mean to a known value.
  - **Two-sample T-test**: Compares the means of two independent groups.
  - **Paired T-test**: Compares means of the same group at two different times.
- **Use Case**: Testing whether a new teaching method improves test scores compared to the old method.

