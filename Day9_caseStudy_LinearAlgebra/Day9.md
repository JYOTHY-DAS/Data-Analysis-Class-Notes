# Data Science and Analytics Class Notes

## 1. Linear Regression

Linear Regression is a supervised machine learning algorithm used for **predicting continuous values**. It models the relationship between a dependent variable \( y \) and one or more independent variables X by fitting a linear equation to the observed data.

### Simple Linear Regression
In **simple linear regression**, the relationship between the dependent variable y and a single independent variable X is modeled as:
$$y = \beta_0 + \beta_1 X + \epsilon$$
Where:
- y is the predicted value.
- $$\beta_0$$ is the intercept.
- $$\beta_1$$ is the coefficient (slope) of the independent variable X.
- $$\epsilon$$ is the error term.

### Example:
Predicting the price of a house based on its size (square footage). The linear regression model might look like:
$$\text{Price} = 50,000 + 200 \times \text{Size (sq ft)}$$

---

## 2. Partial Derivative

A **partial derivative** is the derivative of a function with respect to one variable, while keeping the other variables constant. It's essential in optimization algorithms, particularly in **Gradient Descent** and **Backpropagation** for neural networks.

### Example:
In linear regression, we want to minimize the error between the predicted values and the actual values. The error function (commonly **MSE** – Mean Squared Error) involves multiple variables, and partial derivatives allow us to update each parameter (like the slope $$\beta_1$$ separately during optimization.

---

## 3. Logistic Regression

Logistic Regression is used for **binary classification** problems, where the output is categorical with two classes (e.g., 0 or 1, spam or not spam). Unlike linear regression, it predicts the probability of an event occurring.

### Logistic Function:
The model outputs a probability p using the logistic (sigmoid) function:
$$p = \frac{1}{1 + e^{-(\beta_0 + \beta_1 X)}}$$
Where:
- p is the predicted probability of the positive class (1).
- $$\beta_0$$ and $$\beta_1$$ are model parameters.
- X is the input feature.

### Example:
For a customer who has a score of 80 on a test, logistic regression might predict the probability of that customer purchasing a product as 0.85 (85%).

---

## 4. MSE (Mean Squared Error)

**Mean Squared Error (MSE)** is a common loss function used for regression tasks. It calculates the average of the squared differences between the actual and predicted values.

### Formula:
$$MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$$
Where:
- n is the number of data points.
- $$y_i$$ is the actual value.
- $$\hat{y}_i$$ is the predicted value.

### Example:
For a dataset of 5 house prices and their predicted values:
- Actual prices: [200,000, 300,000, 400,000, 500,000, 600,000]
- Predicted prices: [210,000, 290,000, 395,000, 490,000, 590,000]

The MSE calculates the average of squared errors between the actual and predicted prices, which helps us assess the model's accuracy.

---

## 5. Optimization Techniques

Optimization is the process of adjusting the parameters of a model to minimize the error (or loss function). There are several optimization techniques used in machine learning:

### 5.1 Gradient Descent

**Gradient Descent** is an iterative optimization algorithm used to minimize the loss function by adjusting the parameters in the direction of the negative gradient.

- Start with initial values for the parameters (e.g., $$\beta_0$$, $$\beta_1$$).
- Compute the gradient (partial derivatives of the loss function with respect to each parameter).
- Update the parameters by moving in the direction of the negative gradient:
  $$\theta = \theta - \alpha \cdot \frac{\partial}{\partial \theta} \text{(Loss)}$$
Where:
- $$\theta$$ represents the model parameters.
- $$\alpha$$ is the learning rate (step size).

### 5.2 Gradient Ascent

**Gradient Ascent** is similar to gradient descent, but instead of minimizing the loss function, it maximizes an objective function (e.g., likelihood in logistic regression).

- The update rule is:
$$\theta = \theta + \alpha \cdot \frac{\partial}{\partial \theta} \text{(Objective)}$$
Where:
- $$\theta$$ represents the parameters to be maximized.
- $$\alpha$$ is the learning rate.

### 5.3 Stochastic Gradient Descent (SGD)

**Stochastic Gradient Descent** (SGD) is a variation of gradient descent where the model parameters are updated after each individual training example, rather than after processing the entire dataset.

- This makes SGD faster than traditional gradient descent, especially for large datasets, but can introduce noise in the updates.

### Example:
Consider the task of training a linear regression model on a dataset of house prices. Using **Stochastic Gradient Descent**:
1. Start with a random initial guess for the model parameters.
2. Pick one training example at a time, calculate the gradient, and update the model parameters based on that one example.
3. Repeat until the model converges to the optimal parameters.
---
### 5.4 When to Use and When Not to Use Gradient Descent, Gradient Ascent, and Stochastic Gradient Descent (SGD)

### When to Use Gradient Descent:
- **Regression problems**: Gradient Descent is commonly used for **minimizing loss functions** in regression tasks (e.g., linear regression, logistic regression).
- **Convex objective functions**: Gradient Descent is ideal when the objective function is **convex**, meaning it has one global minimum. This ensures that the algorithm will converge to the global minimum.
- **Continuous and differentiable functions**: It is used when the loss function is **differentiable** and continuous, which allows the algorithm to compute the gradient (rate of change) of the function.

### When Not to Use Gradient Descent:
- **Non-convex objective functions**: If the problem has multiple local minima (e.g., training deep neural networks), **Gradient Descent** may get stuck in a local minimum instead of finding the global minimum.
- **High computational cost**: For large datasets, performing gradient descent on the entire dataset can be computationally expensive.

---

### When to Use Gradient Ascent:
- **Maximizing objective functions**: Gradient Ascent is used when you need to **maximize** an objective function rather than minimize a loss function (e.g., in **maximum likelihood estimation** or **reinforcement learning**).
- **Convex objective functions**: Similar to gradient descent, gradient ascent works well for convex functions where a global maximum is guaranteed.

### When Not to Use Gradient Ascent:
- **Minimization problems**: It is inappropriate for problems where the goal is to **minimize** a loss function (e.g., most classification and regression tasks).
- **Non-convex objective functions**: If the objective function has multiple local maxima, gradient ascent may converge to a local maximum instead of the global maximum.

---

### When to Use Stochastic Gradient Descent (SGD):
- **Large datasets**: SGD is effective for training on **large datasets** because it updates parameters after each individual data point, leading to faster convergence compared to batch gradient descent.
- **Online learning**: When new data continuously arrives, SGD can be used in **online learning** settings where the model parameters are updated iteratively as new data is received.
- **Real-time applications**: SGD is useful in situations where you need to quickly adjust the model as new data comes in or when the training data cannot be stored all at once.

### When Not to Use Stochastic Gradient Descent (SGD):
- **Small datasets**: If the dataset is small, **SGD** may not be necessary and could introduce excessive noise into the model. Batch gradient descent might be a more stable and accurate choice.
- **Convergence issues**: SGD can struggle with **convergence** because the noisy updates (due to individual data points) can cause the algorithm to oscillate around the minimum, making it less stable.
- **High variance**: For problems where the cost function is highly noisy or has high variance, SGD might not perform well without techniques like learning rate decay or momentum to stabilize the updates.

---

## Summary

| Method                        | Use When                                               | Avoid When                                               |
|-------------------------------|--------------------------------------------------------|----------------------------------------------------------|
| **Gradient Descent**           | Minimizing loss in regression problems, convex functions | Non-convex functions, high computational cost            |
| **Gradient Ascent**            | Maximizing objective functions, convex functions      | Minimization problems, non-convex functions              |
| **Stochastic Gradient Descent**| Large datasets, online learning, real-time applications| Small datasets, convergence issues, high variance        |

Each of these optimization techniques has its strengths and weaknesses, and choosing the right one depends on the size of the data, the nature of the function, and the specific problem you're solving.
---
## Note: Convex Functions and Non-Convex Functions

| Feature                        | Convex Functions                                        | Non-Convex Functions                                     |
|---------------------------------|---------------------------------------------------------|----------------------------------------------------------|
| **Minima**                      | Only one global minimum                                 | Multiple local minima and maxima                         |
| **Graph Shape**                 | A smooth, continuous curve (e.g., parabola)             | Multiple peaks and valleys                               |
| **Examples**                    | MSE in Linear Regression                                | Loss functions in Neural Networks                        |
| **Optimization Algorithms**     | Guaranteed to converge to the global minimum (e.g., Gradient Descent) | May get stuck in local minima (e.g., Gradient Descent)   |
