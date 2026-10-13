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