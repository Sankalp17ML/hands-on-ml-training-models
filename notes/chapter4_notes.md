# Chapter 4 — Training Models

## Learning Log

### Day 1 — Project Setup
- Created the project structure.
- Initialized Git.
- Created the first Jupyter notebook.


### Prediction
y_hat = X @ theta

### MSE Cost Function
MSE = (1/m) * sum((y_pred - y_actual)^2)

### Normal Equation
theta = inverse(X.T @ X) @ X.T @ y

### Pseudoinverse
theta = pinv(X) @ y

### Key Observations
- X.T represents matrix transpose.
- The Normal Equation minimizes training MSE.
- A matrix is singular if its determinant is zero.
- The pseudoinverse works even for singular matrices.
- Scikit-Learn learns the intercept automatically by default.

###DAY2

Batch Gradient Descent
\[
\theta_{\text{next}}=\theta-\eta\frac{2}{m}X^T(X\theta-y)
\]

Stochastic Gradient Descent
\[
\theta_{\text{next}}=\theta-\eta\nabla J_i(\theta)
\]

Polynomial Regression
\[
\hat y=\theta_0+\theta_1x+\theta_2x^2
\]


## Learning Curves

**Definition:** Learning curves show how a model's training and validation errors change as the number of training instances increases.

**Purpose:** Identify underfitting, overfitting, and whether adding more training data will improve performance.

### Key Concepts
- **X-axis:** Number of training instances.
- **Y-axis:** Error (usually RMSE).
- **Training error:** Error on data used for training.
- **Validation error:** Error on unseen validation data.

### Interpreting Learning Curves

| Underfitting (High Bias) | Overfitting (High Variance) |
|---|---|
| High training error | Low training error |
| High validation error | High validation error |
| Small gap between curves | Large gap between curves |
| Use a more flexible model | Add data or regularization |

### Important Code
- `learning_curve()` — evaluates a model using different training sizes.
- `train_sizes` — number of training instances used.
- `cv=5` — five-fold cross-validation.
- `neg_root_mean_squared_error` — negative RMSE scoring.
- `.mean(axis=1)` — averages scores across CV folds.

### Key Takeaways
- Learning curves help diagnose bias and variance.
- Adding more data may help overfitting but usually won't fix underfitting when errors have plateaued.
- A good model has low training and validation errors with a small gap.